# Verifiable Document

## **Overview**

**Verifiable Documents** allow users to create **tamper-proof, wallet-first documents** that can be stored locally or on decentralized storage networks, such as **IPFS** or **Arweave**. Each document can be **anchored on-chain**, providing an immutable proof of authenticity. Documents can also be **linked to smart contracts**, enabling automated enforcement in escrow or pledge workflows.

> All operations are executed via the Florune Wallet, ensuring **self-sovereign, local execution**.

---

## **Purpose / Context**

**Problem:**
Organizations and individuals often require tamper-proof documents for **legal, compliance, or intellectual property purposes**. Centralized solutions carry the risk of modification, loss, or lack of verifiability.

**Solution:**
Florune’s Verifiable Document service allows users to:

* Anchor documents **on-chain** for immutability
* **Link documents to smart contracts** (Pledge Contracts or Escrow) for enforceable workflows
* Maintain full **self-sovereign control** over document storage and access

This ensures documents are trustworthy, verifiable, and usable in automated payment or contract workflows.

---

## **Features**

* **Decentralized storage options:** IPFS, Arweave, or centralized host with direct download
* **Revocable documents:** Documents can be suspended or revoked if needed
* **Linked to contracts:** Automatically enforceable within Pledge or Escrow workflows
* **Wallet-first signing:** Cryptographically signed via your private key
* **On-chain anchoring:** Ensures tamper-proof verification of authenticity

---

## **Step-by-Step Tutorial**

### **Prerequisites**

* Florune Wallet installed
* Active EOA (Externally Owned Account) with subscription plan or usage credit
* Network tokens (e.g., Rune) to pay deployment fees

### **Steps**

1. Navigate to **Create** → tap **Create**
2. Upload your file to one of:

   * IPFS
   * Arweave
   * Centralized host (direct download link)
3. Copy the file link
4. Fill in the creation form:

   * Paste file link
   * Choose blockchain network
5. Tap **Create** (top of screen)
6. Confirm the on-chain transaction
7. After minting, go to **History**
8. Locate the document record
9. From **More**, select **Initialize and Setup**
10. Share the **Verifiable Document DID** with relevant parties

---

## **Use Cases / Examples**

* **Education Certificates:** Universities issue tamper-proof diplomas verifiable by employers
* **Contract Enforcement:** Attach signed documents to a Pledge Contract to enforce milestone payments
* **Intellectual Property:** Timestamp creative works or research papers to prove authorship
* **Legal Agreements:** Ensure critical agreements are immutable and verifiable by all parties

---

## **Benefits & Drawbacks**

**Benefits:**

* Tamper-proof and auditable
* Integrates with Florune contracts for automated enforcement
* Full control over document storage and access

**Drawbacks:**

* Requires management of decentralized storage
* Deployment may incur Rune token costs

---

## **Related Services / Cross-links**

* **Pledge Contract:** For milestone-based contracts linked to documents
* **Escrow:** To secure payments tied to verified documents
* **Document Registry:** For lightweight on-chain proof without full content deployment

---

## **Notes & Tips**

* Confirm your document is uploaded correctly before creating a Verifiable Document
* Keep a **local backup** in addition to decentralized storage
* Always link documents to contracts where verification is required for automated enforcement
