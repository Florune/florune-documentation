# Verifiable Document

## **Overview**

**Verifiable Documents** allow users to create **tamper-proof, document verification contract** that let documents be stored locally or on decentralized storage networks, such as **IPFS** or **Arweave**. Each document can be **anchored on-chain**, providing an immutable proof of authenticity. Documents can also be **linked to Pledge Contracts**, enabling automated enforcement.

> All operations are executed via the SafePulse Wallet, ensuring **self-sovereign, local execution**.

---

## **Purpose / Context**

**Problem:**
Organizations and individuals often require tamper-proof documents for **legal, compliance, or intellectual property purposes**. Centralized solutions carry the risk of modification, loss, or lack of verifiability.

**Solution:**
SafePulse’s Verifiable Document service allows users to:

* Anchor documents **on-chain** for immutability
* **Link to Pledge contracts** for enforceable workflows
* Maintain full **self-sovereign control** over document storage and access

This ensures documents are trustworthy, verifiable, and usable in automated payment or contract workflows.

---

## **Features**

* **Decentralized storage options:** IPFS, Arweave, or centralized host with direct download
* **Revocable documents:** Documents can be suspended or revoked if needed
* **Linked to Pledge Contracts:** Automatically enforceable within
* **On-chain anchoring:** Ensures tamper-proof on-chain verification of authenticity

---

## **Step-by-Step Tutorial**

### **Prerequisites**

* SafePulse Wallet installed
* Active EOA (Externally Owned Account) with subscription plan or usage credit
* Issuer/Creator DID: an key DID (did:key) or an ERC-1056 DID with issuer key as its Delegate  
* Network tokens (e.g., Rune) to pay deployment fees

### **Steps**

1. Upload your file to one of:

   * IPFS
   * Arweave
   * Centralized host (direct download link)
2. Tap **Verifiable Document** 
3. Copy the file link/IPFS-CID/Arweave Transaction Id
4. Fill in the creation form:

   * Paste the refrence identifier (file link/IPFS-CID/Arweave Transaction Id)
   * Choose blockchain network
5. Tap **Create** (top of screen)
6. Confirm the on-chain transaction
7. After minting, go to **History**
8. Locate the document history record
9. From More, select **Initialize and Setup** and confirm initialization transaction
10. Share the **Verifiable Document DID** with relevant parties

---

## **Use Cases / Examples**

* **Education Certificates:** Universities issue tamper-proof diplomas verifiable by employers
* **Contract Enforcement:** Attach documents to a Pledge Contract to enforce milestone payments
* **Intellectual Property:** Timestamp creative works or research papers to prove authorship
* **Legal Agreements:** Ensure critical agreements are immutable and verifiable by all parties

---

## **Benefits & Drawbacks**

**Benefits:**

* Tamper-proof and auditable
* Integrates with SafePulse contracts for automated enforcement
* Full control over document storage and access

**Drawbacks:**

* Requires management of decentralized storage
* Deployment may incur Rune token costs (can be created only by elysium members/elysian accounts)

---

## **Related Services / Cross-links**

* **Pledge Contract:** For milestone-based contracts linked to documents/secure payments tied to verified documents

---

## **Notes & Tips**

* Confirm your document is uploaded correctly before creating a Verifiable Document
* Keep a **local backup** in addition to decentralized storage
* Always link documents to contracts where verification is required for automated enforcement
