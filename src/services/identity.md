# Identity Layer

## Introduction

The **Identity Layer** in Florune provides **self-sovereign, blockchain-backed digital identity and credentials**. It enables users, businesses, and organizations to **verify identity and credentials securely, privately, and without reliance on centralized authorities**.

This layer is designed for:

* **Individuals**: managing personal identity and credentials
* **Organizations**: verifying employee, partner, or vendor credentials
* **Developers**: integrating decentralized identity and verifiable credentials into smart contract workflows

All services in this layer are built on **open standards** to ensure interoperability, privacy, and security.

---

## Layer Overview

| Layer Name     | Description                                                                                        | Services                                                   |
| -------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Identity Layer | Provides self-sovereign identity and verifiable credentials for secure, decentralized verification | Decentralized Identity (DID), Verifiable Credentials (VCs) |

**Key Objectives of the Layer:**

* Provide **user-controlled, portable digital identities**
* Enable **secure verification without centralized intermediaries**
* Support **verifiable presentations** for privacy-preserving data sharing
* Integrate seamlessly with Florune’s contracts and document services

---

## Services in Identity Layer

### 1. Decentralized Identity (DID)

**Purpose:**
Enable lightweight, self-sovereign digital identity that is **fully user-controlled, portable, and privacy-preserving**.

**Key Features:**

* Based on **ERC-1056** Ethereum standard
* Fully **user-controlled** – no centralized authority required
* Portable
* Compatible with W3C **verifiable credentials** v2.0
* Secure and cryptographically verifiable

**How It Works:**

1. User creates a DID linked to their blockchain wallet.
2. The DID stores essential metadata and public keys/delegates on-chain.
3. Users control access to their identity data through wallet authorization.
4. Can be used for verifying agreements, documents, and interacting with services.

**Use Case Example:**

* A freelancer registers a DID to authenticate themselves on multiple platforms, providing a verifiable, tamper-proof identity without relying on centralized providers.

**Benefits:**

* **Self-sovereignty** – full user control of identity
* **Interoperability** – compatible with decentralized apps and smart contracts
* **compliance** – uport integration
* **Security** – cryptographic proof of identity, self identifying with EOA's

---

### 2. Verifiable Credentials (VCs)

**Purpose:**
Provide **wallet-first, blockchain-backed digital credentials** that are tamper-proof, privacy-preserving, and verifiable.

**Key Features:**

* Compliant with **W3C Verifiable Credentials v2.0**
* Blockchain-backed and tamper-proof
* Supports **verifiable presentations**
* Can represent education certificates, licenses, compliance documents, or professional credentials

**How It Works:**

1. Credential issuer creates a verifiable credential for a user.
2. Credential metadata and proof are recorded on-chain.
3. User stores credentials in their wallet and selectively shares informations and proofs with third parties.
4. Recipients can verify authenticity without needing direct access to the issuer.

**Use Case Example:**

* A university issues a blockchain-backed diploma to a graduate. The graduate can present proof to employers without exposing sensitive information, and employers can independently verify its authenticity.

**Benefits:**

* **Trustless Verification** – verifiable without a central authority
* **Privacy-Preserving Sharing** – selective disclosure for sensitive data
* **Tamper-Proof** – blockchain ensures integrity and immutability

---

## Layer Benefits Summary

| Service                      | Key Advantages                                          |
| ---------------------------- | ------------------------------------------------------- |
| Decentralized Identity (DID) | Self-sovereign, portable, secure identity               |
| Verifiable Credentials (VCs) | Blockchain-backed credentials with selective disclosure |

**Overall Layer Benefits:**

1. **User-Controlled Identity** – Full autonomy over personal or organizational identity.
2. **Secure Verification** – Blockchain ensures authenticity and prevents tampering.
3. **Privacy & Selective Sharing** – Share only what is necessary.
4. **Integration with Florune Services** – Identity and credentials can seamlessly interact with payment, document, and content layers.
5. **Standardized & Interoperable** – Built on ERC-1056 and W3C standards for broad compatibility.

---

The **Identity Layer** empowers users with **trustworthy, self-sovereign digital identity and credentials**, enabling **secure, verifiable interactions** across Florune’s ecosystem. By combining DIDs with verifiable credentials, Florune supports **privacy-preserving, interoperable, and blockchain-backed identity solutions** suitable for individuals, businesses, and developers alike.
