# Pledge Contract

*A hybrid physical–digital contract framework with flexible milestone enforcement, verifiable documents, and on-chain guarantees.*

---

## **Overview**

A **Pledge Contract** is a decentralized agreement between two or more parties where all obligations, milestones, and deliverables are **digitally anchored** and optionally backed by **escrowed funds**. It serves as a **wallet-first, self-executed contract** where every participant signs with their private key, ensuring integrity, accountability, and traceability without relying on centralized intermediaries.

A Pledge Contract may optionally include:

* **Milestones** representing discrete phases of work
* **Verifiable Documents** that describe deliverables or legal terms
* **Escrow deposits** to guarantee payments
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

Florune’s Pledge Contract provides:

* **Immutable, on-chain agreements** verified by participants' cryptographic signatures
* **Linked deliverables**, such as Verifiable Documents
* **Flexible Milestone-based workflows** for structured work delivery and progressive payments
* **Optional escrowed funds** to secure both sides
* **Automated status updates** to reduce manual coordination

This creates a **trust-minimized contracting system** suitable for digital commerce, services, creative work, licensing, and more.

---

## **Key Features**

### **1. Multi-party Signing**

Each participant signs the contract with their private key, ensuring authenticity and non-repudiation.

### **2. Document Integration**

Attach **Verifiable Documents** as deliverables, guidelines, licenses, terms, or specifications.

### **3. Milestone Enforcement**

Flexible milestones for progressive payments.

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

Everything is controlled in the Florune Wallet — no external software required.

---

## **Step-by-Step Tutorial**

### Prerequisites

* Florune Wallet installed
* Active subscription or usage credits
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
3. Tap **Create**
4. Choose key
4. Approve transaction
5. Contract is now deployed and appears under **History**

Note: oposite the Escrow, Pledge Contract should be created by seller and its DID should be shared with parties, whole process will be done on pledge contracts.

---

### **B. Initializing the Contract**

1. Inside the contract, tap **Initialize**
2. Choose key
3. Approve transaction

Important Note: before initialization contract controller stays empty so INITIALIZE CONTRACT QUICKLY AFTER DEPLOYMENT

---

### **C. Share Contarct DID with parties**

1. Go to History
2. Find Issue record related to your contract
3. On More tap on "Show Transaction Info"
4. Copy DID

---

## **Pledge Contract Status Guide**

| Status        | Meaning                                                             |
| ------------- | ------------------------------------------------------------------- |
| **Pending**   | Contract created but not yet signed by all parties                  |
| **Active**    | All parties signed—contract is in force                             |
| **Executed**  | Terms fulfilled; contract performed successfully                    |
| **Completed** | All deliverables + linked workflows finished (milestones + escrows) |
| **Disputed**  | A party flagged an issue requiring resolution                       |
| **Canceled**  | Contract voided before activation or execution                      |

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
* Escrow locks funds
* Each step verified for transparency

### **4. Community DAO Workflows**

* DAO hires contributors
* Pledge Contract governs deliverables
* Escrow ensures payment fairness

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
* All parties must use Florune Wallet for consistency

---

## **Related Services**

* **Verifiable Documents** — attach deliverables, terms, proofs
* **Escrow** — secure payment workflows linked to contract milestones
* **Document Registry** — timestamp documents referenced by contract

---

## **Tips & Best Practices**

* Always attach a Verifiable Document describing scope and expectations
* Break work into **clear milestones** to reduce disputes
* Use escrow for high-value or high-risk agreements
* Keep communication in-app to maintain transparency
