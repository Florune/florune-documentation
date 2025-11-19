# Florune – Payment & Agreement Layer

## Introduction

The **Payment & Agreement Layer** is the foundation of trustless financial interactions within the Florune ecosystem. It provides **secure, automated, and transparent mechanisms** for managing funds and agreements between parties, without the need for intermediaries.

This layer is designed for:

* **Individuals**: Freelancers, gig workers, and P2P payments
* **Businesses & Enterprises**: Small B2B contracts, milestone-based projects
* **Developers & Integrators**: Automated payment workflows via smart contracts

All services in this layer leverage **on-chain smart contracts** to ensure **trust, automation, and security**.

---

## Layer Overview

| Layer Name                | Description                                                              | Services                 |
| ------------------------- | ------------------------------------------------------------------------ | ------------------------ |
| Payment & Agreement Layer | Provides secure, automated escrow and contract-based payment mechanisms. | Escrow, Pledge Contracts |

**Key Objectives of the Layer:**

* Facilitate **trustless transactions**
* Protect all parties through **automated agreements**
* Support **milestone-based and phased payments**
* Reduce dependency on intermediaries and central authorities

---

## Services in Payment & Agreement Layer

### 1. Escrow

**Purpose:**
Protect both parties in low- to mid-value peer-to-peer transactions by securely holding funds until agreed conditions are met.

**Key Features:**

* **Flat deposit fee + 1% withdrawal fee**
* Supports **time-bound, revocable, and rollback agreements**
* **On-chain enforcement** ensures transparency and trust
* Ideal for **freelancers, gig payments, and small B2B contracts**

**How It Works:**

1. Sender deposits funds into the Escrow smart contract.
2. Funds remain locked until the recipient fulfills the agreement.
3. On completion, funds are released automatically.
4. Optionally, agreements can be **revoked or rolled back** if conditions are unmet.

**Use Case Example:**

* A freelancer completes a 10-hour project. The client deposits funds into escrow, and payment is automatically released after project verification.

**Benefits:**

* **Trustless transactions**: No reliance on intermediaries
* **Low fees**: Cost-effective for small transactions
* **Automated enforcement**: Smart contracts handle all payment logic
* **Security**: Funds are cryptographically secured on-chain

---

### 2. Pledge Contracts

**Purpose:**
Provide **advanced escrow functionality** for larger or milestone-based agreements.

**Key Features:**

* Supports **milestones & partial payouts**
* **Revocable** and **rollback** options for flexibility
* **Document & signature binding** for legal enforceability
* **One-time creation fee** (0% ongoing fees)
* Example deployment: **33 Rune per contract**

**How It Works:**

1. Contract creator defines **milestones** and associated payouts.
2. Funds are deposited into the Pledge Contract smart contract.
3. As each milestone is completed and verified, funds are released.
4. All contract terms are **cryptographically secured and verifiable**.

**Use Case Example:**

* A software development company hires an agency for a 3-month project. Payments are released as milestones are completed, ensuring accountability.

**Benefits:**

* **Flexible agreements**: Milestone-based payouts reduce risk for both parties
* **Revocable & secure**: Parties retain control, with on-chain enforcement
* **Document binding**: Legal and auditability support
* **Cost-effective**: One-time deployment fee with no ongoing costs

---

## Layer Benefits Summary

| Service          | Key Advantages                                                |
| ---------------- | ------------------------------------------------------------- |
| Escrow           | Trustless, low-fee, automated P2P payments                    |
| Pledge Contracts | Milestone-based, revocable, document-bound agreements, secure |

**Overall Layer Benefits:**

1. **Trustless Payments** – Reduces risk in financial transactions.
2. **Automation** – Smart contracts handle enforcement automatically.
3. **Flexibility** – Supports simple and complex agreements (from P2P to enterprise).
4. **Security & Transparency** – On-chain contracts provide immutable proof of actions.
5. **Cost Efficiency** – Minimal fees compared to traditional intermediaries.

---

## Conclusion

The **Payment & Agreement Layer** is the backbone of Florune’s ecosystem, providing **secure, automated, and transparent financial services**. By leveraging smart contracts, this layer ensures **trust, flexibility, and efficiency**, enabling freelancers, businesses, and enterprises to transact safely and confidently.
