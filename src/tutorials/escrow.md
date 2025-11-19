# Escrow

*A trustless, non-custodial payment safeguard for peer-to-peer transactions and service agreements.*

---

## **Overview**

Florune Escrow is a **trust-minimized payment mechanism** that holds funds securely until agreed-upon conditions are met. Built entirely onchain, it protects **buyers, sellers, clients, freelancers, and service providers** during low- to mid-value transactions.

With an easy setup, transparent fee structure, and cryptographic verification, Florune’s Escrow reduces fraud risk, removes intermediaries, and creates a neutral, automated environment for secure payments.

---

## **Context & Problem**

### **The Problem**

Digital transactions between two parties (e.g., freelancer ↔ client, buyer ↔ seller) are prone to:

* Payment fraud
* Delivery disputes
* Chargebacks
* Legally unenforceable agreements
* Lack of transparency during the transaction lifecycle

Centralized escrow providers exist but introduce:

* High fees
* Custodial risk
* Limited verification
* Slow dispute resolution
* Country restrictions

### **The Solution**

Florune Escrow replaces centralized processors with **onchain smart contracts**, giving users:

* Non-custodial fund holding
* Cryptographically secured signatures
* Immutable payment flows
* Transparent status updates
* Revocable, time-bound, and rollback options

This creates a fair, automated payment channel ideal for digital work and simple agreements.

---

## **Use Cases**

### **1. Freelance / Gig Work**

* Client deposits funds in escrow
* Freelancer completes the work
* Client releases payment upon approval

### **2. P2P Item Purchases**

* Buyer locks payment in escrow
* Seller delivers the product
* Buyer verifies and releases funds

### **3. Deposits, Reservations, and Rentals**

* Secure holding of booking deposits
* Automatic rollback if conditions aren’t met

### **4. Small B2B Transactions**

* Protects both parties in quick service delivery
* Ideal for prototype delivery, consulting sessions, one-off jobs

### **5. Content & Digital Deliverables**

* Works seamlessly with the **Asset Paywall**
* Protects creators and purchasers in content delivery workflows

---

## **Key Features**

### **1. Trustless, Non-Custodial Payment Holding**

Funds are held onchain — not by Florune, not by a third party.

### **2. Revocable, Time-Bound, Rollback Support**

Flexible payment protection with conditional rules.

### **3. Simple Fee Structure**

* **Flat deposit fee**
* **1% withdrawal fee**

No hidden costs or subscriptions required.

### **4. Status Transparency**

Each escrow moves through a clear lifecycle:

* **Open**
* **Freeze**
* **Release**
* **Cancel**

### **5. Wallet-First Flow**

The entire process is managed in the Florune Wallet — from creation to withdrawal.

---

## **Escrow Lifecycle (Status Guide)**

| Status      | Meaning                                            |
| ----------- | -------------------------------------------------- |
| **Open**    | Escrow created; waiting for deposit or approval    |
| **Freeze**  | Funds locked and held securely                     |
| **Release** | Funds released to recipient upon agreed conditions |
| **Cancel**  | Funds returned to sender                           |

---

## **Step-by-Step Tutorial**

### **Prerequisites**

* Florune Wallet installed
* Native network tokens for gas fees
* Any payment token approved for use

---

### **A. Creating an Escrow Deposit**

1. Open **Create** → select **Escrow Deposit**
2. Fill in the deposit details:

   * Recipient wallet address
   * Amount
   * Optional memo or notes
3. Select network
4. Tap **Create**
5. A record appears under **History**

---

### **B. Approving Tokens for Escrow Use**

Before depositing, you must allow the smart contract to handle your tokens.

1. Open the escrow record
2. Tap **Approve Token**
3. Confirm
4. Wait for confirmation

Once approved, the escrow is ready for deposit.

---

### **C. Depositing Funds**

1. Open the escrow record
2. Tap **Deposit**
3. Enter the amount
4. Confirm transaction
5. Status becomes **Freeze** when funds are secured

---

### **D. Releasing or Canceling the Escrow**

#### **Release**

Used when:

* The work was delivered
* The item was received
* The agreement is fulfilled

1. Open the escrow record
2. Tap **Release**
3. Confirm the action

Funds go to the recipient.

#### **Cancel**

Used when:

* Agreement fails
* Time expires
* Parties agree to cancel

1. Open the escrow
2. Tap **Cancel**
3. Confirm

Funds return to the sender.

---

## **Real-World Examples**

### **Example 1: Buyer ↔ Seller Transaction**

Buyer deposits payment → Seller ships item → Buyer confirms → Payment released.

### **Example 2: Freelancer ↔ Client Work**

Client deposits → Freelancer delivers design files → Client approves → Funds released.

### **Example 3: Refundable Deposit**

User makes a booking deposit → Service is unavailable → Deposit canceled and refunded automatically.

---

## **Benefits**

* **Protects both parties** with neutral fund holding
* **Reduces fraud** in digital transactions
* **Secure and transparent** lifecycle
* **Low-cost payment protection**
* **Automated enforcement** through smart contracts
* **Compatible with Pledge Contracts and Paywalls**

---

## **Drawbacks**

* Requires basic understanding of gas fees
* Both parties should use blockchain wallets
* Status resolution requires user interaction (no central arbiter)

---

## **Best Practices**

* Always keep communication in writing (or in Verifiable Documents)
* For larger agreements, pair Escrow with a **Pledge Contract**
* Use time-bound or revocable conditions if risk is involved
* Confirm wallet addresses carefully before depositing
