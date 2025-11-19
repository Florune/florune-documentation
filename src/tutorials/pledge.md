# Pledge Contract

*A hybrid physical–digital contract framework with milestone enforcement, verifiable documents, and on-chain guarantees.*

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
* **Milestone-based workflows** for structured work delivery
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

Create phases (milestones) that are completed sequentially or individually with explicit confirmation from involved parties.

### **4. Optional Escrow Binding**

Secure payments by linking to **Escrow Deposits**, ensuring funds are locked until milestones are achieved.

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
* A Verifiable Document (optional but recommended)

---

### **A. Creating a Basic Pledge Contract**

1. Open **Create** → tap **Pledge Contract**
2. Fill in contract details:

   * Title
   * Description
   * Parties involved
3. Select **network**
4. Tap **Create**
5. Approve transaction
6. Contract is now deployed and appears under **History**

---

### **B. Linking Verifiable Documents (Optional)**

1. Go to the contract record
2. Tap **More** → **Link Document**
3. Select one or multiple Verifiable Documents
4. Wait for confirmation
5. Linked documents now appear in contract details

---

### **C. Adding Milestones (Optional)**

1. Open the contract
2. Tap **Add Milestone**
3. Enter milestone name + details
4. Save
5. Repeat for additional steps

---

### **D. Initializing the Contract**

1. Inside the contract, tap **Initialize**
2. All participants must sign
3. Once everyone signs → **Status becomes Active**

---

### **E. Completing Milestones**

1. Select a milestone
2. Tap **Mark Complete**
3. Other party may need to confirm
4. System updates contract status

---

### **F. Finalizing the Contract**

Once all milestones are complete:

* Tap **Execute Contract**
* If linked to Escrow, funds will automatically release
* Status becomes **Executed** or **Completed** depending on workflow

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
