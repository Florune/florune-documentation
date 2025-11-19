# DID

## Overview

**DID** stands for **Decentralized Identifier**. A DID is a globally unique identifier that allows its controller to prove cryptographic control over it. The entity controlling a DID is called the **controller**. DIDs are not limited to humans—they can represent organizations, devices, data models, or any abstract entity.

> A DID identifies any subject (e.g., person, organization, device, or data model) that the controller decides it identifies.

DIDs are persistent identifiers: even if the associated cryptographic material changes, the DID itself does not need to change. A single DID can have multiple keys, and these keys can be rotated independently. DIDs are typically shorter than the raw public keys they use, making them convenient as stable identifiers.

Each DID is associated with a **DID Document**, which describes:

* The subject of the DID
* Public keys (verification methods)
* Authentication mechanisms
* Authorized controllers
* Service endpoints for interaction

---

## DID Methods

A DID method defines how DIDs are created, resolved, and updated. It specifies:

* The DID format
* Supported operations (key rotation, adding controllers, etc.)
* Cryptography and encoding

Here we focus on **two DID methods**: `did:key` and `did:ethr` (ERC‑1056).

---

## did:key

`did:key` is a **purely generative DID method**. The DID is deterministically derived from a public key, so there is **no registry or blockchain** involved.

### Syntax

```
did:key:<multibase-encoded-public-key>
```

Example:

```
did:key:z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK
```

* The DID itself encodes the key using **multicodec** and **multibase**.
* There is **no need for transactions or on-chain storage**.

### DID Document

A `did:key` DID Document includes:

* `verificationMethod`: public key(s) derived from the DID
* `authentication` and `assertionMethod`: keys authorized for signing and verification
* `keyAgreement` (optional): derived keys for encryption

Example:

```json
{
  "@context": ["https://www.w3.org/ns/did/v1"],
  "id": "did:key:z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK",
  "verificationMethod": [
    {
      "id": "did:key:z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK#z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK",
      "type": "Ed25519VerificationKey2018",
      "controller": "did:key:z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK",
      "publicKeyMultibase": "z<multibase-encoded-key>"
    }
  ],
  "authentication": [
    "did:key:z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK#z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK"
  ],
  "assertionMethod": [
    "did:key:z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK#z6MkhaXgBZDvotDkL5257faiztiGiC2QtKLGpbnnEGta2doK"
  ]
}
```

**Key points**:

* The DID is **self-controlled** (the key is its own controller).
* There is **no need for registration**, and the DID Document can always be derived from the public key.

---

## did:ethr (ERC‑1056)

`did:ethr` is a DID method **anchored on Ethereum** using the **ERC‑1056 Lightweight Identity** standard.

### Overview

ERC‑1056 defines an **on-chain identity registry** that enables:

* Adding/removing **delegates** for signing or key management
* Adding **attributes** such as service endpoints or verification keys
* Rotating keys or updating controllers
* Tracking actions via Ethereum transactions

The DID method allows DIDs to be **self-sovereign** while anchored on Ethereum for verification and persistence.

### Syntax

```
did:ethr:<ethereum-address>
```

Example:

```
did:ethr:0xAbC123456789abcdef123456789abcdef1234567
```

For testnets:

```
did:ethr:goerli:0xAbC123456789abcdef123456789abcdef1234567
```

### DID Document

When resolved, the DID Document includes:

* `verificationMethod`: keys/delegates registered on-chain
* `authentication`: keys authorized for authentication
* `service`: optional endpoints registered as attributes
* `controller`: the Ethereum address or delegates controlling the DID

Example:

```json
{
  "@context": ["https://www.w3.org/ns/did/v1"],
  "id": "did:ethr:0xAbC123456789abcdef123456789abcdef1234567",
  "controller": "did:ethr:0xAbC123456789abcdef123456789abcdef1234567",
  "verificationMethod": [
    {
      "id": "did:ethr:0xAbC123456789abcdef123456789abcdef1234567#delegate-1",
      "type": "EcdsaSecp256k1RecoveryMethod2020",
      "controller": "did:ethr:0xAbC123456789abcdef123456789abcdef1234567",
      "publicKeyHex": "02ab..."
    }
  ],
  "authentication": [
    "did:ethr:0xAbC123456789abcdef123456789abcdef1234567#delegate-1"
  ],
  "service": [
    {
      "id": "did:ethr:0xAbC123456789abcdef123456789abcdef1234567#linked-domain",
      "type": "LinkedDomains",
      "serviceEndpoint": ["https://example.com"]
    }
  ]
}
```

**Key points**:

* The DID is **anchored on-chain**, allowing verifiable and auditable changes.
* Only delegates or the Ethereum address itself can update keys, controllers, or service endpoints.
* Updates require **Ethereum transactions**, which may incur gas costs.

---

## Comparison: did:key vs did:ethr

| Feature                       | `did:key`                           | `did:ethr` (ERC‑1056)                        |
| ----------------------------- | ----------------------------------- | -------------------------------------------- |
| **Storage**                   | Fully off-chain                     | On-chain registry (Ethereum)                 |
| **Cost**                      | Free                                | Gas required for updates                     |
| **Key Rotation / Delegation** | Not possible (new key = new DID)    | Supported via delegates and registry updates |
| **Controller**                | Implicitly the key itself           | Ethereum address or delegates                |
| **Service Endpoints**         | Derived or included in resolved DID | Stored as on-chain attributes                |
| **Trust / Decentralization**  | Fully decentralized                 | Dependent on Ethereum and registry contract  |

---

## Summary

* `did:key` is **simple and deterministic**, ideal for ephemeral or off-chain DIDs.
* `did:ethr` is **Ethereum-backed**, supporting verifiable, auditable, and self-sovereign identities on-chain.
* Both methods resolve to DID Documents that specify keys, controllers, authentication, and services.

---

## **Contract DID**

**Decentralized Identifiers (DIDs)** are a cornerstone of identity in decentralized systems, enabling users, organizations, and digital assets to have **self-sovereign, verifiable identities**. In the context of smart contracts, Florune introduces **Contract DIDs** — a method of assigning globally unique identifiers to deployed contracts, registries, and other on-chain entities, while maintaining **privacy and controlled access**.

Contract DIDs serve as **cryptographic handles** that represent deployed contracts or registries on a blockchain. They allow users to reference, interact with, or verify these entities without exposing sensitive internal data.

---

### **Structure of Contract DID**

A **Contract DID** is constructed in the following format:

```
did:ethr:<chain-id>:<contract-id-hex>[;key=<cipher-key-hex>]
```

* **did:ethr** – Indicates that this is an Ethereum-compatible DID.
* **<chain-id>** – The chain ID where the contract is deployed.
* **<contract-id-hex>** – The unique identifier of the deployed contract in hexadecimal format.
* **key=<cipher-key-hex> (optional)** – A private cipher key used for securing contract data. **This key must never be shared with unrelated parties**, as possession allows decryption of sensitive contract information.

Example:

```
did:ethr:1:0x4b3c7a9e5f2d3a6b8c9d0e1f2a3b4c5d6e7f8a9b;key=0a1b2c3d4e5f67890123456789abcdef
```

In this example:

* The contract is deployed on **Ethereum mainnet (chain-id 1)**.
* The contract’s address is `0x4b3c7a9e5f2d3a6b8c9d0e1f2a3b4c5d6e7f8a9b`.
* A **private cipher key** is associated to encrypt sensitive contract state.

---

### **Registry DID**

Contracts often interact with registries — on-chain data structures that **map, verify, or index other contracts, users, or assets**. Registry DIDs are assigned in a simpler format to reference these registries:

```
did:ethr:<chain-id>:<32byte-hash-hex>
```

* **<chain-id>** – Blockchain network where the registry resides.
* **<32bit-hash-hex>** – A unique hash representing the registry or dataset.

Example:

```
did:ethr:5:0x9f8a7b6c5d4e3f2a1b0c1d2e3f4a5b6c7d8e9f0a1b2c3d4e5f6a7b8c9d0e1f2
```

Registries can store mappings of **users to their Contract DIDs**, smart contract metadata, or verifiable records, enabling **tamper-proof lookup, automated verification, and secure referencing**.

---

### **Usage and Privacy Considerations**

* Contract DIDs allow **users to interact with contracts** securely by referring to a permanent on-chain identifier without needing the raw contract address.
* Sensitive data inside contracts or registries can be **encrypted with the private key parameter** (`key=<cipher-key-hex>`).
* Only authorized parties should be given access to the cipher key; sharing it externally may compromise the security of encrypted contract data.
* Users can query registries using **Registry DIDs** to discover or verify associated Contract DIDs, enabling decentralized discovery while maintaining privacy.

---

### **Key Benefits**

1. **Decentralized Reference**: Provides a global, verifiable identifier for smart contracts and registries.
2. **Secure Access Control**: Optional cipher keys allow encrypted contract states to remain confidential.
3. **Tamper-Proof Registry Mapping**: Registry DIDs provide a verifiable method to index contracts and users.
4. **Interoperability**: Compatible with Ethereum and EVM-based chains, making Contract DIDs usable across multiple networks.

---

This structure ensures that Florune users can **maintain self-sovereign identity for contracts and registries**, interact securely with encrypted smart contracts, and trust the authenticity of registry data without relying on centralized services.
