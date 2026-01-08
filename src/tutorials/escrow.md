# Escrow

*A trustless, non-custodial payment safeguard for peer-to-peer and high-value transactions.*

---

## **Overview**

SafePulse Escrow is a **trustless, non-custodial onchain escrow service** that securely locks funds until both parties meet agreed-upon conditions. Designed for **buyers, sellers, freelancers, enterprises, and service providers** where trust and protection are critical.

With transparent fees and guaranteed neutrality, SafePulse Escrow eliminates fraud risks and intermediaries — delivering a secure, automated environment for global payments of any size.

---

## **Context & Problem**

### **The Problem**

Digital agreements — whether between individuals or businesses — frequently face:

* Payment fraud
* Delivery disputes
* Chargebacks
* Unenforceable promises
* Lack of trusted middlemen
* High cost of middlemen
* No protection for large-value deals
* Opaque transaction processes

Centralized escrow alternatives exist, but they introduce:

* High fees (often 2–10%+)
* Custodial risk (fund freezing, loss, shutdowns)
* Slow and costy dispute resolution
* Geographic restrictions
* Risk of platform censorship

For **large-value or cross-border transactions**, these risks become even more severe.

### **The Solution**

SafePulse Escrow replaces intermediaries with **automation, transparency, and cryptography**:

* Smart contracts hold funds securely
* Neither SafePulse nor any third party can access funds
* Status is always transparent to both parties
* Options for rollback, cancellation, and freeze under safe conditions and only by parties

This makes it suitable for **everything from small digital engagements to high-value deals**.

---

## **Use Cases**

### **1. High-Value Transactions**

*Manufacturing orders, consulting retainers, licensing fees*

* Securely holds large sums
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

### **5. Content & Digital Sales**

* Protects both sellers and buyers

---

## **Key Features**

### **1. Trustless, Non-Custodial Fund Holding**

Funds are locked in smart contracts — not controlled by SafePulse or any third party.

### **2. Safe for High-Value Transactions**

Smart contracts guarantee:

* No third-party access
* No interference
* No misappropriation

### **3. Revocable, Time-Bound, and Rollback Support**

Automated safety mechanisms for any agreement size.

### **4. Simple Fee Structure**

* **Flat deposit fee (pays in network native token)**
* **1% withdrawal fee**
* No subscriptions or access token required

Cheaper and safer than centralized escrow — even for high-value deals.

### **5. Complete Status Transparency**

Escrow lifecycle:

* **Open**
* **Freeze**
* **Release**
* **Cancel**

Every party always knows the exact state.

### **6. Wallet-First, On-Device Execution**

All actions happen through the SafePulse Wallet — intuitive, secure, and verifiable.

---

## **Escrow Lifecycle (Status Guide)**

| Status      | Meaning                                            |
| ----------- | -------------------------------------------------- |
| **Open**    | token deposited, waiting for release/freeze/cancel |
| **Freeze**  | Funds locked securely inside smart contract until expiration time |
| **Release** | Funds released and allow recipient to withdraw     |
| **Cancel**  | Allow sender/buyer/contractee to refund            |

---

## **Step-by-Step Tutorial**

### **Prerequisites**

* SafePulse Wallet installed
* Gas tokens available
* Payment token approved for use

---

## **A. Approving Tokens for Escrow**

1. Open the escrow record
2. Tap **Approve Token**
3. Confirm the transaction

Once approved, the deposit can be made.

---

## **B. Creating an Escrow Deposit**

1. At organize section onder title of escrow Tap **Approve**
2. Enter:

   * Recipient address
   * Amount
   * expiration date
3. Select network and token
4. Tap **Deposit**
5. Escrow appears in **History**
6. Share Deposit DID with your party

---

## **C. Releasing or Canceling**

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

### Escrow Contract Status Guide

#### 1. `open`

**Meaning:** Funds deposited, escrow active.

* 🚫 Withdraw
* ✅ Rollback → allowed 5 days after expiration

---

#### 2. `freeze`

**Meaning:** Escrow blocked.

* 🚫 Withdraw
* 🚫 Rollback

---

#### 3. `release`

**Meaning:** Escrow released to seller.

* ✅ Withdraw (seller)
* 🚫 Rollback

---

#### 4. `cancel`

**Meaning:** Escrow canceled.

* 🚫 Withdraw
* ✅ Rollback (buyer)

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
