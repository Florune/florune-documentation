# Document Registry

*A lightweight, low-cost, onchain proof-of-existence system for timestamping documents, research, IP, and digital work.*

---

## **Overview**

The Document Registry provides a **fast, cost-efficient and immutable method** to prove that a document existed at a specific point in time. Instead of storing the full file onchain, SafePulse only records the **hash**, making the process cost-efficient while maintaining strong cryptographic guarantees.

This service is ideal for protecting **intellectual property**, **research**, **legal documents**, **design drafts**, **code**, and any other material where authorship and existence must be provably timestamped.

A trustless, permanent anchor for any file that need to be verified.

---

## **Context & Problem**

### **The Problem**

Traditional document notarization methods suffer from:

* High costs for official notary services
* Slow processing
* Geographic limitations
* Risk of altered or missing records
* Dependence on centralized institutions

Organizations and creators need a way to **prove authorship**, **establish priority**, and **timestamp content** without revealing the full document or relying on third parties.

### **The Solution**

SafePulse Document Registry creates an **immutable onchain proof** that a specific document, identified by its hash, existed at a given moment. This proof is:

* Cryptographically verifiable
* Public or private document identifier
* Permanent and censorship-resistant
* Quick and inexpensive

This allows creators, researchers, and businesses to validate authorship or existence whenever needed.

---

## **Use Cases**

### **1. Intellectual Property Protection**

* Artists timestamp digital artwork
* Writers record novel drafts
* Developers anchor new code or smart contracts
* Designers secure product sketches

### **2. Research & Innovation**

* Recording first publication dates
* Protecting proprietary formulas
* Proving original authorship of research papers
* Documenting experiments or iterations

### **3. Legal and Compliance**

* Timestamping agreements before signature
* Anchoring evidence documents
* Recording immutable audit logs

### **4. Enterprise Workflows**

* Documenting internal policies
* Securing confidential revisions off-chain
* Establishing chain-of-custody events

---

## **Key Features**

### **1. Fast and Low-Cost**

Designed as a lightweight alternative to Verifiable Documents.

### **2. Non-custodial Data management**

File stays off-chain by user/issuer, we verify.

### **3. Immutable and Permanent**

Records cannot be deleted or modified, ensuring trustworthiness.

### **4. Flexible Storage Options**

Users can store files:

* Locally
* IPFS
* Arweave
* Any private or centralized host

### **5. No Initialization Required**

Unlike Verifiable Documents, the record exists immediately after registration.

---

## **Step-by-Step Tutorial**

### **Prerequisites**

* SafePulse Wallet installed
* Native token balance for registration fees
* Issuer/Creator DID: an key DID (did:key) or an ERC-1056 DID with issuer key as its Delegate  
* File prepared and hashed automatically by the app

---

### **A. Registering a Document**

1. Upload your file to one of:

   * IPFS
   * Arweave
   * Centralized host (direct download link)
2. Tap **Document Registry** 
3. Copy the file link/IPFS-CID/Arweave Transaction Id
4. Fill in the creation form:

   * Paste the refrence identifier (file link/IPFS-CID/Arweave Transaction Id)
   * Choose blockchain network
5. Tap **Register** (top of screen)
6. Confirm the on-chain transaction
7. After minting, go to **History**
8. Locate the document history record
9. Share the **Verifiable Document DID** with relevant parties

---

## **Real-World Examples**

### **Example 1: Protecting Creative Work**

A designer registers a new product sketch. Months later, if questioned about authorship, the onchain timestamp validates they created it first.

### **Example 2: Academic Research Timestamp**

A scientist anchors early drafts of a paper before journal submission, proving that research was conducted earlier than similar publications.

### **Example 3: Internal Company Evidence**

A compliance officer anchors a log of policy updates to prove the timeline of organizational changes.

---

## **Benefits**

* Extremely low-cost proof registration
* Works instantly with minimal user steps
* Does not expose or upload the actual file
* Immutable and verifiable forever
* Provides strong authorship protection
* No dependency on centralized notaries

---

## **Drawbacks**

* Does **not** support revocation
* Does **not** support multiple controller
* Cannot attach signatures
* Cannot filter/limit verifiers

For these advanced features, **Verifiable Documents** are recommended.

---

## **Best Practices**

* Save the original file securely — the hash depends on exact content
* Use decentralized storage (IPFS/Arweave) for long-term preservation
* Register drafts and versions frequently if working iteratively
* Combine registry entries with Pledge Contracts for deliverable verification
* For legal agreements, convert to Verifiable Documents if signatures are needed
