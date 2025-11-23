# Asset Paywall

*Decentralized content monetization with onchain access control, multi-payment support, and DID-authenticated delivery.*

---

## **Overview**

The **Asset Paywall** service allows creators, businesses, and developers to **register an digital content delivery contract**.
It is designed to support:

* **Digital content sales** (media, PDFs, files, videos, audio, images)
* **Knowledge & research monetization**
* **Premium memberships**
* **One-time or tiered access models**
* **Onchain payment validation**
* **DID-authenticated access**

The Asset Paywall integrates deeply with the Florune ecosystem, using:

* **DIDs** for identity/authorship

It works fully **wallet-first**, ensuring users **retain local control** while publishers remain **sovereign owners** of their content.
Issuers wont share ownership, they register an content delivery contract, customers approve the contract by payment and receive content identifier. 

---

## **Context & Problem**

### **The Problem**

Most content monetization platforms:

* Require central hosting
* Control creator accounts
* Can censor, block, or shadowban
* Offer weak content protection
* Depend on fragile credential-based logins

Creators need **trustless payment** and **ownership** without relying on intermediaries.

### **The Solution**

Florune’s **Asset Paywall**:

* Uses **smart-contract payments**
* Deliver **content identifier** after payment
* Stores protected assets via decentralized links or secure URLs
* Uses **DID**, not centralized accounts
* Runs entirely from the user's wallet (no platform custody)

---

## **Key Features**

### 💸 **1. Multi-Asset Payments**

Publishers can charge:

* Stablecoins
* Other chain-native assets (where supported)

### 🎫 **2. Flexible Access Models**

* **One-time purchase means approve contract**

### 📍 **3. Onchain Proof of Purchase**

Proofs are stored as lightweight logs and anchored to the buyer’s DID.

---

# **Use Cases**

## **1. Content Creators & Educators**

* Paid course videos
* Premium guides and PDFs
* Photography, digital art, designs
* Locked newsletters or research papers

## **3. Media & Journalism**

* Pay-per-article
* Premium investigations
* Subscriber-only content

## **4. Businesses & Enterprises**

* Shared documents 
* Monetized research reports

---

# **Step-by-Step Tutorial**

## A. **Creating a Paywalled Asset**

* Upload or host file on an centralized or decentralized storage
1. Open the wallet
2. Tap **Asset Paywall**
3. Choose the asset type
4. Choose your payment configuration

   * Issuer DID
   * Network and token
   * Price
   * Asset Name
6. Confirm onchain deployment
7. Asset Paywall contract is deployed
8. Share the asset **DID**

---

## B. **User Purchasing Access**

1. Open wallet
2. Scan Paywall QR or paste DID
3. View content preview + price
4. Tap **Purchase**
5. Wallet executes payment contract
6. On success, wallet receives access token bound to DID
7. Content unlocks automatically

---

## C. **Managing Asset**

At Contract organization there is options for freeze/unfreeze asset, collect payments or delete asset.

---

# **Real-World Examples**

### Example 1 — Paid PDF Guide

A researcher sells a 200-page PDF on IPFS via paywall.
After paying, users get a DID-bound decryption key.

### Example 2 — Video Course

Teacher uploads course videos behind a paywall with 30-day access.

### Example 3 — Premium Article

A journalist publishes a pay-per-article story with a one-time purchase.

### Example 4 — Photography Pack

A designer distributes a set of high-resolution files, protected by the paywall.

---

# **Benefits**

### For Creators

* 1% platform fees
* No censorship
* Automated payments
* Privacy first, no KYC

### For Users

* No centralized accounts
* Portable access
* Verifiable proof of purchase
* Zero-knowledge access control

### For Businesses

* Internal distribution
* Contract-based licensing
* Easy integration

---

# **Drawbacks / Considerations**

* Requires gas fees on deployment
* Content hosting costs depend on storage provider
* Price changes may require redeployment (contract-defined)
* Users must protect local wallet keys for access retention

---

# **Best Practices**

* **Always encrypt sensitive files** before uploading
* Offer **low-cost preview content** to improve user trust
