# Pledge Contract

*A hybrid physical–digital contract framework with flexible milestone enforcement, verifiable documents, and on-chain guarantees.*

---

## **Overview**

A **Pledge Contract** is a decentralized agreement between two parties where all obligations, milestones, and deliverables are **digitally anchored**. It serves as a **self-executed contract** where every participant signs with their private key, ensuring integrity, accountability, and traceability without relying on centralized intermediaries.

A Pledge Contract may optionally include:

* **Milestones** multiple Pledge Contracts can be linked to one document *can use diffrent coins for payments, *using different parties for each payments from parties and controllers at Verifiable Document
* **Verifiable Documents** for document verifiacation and authentication and document binding
* **Auto-updating statuses** triggered by contract actions

---

## **Context & Problem**

### **The Problem**

Traditional contracts lack:

* Automatic enforcement
* Transparency across parties
* Immutable records of milestone progress
* Easy verification of terms or deliverables
* Integrated payment guarantees

They often require **third-party mediators**, which increases cost, reduces trust, and slows execution.

### **The Solution**

SafePulse’s Pledge Contract provides:

* **Immutable, on-chain agreements** verified by participants' cryptographic signatures
* **Linked deliverables**, such as Verifiable Documents
* **Flexible Milestone-based workflows** for structured work delivery and progressive payments
* **Automated status updates** to reduce manual coordination

This creates a **trustless contracting system** suitable for digital commerce, services, creative work, licensing, and more.

---

## **Key Features**

### **1. Multi-party Signing**

Each participant signs the contract with their private key, ensuring authenticity and non-repudiation.

### **2. Document Integration**

Attach **Verifiable Documents** as deliverables, guidelines, licenses, terms, or specifications.

### **3. Milestone Enforcement**

Be used as Flexible milestones for progressive payments.

### **4. Multiple Payments on One Document**

One Verifiable Document can be used for multiple Pledge Contracts, with diffrent parties and multiple payment process.

### **5. Full Status Lifecycle**

Automatically transitions through states such as:

* Pending
* Active
* Executed
* Disputed
* Completed
* Canceled

### **6. Wallet-First Operation**

Everything is controlled in the SafePulse Wallet — no external software required.

---

## **Step-by-Step Tutorial**

### Prerequisites

* SafePulse Wallet installed
* Active subscription or usage credits
* Issuer/Creator DID: an key DID (did:key) or an ERC-1056 DID with issuer key as its Delegate  
* Network tokens for contract deployment
* A Verifiable Document for document-bound payments

---

### **A. Creating a Pledge Contract**

1. Tap **Pledge Contract**
2. Fill in contract details:

   * Seller/Contarctor/Issuer DID
   * Contractee/buyer address
   * Network and Token
   * Enter Verifiable Document Contract DID (optional)
3. Tap **Create** and Approve transaction
4. After minting, go to **History**
5. Locate the document history record
6. From More, select **Initialize and Setup** and confirm initialization transaction

Notes: 

* oposite the Escrow, Pledge Contract should be created by seller and its DID should be shared with parties, whole process will be done on pledge contracts.
* Important Note: before initialization contract controller stays empty so INITIALIZE CONTRACT QUICKLY AFTER DEPLOYMENT

---

### **B. Share Contarct DID with parties**

1. Go to History
2. Find Issue record related to your contract
3. On More tap on "Show Transaction Info"
4. Copy DID

---

## **Pledge Contract Status Guide**

| Status        | Meaning                                                             |
| ------------- | ------------------------------------------------------------------- |
| **Pending**   | Contract created but not yet Accepted by Seller                     |
| **Active**    | Seller Accepted agreement                                           |
| **Executed**  | Terms fulfilled                                                     |
| **Completed** | All deliverables + linked workflows finished, Buyer approve fulfillment|
| **Disputed**  | A party flagged an issue requiring resolution, funds won't release|
| **Canceled**  | Contract voided before activation or execution, seller rejected the agreement|

---

### Pledge Contract Status Guide

#### 1. `pending`

**Meaning:** Service is initialized but not started yet.

* **Entered by:** Default state.
* **Who can act:** Seller (issuer).
* **Transitions to:**

  * `active` → seller starts service
  * `canceled` → seller cancels before starting
* **Permissions:**

  * ✅ Rollback → buyer
  * ✅ Cancel → seller
  * 🚫 Withdraw

---

#### 2. `active`

**Meaning:** Service has started and is ongoing.

* **Entered by:** Seller starts service.
* **Who can act:** Seller (execute), Buyer (dispute).
* **Transitions to:**

  * `executed` → seller executes service
  * `disputed` → buyer disputes service
* **Permissions:**

  * 🚫 Rollback (unless expired)
  * 🚫 Cancel
  * 🚫 Withdraw

---

#### 3. `executed`

**Meaning:** Seller marked service as delivered.

* **Entered by:** Seller executes service.
* **Who can act:**

  * Buyer → confirm (`completed`)
  * Buyer → dispute (`disputed`)
  * Seller → withdraw after 5 days post-expiration (if no dispute)
* **Transitions to:**

  * `completed` → buyer confirms delivery
  * `disputed` → buyer disputes service
* **Permissions:**

  * 🚫 Rollback
  * ✅ Withdraw (after 5 days if no dispute)
  * 🚫 Cancel

---

#### 4. `disputed`

**Meaning:** Buyer raised a dispute.

* **Entered by:** Buyer disputes service.
* **Who can act:**

  * Buyer → complete it
  * Seller → cancel it
* **Transitions to:**

  * `completed` → by buyer
  * `canceled` → by seller
* **Permissions:**

  * 🚫 Rollback
  * 🚫 Withdraw
  * 🚫 Cancel

---

#### 5. `completed`

**Meaning:** Buyer confirmed delivery and acceptance.

* **Entered by:** Buyer completes service.
* **Who can act:** Seller → withdraw.
* **Permissions:**

  * ✅ Withdraw (seller)
  * 🚫 Rollback
  * 🚫 Dispute
  * 🚫 Cancel

---

#### 6. `canceled`

**Meaning:** Seller canceled service before completion.

* **Entered by:** Seller cancels.
* **Who can act:** Buyer → rollback.
* **Permissions:**

  * ✅ Rollback (buyer)
  * 🚫 Withdraw
  * 🚫 Execute/Complete

---

#### 📌 Notes

* Dispute only possible from `active` or `executed`.
* Rollback allowed only when:

  * State is not `active`, or expired
  * State is not `executed`, `completed`, or `disputed`
* Withdraw allowed only when:

  * State is `completed`, or
  * State is `executed` and 5 days passed with no dispute
* No transitions allowed from `completed`, `disputed`, or `canceled` unless manual.
* 🔐 Funds are locked until customer approves completion.

---

#### 📎 Linked Document Rules

If linked to a **Verifiable Document**:

* For **`executed`** → seller must sign on-chain in the Document Contract.
* For **`completed`** → buyer must sign on-chain in the Document Contract.
* For **`canceled`** → Document Contract must be in **suspended** or **revoked** status.

---

## **Real-World Use Cases**

### **1. Freelance or Service Agreements**

* Designer and client define milestones
* Verifiable Document details requirements
* Client deposits funds in escrow
* Each milestone is approved before payment is released

### **2. Licensing & Intellectual Property**

* A creator issues rights via a Verifiable Document
* Licensee accepts terms through contract signing
* Usage rights become provable on-chain

### **3. B2B Supplier Agreements**

* Milestones tied to shipment or delivery phases
* Locks funds and payments till conditions met
* Each step verified for transparency

---

## **Benefits & Drawbacks**

### **Benefits**

* Proven authenticity through cryptographic signatures
* Protects both parties via escrow-secured terms
* Transparent progress tracking
* Immutable record of obligations and deliverables
* Zero reliance on centralized intermediaries

### **Drawbacks**

* Requires users to understand decentralized storage
* On-chain actions incur gas fees
* All parties must use SafePulse Wallet for consistency

---

## **Related Services**

* **Verifiable Documents** — attach deliverables, terms, proofs, secure payment workflows linked to contract milestones,timestamp documents referenced by contract

---

## **Tips & Best Practices**

* Always attach a Verifiable Document describing scope and expectations
* Break work into **seperated milestones contracts with required tokens** to reduce disputes
* Use escrow for high-value or high-risk agreements
* Keep communication in-app to maintain transparency
