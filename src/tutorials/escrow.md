# Escrow

*A trustless, non-custodial payment safeguard for peer-to-peer and high-value transactions.*

---

## **Overview**

Florune Escrow is a **trust-minimized, non-custodial onchain payment mechanism** that securely locks funds until both parties meet agreed-upon conditions. Designed for **buyers, sellers, freelancers, enterprises, and service providers**, it is ideal for **high-value transactions** where trust and protection are critical.

With transparent fees, cryptographic enforcement, and guaranteed neutrality, Florune Escrow eliminates fraud risks and intermediaries — delivering a secure, automated environment for global payments of any size.

---

## **Context & Problem**

### **The Problem**

Digital agreements — whether between individuals or businesses — frequently face:

* Payment fraud
* Delivery disputes
* Chargebacks
* Unenforceable promises
* Lack of trusted middlemen
* No protection for large-value deals
* Opaque transaction processes

Centralized escrow alternatives exist, but they introduce:

* High fees (often 2–10%+)
* Custodial risk (fund freezing, loss, shutdowns)
* Slow dispute resolution
* Geographic restrictions
* Risk of platform censorship

For **large-value or cross-border transactions**, these risks become even more severe.

### **The Solution**

Florune Escrow replaces intermediaries with **automation, transparency, and cryptography**:

* Smart contracts hold funds securely
* Neither Florune nor any third party can access funds
* Payments follow signature-verified, immutable logic
* Status is always transparent to both parties
* Options for rollback, cancellation, or conditional release

This makes it suitable for **everything from small digital engagements to high-value deals** worth thousands or millions.

---

## **Use Cases**

### **1. High-Value B2B Transactions**

*Manufacturing orders, consulting retainers, licensing fees*

* Securely holds large sums
* Ensures contract milestones are met
* Prevents fraud or late delivery

### **2. Freelance / Gig Work**

*Design, development, marketing, writing, auditing*

* Client deposits funds in escrow
* Freelancer completes work
* Payment released on approval

### **3. P2P Item Purchases**

*High-value goods, collectibles, hardware, digital assets*

* Buyer locks payment
* Seller delivers
* Buyer verifies and releases

### **4. Deposits, Rentals, Prepayments**

*Real estate, equipment rentals, agency pre-bookings*

* Supports refundable deposits
* Automatically rolls back if conditions fail

### **5. Large Digital Deliverables**

*Software source code, research, proprietary datasets*

* Easily combines with **Verifiable Documents**
* Ensures proof-of-delivery before release

### **6. Content & Digital Asset Sales**

* Protects both creators and buyers
* Seamless integration with **Asset Paywall**

---

## **Key Features**

### **1. Trustless, Non-Custodial Fund Holding**

Funds are locked in smart contracts — not controlled by Florune or any third party.

### **2. Safe for High-Value Transactions**

Smart contracts guarantee:

* No freezing
* No mismanagement
* No interference
* No misappropriation

### **3. Revocable, Time-Bound, and Rollback Support**

Automated safety mechanisms for any agreement size.

### **4. Simple Fee Structure**

* **Flat deposit fee**
* **1% withdrawal fee**
* No subscriptions required

Cheaper and safer than centralized escrow — even for high-value deals.

### **5. Complete Status Transparency**

Escrow lifecycle:

* **Open**
* **Freeze**
* **Release**
* **Cancel**

Every party always knows the exact state.

### **6. Wallet-First, On-Device Execution**

All actions happen through the Florune Wallet — intuitive, secure, and verifiable.

---

## **Escrow Lifecycle (Status Guide)**

| Status      | Meaning                                            |
| ----------- | -------------------------------------------------- |
| **Open**    | Escrow created; awaiting token approval or deposit |
| **Freeze**  | Funds locked securely inside smart contract        |
| **Release** | Funds released to the recipient                    |
| **Cancel**  | Funds refunded to the sender                       |

---

## **Step-by-Step Tutorial**

### **Prerequisites**

* Florune Wallet installed
* Gas tokens available
* Payment token approved for use

---

## **A. Creating an Escrow Deposit**

1. Open **Create → Escrow Deposit**
2. Enter:

   * Recipient address
   * Amount
   * Optional memo
3. Select network
4. Tap **Create**
5. Escrow appears in **History**

---

## **B. Approving Tokens for Escrow**

1. Open the escrow record
2. Tap **Approve Token**
3. Confirm the transaction

Once approved, the deposit can be made.

---

## **C. Depositing Funds**

1. Open the escrow record
2. Tap **Deposit**
3. Enter the amount
4. Confirm
5. Status becomes **Freeze**

---

## **D. Releasing or Canceling**

### **Release**

Used when obligations are met:

* Work delivered
* Product received
* Agreement fulfilled

User taps **Release → Confirm**.

### **Cancel**

Used when:

* Conditions fail
* Deadlines pass
* Mutual cancellation occurs

Funds are returned to the sender.

---

## **Real-World Examples**

### **1. High-Value Contract Payment**

$50,000 locked → Developer delivers → Company verifies → Funds released.

### **2. Hardware Purchase**

Buyer deposits → Seller ships → Buyer confirms → Funds released.

### **3. Security Deposit**

Tenant deposits → No issues → Deposit returned upon cancellation.

---

## **Benefits**

* Safe for **high-value** and **cross-border** payments
* Non-custodial and censorship-resistant
* Transparent and automated lifecycle
* Eliminates fraud and trust issues
* Simple and predictable costs
* Integrates with **Pledge Contracts** and **Paywalls**

---

## **Drawbacks**

* Requires blockchain familiarity
* Both parties must manage wallets
* No centralized party can force a resolution
