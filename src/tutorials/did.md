# DID

*A self-sovereign, portable, Ethereum-based identity standard for secure, user-controlled interaction across Florune services.*

---

## **Overview**

Florune’s **Decentralized Identity (DID)** system is built on the **ERC-1056** identity standard, allowing users to create a **self-sovereign digital identity** that is:

* **User-controlled** (no central authority)
* **Portable** across services and networks
* **Privacy-preserving**, with no forced disclosure
* **Compatible with Verifiable Credentials and onchain contracts**

A DID is the foundational element powering all advanced workflows in Florune, including:

* Verifiable Credentials
* Document verification
* Pledge Contract authorization
* Escrow interactions
* Asset Paywall access

Your DID enables you to prove *who you are* cryptographically, without giving up personal data, documents, or reliance on centralized identity providers.

---

## **Context & Problem**

### **The Problem**

Most modern digital identity systems suffer from:

* Centralized control (Google, Apple, government IDs)
* Limited portability across platforms
* High privacy exposure
* Risk of surveillance or data misuse
* Fragmented identity silos

Users need a secure identity they can use across agreements, documents, services, and contracts **without depending on third parties**.

### **The Solution**

Florune implements **ERC-1056 Decentralized Identity**, giving users:

* A cryptographic identity bound to their wallet
* A globally resolvable DID Document
* Self-sovereign control of keys
* Maximum privacy with minimum data sharing
* Full integration with the onchain ecosystem

Your DID becomes your trust anchor across all services.

---

## **Key Features**

### **1. Self-Sovereign Control**

You create your identity locally on your device.
No admin, no provider, no central manager.

### **2. Portable & Cross-Platform**

Your DID can be used across multiple networks, dapps, and verification systems.

### **3. Privacy-First**

DIDs do not require linking to names, emails, or personal data.

### **4. Verifiable & Tamper-Proof**

Each DID has an onchain **DID Document** describing:

* Public keys
* Verification methods
* Authentication methods
* Delegates (optional)

### **5. Works With Verifiable Credentials**

Your DID can issue, verify, and receive:

* Certificates
* Licenses
* Compliance proofs
* Identity attestations

### **6. Required for Florune Contracts**

DIDs authorize:

* Pledge Contract interactions
* Signing Verifiable Documents
* Disputes and approvals
* Asset Paywall access rights

---

## **Use Cases**

### **1. Freelance Work & Payments**

A freelancer uses a DID to identify themselves in a Pledge Contract — no email or passport needed.

### **2. Enterprise Compliance**

Companies issue DID-backed credentials to employees, proving compliance or training certifications.

### **3. Education & Certification**

Schools issue DID-bound certificates that can be verified anywhere.

### **4. Secure Document Management**

Documents are signed using the DID’s verification keys.

### **5. Content Distribution**

Asset Paywall access can be tied to a user’s DID, proving rights and preventing unauthorized sharing.

---

## **Step-by-Step Tutorial**

### **A. Creating Your DID**

1. Open the Florune Wallet
2. Navigate to **Identity**
3. Tap **Create DID**
4. The wallet generates:

   * A DID string
   * Verification keys
   * Controller information
5. Confirm creation
6. Your DID is now active and visible under **Identity → Details**

---

### **B. Managing Your DID**

Inside the DID details page, you can:

* View DID Document
* View public keys
* Add/Remove delegates (optional)
* Rotate keys for security
* Export DID metadata

All sensitive operations stay local on your device unless explicitly broadcast onchain.

---

### **C. Using DID With Services**

#### **1. Verifiable Documents**

* DID signs or authorizes document issuance
* DID proves ownership of the document
* DID is part of the certificate metadata

#### **2. Pledge Contracts**

* DID identifies seller or buyer
* DID signs execution/completion steps
* DID is required for disputes and approvals

#### **3. Escrow Deposits**

* DID represents the depositor or recipient

#### **4. Verifiable Credentials**

* DID can receive or verify credentials
* Required for presentations and selective disclosure

---

Florune applies the ERC-1056 standard, ensuring maximum interoperability.

---

## **Real-World Examples**

### **Example 1 — Talent Marketplace**

A freelancer uses their DID to authenticate in a contract without revealing personal identity. The buyer verifies the DID and contract execution onchain.

### **Example 2 — Employee ID System**

A company issues VCs tied to employee DIDs.
Employees prove qualifications without exposing private data.

### **Example 3 — Anonymous Research Publication**

A researcher anchors findings under a pseudonymous DID, later proving authorship without revealing identity at submission time.

---

## **Benefits**

* Fully decentralized identity
* No personal data exposure
* Secure and key-controlled
* Interoperable with global standards
* Works seamlessly across Florune services
* Ideal for anonymous or pseudonymous workflows

---

## **Drawbacks**

* User is responsible for securing private keys
* Identity recovery requires proper key backups
* Cross-network DID document updates require gas fees

---

## **Best Practices**

* Enable key rotation for long-term identity protection
* Back up your wallet securely
* Use separate DIDs for public and private activities
* Combine DID with Verifiable Credentials for strong attestations
* Always verify DID controllers on incoming requests
