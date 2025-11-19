# Payment & Agreement Layer

## **Introduction**

The **Payment & Agreement Layer** is the foundation of Florune’s trustless financial ecosystem. It provides **secure, automated, and transparent mechanisms** for managing funds, contracts, and conditional agreements between parties — all without relying on intermediaries or custodians.

This layer is designed for a wide spectrum of users:

* **Individuals:** Freelancers, gig workers, and peer-to-peer (P2P) payments
* **Businesses & Enterprises:** Small B2B contracts, milestone-driven projects, and enterprise workflows
* **Developers & Integrators:** Automated payment flows and programmatic contract interactions

Every service in this layer leverages **on-chain smart contracts** to provide **trust, security, and automation**, ensuring that agreements execute exactly as defined and that funds are handled safely.

---

## **Layer Overview**

| Layer Name                | Description                                                              | Services                 |
| ------------------------- | ------------------------------------------------------------------------ | ------------------------ |
| Payment & Agreement Layer | Provides secure, automated escrow and contract-based payment mechanisms. | Escrow, Pledge Contracts |

**Key Objectives of the Layer:**

* Enable **trustless, high-value transactions**
* Protect participants with **automatic enforcement**
* Facilitate **milestone-based and phased payments**
* Reduce reliance on intermediaries or centralized authorities

---

## **Services in the Payment & Agreement Layer**

### **1. Escrow**

**Purpose:**
Escrow provides a **trustless, non-custodial payment mechanism** that securely holds funds until agreed-upon conditions are fulfilled. It is ideal for **high-value transactions**, protecting both buyers and sellers while remaining cost-effective compared to Pledge Contracts.

**Key Features:**

* **Flat deposit fee + 1% withdrawal fee**
* Supports **revocable, time-bound, and rollback agreements**
* **On-chain enforcement** ensures transparency and trust
* **High-value capable**, yet simpler and cheaper than Pledge Contracts
* Managed fully via the **Florune Wallet**

**How It Works:**

1. Sender deposits funds into the Escrow smart contract
2. Funds remain locked until the recipient fulfills the agreement
3. Upon completion, funds are automatically released
4. Conditional rollback or cancellation is supported if obligations are unmet

**Use Cases:**

* Freelance / Gig Work: Client deposits → Freelancer delivers → Funds released
* P2P Item Purchases: Buyer deposits → Seller delivers → Buyer verifies → Funds released
* High-Value B2B Transactions: Secure large payments for prototypes, consulting sessions, or licensing deals
* Deposits, Reservations, and Rentals: Automatically refundable if conditions fail
* Digital Content Delivery: Works seamlessly with **Asset Paywall** for monetized content

**Benefits:**

* **Trustless transactions** without intermediaries
* **Cost-effective** for high-value and regular payments
* **Automated enforcement** via smart contracts
* **Secure, transparent lifecycle**
* **Compatible with Pledge Contracts** for more complex workflows

---

### **2. Pledge Contracts**

**Purpose:**
Pledge Contracts extend escrow functionality to **larger, milestone-based, or complex agreements**, making them ideal for **enterprise-grade projects** and **high-value contracts** requiring multiple stages, verification, or document linkage.

**Key Features:**

* **Milestones & partial payouts** — release funds based on verified project stages
* **Revocable & rollback options** for flexible risk management
* **Document & signature binding** — ensures legal enforceability and auditability
* **One-time creation fee** with **0% ongoing fees**
* Example: **33 Rune** per contract deployment
* Fully integrates with **Verifiable Documents**, syncing payout conditions with document status

**How It Works:**

1. Contract creator defines milestones and corresponding payouts
2. Funds are deposited into the Pledge Contract smart contract
3. As each milestone is verified, funds are released automatically
4. All contract terms, payments, and document interactions are **cryptographically secured and auditable**

**Use Cases:**

* Enterprise Software Development: Payment released as each development milestone is completed
* Licensing or Procurement: Funds unlocked when verified deliverables or documentation are submitted
* Complex Freelance Projects: Large creative or consulting projects with multi-phase deliverables
* Document-Linked Agreements: Synchronize payments with signed verifiable documents to ensure accountability
* Cross-Border B2B Deals: Ensures high-value payments execute reliably across jurisdictions

**Benefits:**

* **Flexible agreements**: Milestone-based, partial payouts, rollback support
* **Revocable & secure**: Parties retain control, fully enforced on-chain
* **Document binding**: Legal and audit-ready, linked to verifiable documents
* **Cost-efficient**: One-time creation fee for long-term security
* **Ideal for heavy payments** and complex workflows

---

## **Layer Benefits Summary**

| Service          | Key Advantages                                                                      |
| ---------------- | ----------------------------------------------------------------------------------- |
| Escrow           | Trustless, high-value capable, automated P2P payments, low fees                     |
| Pledge Contracts | Milestone-based, revocable, document-linked agreements, suitable for large payments |

**Overall Layer Benefits:**

1. **Trustless Payments:** Reduces risk across all transaction sizes
2. **Automation:** Smart contracts manage enforcement automatically
3. **Flexibility:** Supports simple to complex agreements, individual to enterprise
4. **Security & Transparency:** Immutable, auditable on-chain contracts
5. **Cost Efficiency:** Cheaper and faster than traditional intermediaries

---

The **Payment & Agreement Layer** is the backbone of Florune’s ecosystem. By combining **Escrow for high-value payments** and **Pledge Contracts for flexible, milestone-driven agreements**, it provides a **secure, automated, and transparent financial infrastructure** that empowers individuals, businesses, and enterprises to transact confidently across borders and industries.
