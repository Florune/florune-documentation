# 📘 How-To Guides

This section provides step-by-step instructions for using Contract Foundry’s features via the official Android wallet application. All operations—from identity creation to smart contract deployment—are executed locally on your device, ensuring secure, self-sovereign interaction with the blockchain.

> ⚠️ **Note**: All actions require a EOA as delegate and for deployment an active subscription plan or account charge based on usage needs.

---

## Overview

This documentation explains how to create and manage **Verifiable Documents**, **Pledge Contracts**, **Escrow Deposits**, **Document Registries**, and **Asset Paywalls** on the platform.

---

## 📑 Verifiable Document

### Steps

1. Navigate to **Create** → tap **Create** button.
2. Upload file to:

   * IPFS
   * Arweave
   * Centralized host with direct download link
3. Copy the file link.
4. Fill the form:

   * Paste file link
   * Choose network
5. Tap **Create** (top of screen).
6. Confirm blockchain transaction.
7. After minting → go to **History**.
8. Locate the document record.
9. From **More**, select **Initialize and Setup**.
10. Share the **Verifiable Document DID**.

---

## 📜 Pledge Contract

> **Issuer = Seller**
> Must be created on the same network as the linked Verifiable Document.

### Steps

1. Navigate to **Create** → tap **Create**.
2. Fill the form:

   * Choose network
   * Select token
   * (Optional) Link to Verifiable Document:

     * Toggle **Document Link**
     * Enter Verifiable Document DID
3. Tap **Create** (top of screen).
4. Confirm transaction.
5. After minting → go to **History**.
6. Locate pledge record.
7. From **More**, select **Initialize and Setup**.
8. Confirm transaction.
9. Share **Pledge Contract DID** with buyer.

**Fees & Conditions**

* 0% withdrawal fee
* Other platform terms may apply

---

### 🔄 Pledge Contract Status Guide

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

## 💰 Escrow Deposit

> **Depositor = Customer/Buyer**
> Stablecoin deposits require approval first.

### Pre-requisite: Token Approval

1. Navigate to **Organize**.
2. Choose network and token.
3. Set allowed approval amount.

### Steps

1. From **Escrow Contract card** → tap **Deposit Contract**.
2. Fill in the form:

   * Network
   * Token
   * Expiration time
3. Tap **Deposit** (top of screen).
4. Confirm transaction.
5. Share **Escrow DID** with seller.

**Fees & Conditions**

* Flat fee for deposit
* 1% withdrawal platform fee

---

### 🔄 Escrow Contract Status Guide

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

## 🗂️ Document Registry

* Works like Verifiable Document creation.
* No **Initialization** step required.
* Instead of **Create**, tap **Register**.
* Issuer must have balance to cover flat registration fee.

---

## 🔐 Asset Paywall Registration

### Steps

1. Upload file to:

   * IPFS
   * Arweave
   * Centralized storage (direct download link required)
2. Ensure issuer has balance for flat registration fee.
3. Register asset via platform interface.
