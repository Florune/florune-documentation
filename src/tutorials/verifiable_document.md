# Verifiable Document

## Overview

**Verifiable Documents** allow users to create **tamper-proof, wallet-first documents** that can be stored locally or on decentralized storage networks, such as **IPFS** or **Arweave**. Each document can be **anchored on-chain**, providing an immutable proof of authenticity. Documents can also be **linked to smart contracts**, enabling automated enforcement in escrow or pledge workflows.

> All operations are executed via the Florune Wallet, ensuring **self-sovereign, local execution**.

---

## Purpose / Context

**Problem:** Organizations and individuals need tamper-proof documents for legal, compliance, or intellectual property purposes. Centralized solutions risk modification or loss.

**Solution:** Florune’s Verifiable Document service allows users to:

* Anchor documents on-chain for immutability
* Share selectively while preserving privacy
* Link documents to Pledge Contracts or Escrow for enforceable workflows

---

## Features

* **Decentralized storage options:** IPFS, Arweave, or centralized host with direct download
* **Revocable documents**: Can be suspended or revoked if needed
* **Linked to contracts**: Automatically enforceable in pledge or escrow workflows
* **Wallet-first signing**: Cryptographically signed via your private key
* **Selective disclosure**: Share only the information necessary

---

## Step-by-Step Tutorial

### Prerequisites

* Florune Wallet installed
* Active EOA (Externally Owned Account) with subscription plan or usage credit
* Network tokens (e.g., Rune) to pay deployment fees

### Steps

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

## Use Cases / Examples

* **Education Certificates:** Universities issue tamper-proof diplomas verifiable by employers
* **Contract Enforcement:** Attach signed documents to a Pledge Contract to enforce milestone payments
* **Intellectual Property:** Timestamp creative works or research papers to prove authorship

---

## Benefits & Drawbacks

**Benefits:**

* Tamper-proof and auditable
* Privacy-preserving via selective disclosure
* Integrates with Florune contracts for automated enforcement

**Drawbacks:**

* Requires user to manage decentralized storage
* Deployment may incur Rune token costs

---

## Related Services / Cross-links

* **Pledge Contract:** For milestone-based contracts linked to documents
* **Escrow:** To secure payments tied to verified documents
* **Document Registry:** For lightweight on-chain proof without full content deployment

---

## Notes & Tips

* Always confirm that your document is correctly uploaded before creating a Verifiable Document
* Keep a local copy in addition to decentralized storage for backup
* Use selective disclosure for sensitive personal or financial information

---
