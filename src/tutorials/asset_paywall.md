# Asset Paywall

*Decentralized content monetization with onchain access control, multi-payment support, and DID-authenticated delivery.*

---

## **Overview**

The **Asset Paywall** service allows creators, businesses, and developers to **lock digital content behind a secure paywall** and grant access only when payment is confirmed.
It is designed to support:

* **Digital content sales** (media, PDFs, files, videos, audio, images)
* **Knowledge & research monetization**
* **Premium memberships**
* **One-time or tiered access models**
* **Onchain payment validation**
* **DID-authenticated access**

The Asset Paywall integrates deeply with the Florune ecosystem, using:

* **DIDs** for identity/authorship
* **Verifiable Documents** for content metadata
* **Document Registry** for anchoring
* **Wallet-based decryption access**
* **Rune, stablecoins, or supported assets** as payment

It works fully **wallet-first**, ensuring users **retain local control** while publishers remain **sovereign owners** of their content.

---

## **Context & Problem**

### **The Problem**

Most content monetization platforms:

* Take high fees
* Require central hosting
* Control creator accounts
* Can censor, block, or shadowban
* Offer weak content protection
* Depend on fragile credential-based logins

Creators need **trustless payment**, **creator ownership**, and **secure access control** without relying on intermediaries.

### **The Solution**

Florune’s **Asset Paywall**:

* Uses **smart-contract payments**
* Grants **verifiable, cryptographic access** after payment
* Stores protected assets via decentralized links or secure URLs
* Uses **DID-based access control**, not centralized accounts
* Runs entirely from the user's wallet (no platform custody)
* Allows **revocable, transferable, permissioned** access control

---

## **Key Features**

### 🧱 **1. Contract-Based Access Control**

Access rules are enforced via smart contracts, not centralized servers.

### 💸 **2. Multi-Asset Payments**

Publishers can charge:

* Rune
* Stablecoins
* Other chain-native assets (where supported)

### 🔐 **3. DID Gated Content**

Only users with valid DID + payment signature can access the asset.

### 🎫 **4. Flexible Access Models**

* **One-time purchase**
* **Timed access** (24h, 7d, 30d, custom)
* **Subscription-like periodic renewal**
* **Tiered access** (Basic, Pro, VIP)

### 🗂️ **5. Multiple Asset Types Supported**

* Documents
* PDF
* Audio
* Images
* Video
* Encrypted files
* Private URLs
* API endpoints

### 📍 **6. Onchain Proof of Purchase**

Proofs are stored as lightweight logs and anchored to the buyer’s DID.

### 🔄 **7. Revocable Access**

Creators can optionally revoke access manually or by rule triggers.

---

# **Use Cases**

## **1. Content Creators & Educators**

* Paid course videos
* Premium guides and PDFs
* Photography, digital art, designs
* Locked newsletters or research papers

## **2. Developers & API Monetization**

* API endpoints that unlock after payment
* Tiered access for dev tools
* Fair usage with onchain proofs

## **3. Media & Journalism**

* Pay-per-article
* Premium investigations
* Subscriber-only content

## **4. Businesses & Enterprises**

* Internal documents shared securely
* Monetized research reports
* Document-based licensing

## **5. Web3 Monetization**

* NFT media backup paywalls
* DAO-controlled content
* Creator tokens integrated with paywall flows

---

# **Technical Architecture**

### **1. Asset**

The actual content stored as:

* Encrypted file
* Direct URL
* IPFS/Arweave link
* Verifiable Document wrapper

### **2. Access Contract**

Blockchain contract managing:

* Payment verification
* Expiration time
* Access rules
* Revenue splits (future feature)

### **3. User DID**

Used to bind access permission to the buyer.

### **4. Wallet Execution**

All requests and decryptions run locally inside the user’s device.

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

### Example 3 — Private API

Developers expose “Premium Quotes API” behind a blockchain-verified paywall.
Users automatically renew access each week.

### Example 4 — Premium Article

A journalist publishes a pay-per-article story with a one-time purchase.

### Example 5 — Photography Pack

A designer distributes a set of high-resolution files, protected by the paywall.

---

# **Benefits**

### For Creators

* Zero platform fees (creator keeps all revenue)
* Full ownership of content
* No censorship
* Automated payments
* DID-based control

### For Users

* No centralized accounts
* Portable access
* Verifiable proof of purchase
* Zero-knowledge access control

### For Businesses

* Secure internal distribution
* Reliable access logs
* Contract-based licensing
* Easy integration with enterprise workflows

---

# **Drawbacks / Considerations**

* Requires gas fees on deployment
* Content hosting costs depend on storage provider
* Price changes may require redeployment (contract-defined)
* Users must protect local wallet keys for access retention

---

# **Best Practices**

* **Always encrypt sensitive files** before uploading
* Use **Document Registry** to timestamp ownership claims
* Use **DID rotation** if upgrading identity keys
* Offer **low-cost preview content** to improve user trust
* Avoid embedding full content in URL — use encrypted storage
