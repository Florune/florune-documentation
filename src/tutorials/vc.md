# Verifiable Credentials

*Wallet-first, privacy-preserving credentials compliant with W3C VC v2.0 and anchored to Florune DIDs.*

---

## **Overview**

Florune’s **Verifiable Credentials (VCs)** provide a secure, decentralized way to issue, verify, and present proofs of:

* Skills & achievements
* Education & training
* Compliance & licenses
* Membership & identity attributes
* Business records or attestations

VCs are:

* **Tamper-proof** (cryptographically verifiable)
* **Self-sovereign** (stored in the user’s wallet)
* **Portable** across networks and platforms
* **Privacy-preserving** via **selective disclosure & verifiable presentations**
* **Built on W3C Verifiable Credential v2.0**

A VC is signed by the issuer’s **DID**, held by the subject’s **wallet**, and verifiable by any third party.

---

## **Context & Problem**

### **The Problem**

Traditional credentials (certificates, licenses, IDs) have challenges:

* Easy to forge or manipulate
* Hard to verify internationally
* Require centralized authorities
* Reveal too much personal data
* Slow manual verification processes
* Not portable across platforms

Users and organizations need **trusted, private, standardized digital credentials** that work anywhere.

### **The Solution**

Florune VCs:

* Are **verified via blockchain + DID signatures**
* Require **no central authority**
* Support **selective disclosure** (only reveal what’s necessary)
* Allow **flexible proof presentations**
* Can represent **any type of claim** — academic, corporate, legal, or personal

VCs integrate deeply with Florune’s identity and document ecosystem, powering secure B2B and P2P verification workflows.

---

## **Use Cases**

### **1. Education & Certification**

* Schools issue degrees or certificates as VCs
* Training centers issue completion badges
* Students share credentials without revealing full identity

### **2. Enterprise Compliance**

* Employees receive compliance certifications (e.g., AML/KYC training)
* Contractors prove qualifications before engagement
* Auditors verify digital proof instantly

### **3. Talent & Freelancing**

* Freelancers present verified work history or skill credentials
* Clients validate identity attributes without exposing personal details

### **4. Legal & Regulatory**

* Businesses issue licenses or compliance documents
* Individuals prove age or residency using selective disclosure
* Lawyers validate document issuance via VCs

### **5. Web3 & Onchain Reputation**

* Proof-of-contribution credentials
* DAO participation records
* Reputation scoring anchored to DID

---

## **Key Features**

### **1. W3C VC v2.0 Compliant**

Ensures global compatibility with web3 wallets, institutions, and verifiers.

### **2. Self-Sovereign Storage**

Credentials stay in the payer’s device — **no platform custody**.

### **3. Selective Disclosure**

Users reveal **only the needed fields** to a verifier.

### **4. DID-Based Signing**

Both issuer and holder use their **Decentralized Identity (DID)**.

### **5. Blockchain Anchoring**

Credential hashes or metadata can be anchored onchain for immutability.

### **6. Revocation Support**

Issuers can revoke credentials using their DID keys (if issued with revocation registry).

---

## **Credential Structure (Simplified Example)**

```json
{
  "@context": ["https://www.w3.org/2018/credentials/v2"],
  "type": ["VerifiableCredential", "EducationCertificate"],
  "issuer": "did:erc1056:0xABC...",
  "credentialSubject": {
    "id": "did:erc1056:0x123...",
    "name": "John Doe",
    "course": "Blockchain Development"
  },
  "proof": {
    "type": "EcdsaSecp256k1Signature",
    "created": "2025-01-01T00:00:00Z",
    "proofPurpose": "assertionMethod",
    "verificationMethod": "did:erc1056:0xABC#owner",
    "signatureValue": "0x..."
  }
}
```

---

# **Step-by-Step Tutorial**

## **A. Receiving a Credential**

1. Open the Florune Wallet
2. Navigate to **Identity → Credentials**
3. Tap **Receive VC**
4. Scan QR code / paste credential payload
5. Wallet verifies:

   * Issuer DID
   * Signature
   * Expiration & revocation (if applicable)
6. Accept and store the VC locally

Your VC is now available for presentations or sharing.

---

## **B. Issuing a Credential**

### Prerequisites

* Your DID must be initialized
* You must have issuer permissions in your workflow
* (Optional) Verifiable Document to attach additional files

### Steps

1. Navigate to **Issue Credential**
2. Fill in the credential fields:

   * Type (certificate, membership, license…)
   * Subject DID
   * Data fields
3. (Optional) Attach Verifiable Document
4. Tap **Issue**
5. Wallet signs VC using issuer’s DID
6. Share VC with subject via:

   * QR Code
   * Direct import
   * Encrypted message

---

## **C. Presenting a Credential (“Verifiable Presentation”)**

A presentation allows the holder to share **only the required parts** of the credential.

1. Open the credential
2. Tap **Present**
3. Select fields to reveal
4. Wallet generates:

   * A zero-knowledge / selective disclosure proof
   * Holder’s DID authentication
5. Share the presentation with verifier

This preserves maximum privacy.

---

## **D. Revoking a Credential (Optional)**

1. Open **Issued Credentials**
2. Select credential
3. Tap **Revoke**
4. Confirm DID-signed revocation

Verifiers will see the credential as revoked in future checks.

---

# **Real-World Examples**

### **Example 1 — Digital Degree**

A university issues VCs instead of PDFs.
Employers verify authenticity instantly without contacting the school.

### **Example 2 — Driver License Check**

User presents only “Over 18” instead of full identity details.
Selective disclosure protects privacy.

### **Example 3 — Corporate Compliance**

An employee presents a “Certified AML Officer” credential to a financial institution.
The institution verifies:

* DID of employee
* DID of the issuing company
* Integrity of the credential

### **Example 4 — DAO Reputation**

A DAO issues contribution-based VCs to members.
Tools read VC reputation to grant roles or voting rights.

---

# **Benefits**

* Trustless, verifiable credentials
* Self-sovereign, not platform-controlled
* Portable across apps, companies, and chains
* Supports privacy and selective disclosure
* Compatible with global W3C standards
* Works seamlessly with DID and Document Contracts

---

# **Drawbacks**

* Users must safeguard wallet and credentials
* Revocation requires issuer DID control
* Some platforms still rely on centralized credential formats

---

# **Best Practices**

### For Issuers

* Use stable, persistent DIDs
* Anchor revocation lists onchain
* Avoid including unnecessary personal data
* Use credential types aligned with global schemas (e.g., W3C)

### For Holders

* Make secure encrypted backups of credentials
* Use selective disclosure whenever possible
* Keep DID keys rotated and secure

### For Verifiers

* Always check DID signature and timestamp
* Verify revocation status
* Use VC-compliant parsers for best interoperability
