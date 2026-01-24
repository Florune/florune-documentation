# Transparency

This page describes how SafePulse operates, what it can and cannot do, and how user funds, data, and contracts are handled. It is intended to provide clear, verifiable information for users, developers, auditors, and regulators.

---

## 1. Platform Status

SafePulse is live and operational.

* **Mainnet:** Active
* **Testnet:** Active
* **Environment:** Production

SafePulse provides smart-contract infrastructure for agreements, payments, and document verification.

---

## 2. Custody & Control Model

### Non-Custodial by Design

SafePulse is a **non-custodial platform**.

* SafePulse **does not hold user funds**
* SafePulse **does not control private keys**
* SafePulse **cannot move funds without user authorization**
* SafePulse **cannot access or recover user assets**

All asset movement requires cryptographic signatures from the relevant user wallets.

### Contracts Involving Deposits

In the following contracts, users deposit funds into **SafePulse smart contracts**:

* Escrow contracts
* Document Registry contracts
* Asset Paywall contracts

These contracts are **non-custodial**:

* Funds are controlled exclusively by contract logic and user signatures
* Only depositors and contract parties can access or release funds
* SafePulse has **no unilateral control** over deposited assets

### Contracts Without Deposits

In the following contracts, SafePulse has **no access or control** at all:

* Pledge Contracts
* Verifiable Document contracts

Each instance is deployed per user and operates independently.

---

## 3. Private Keys & Signatures

* SafePulse **never generates, stores, transmits, or recovers private keys**
* All interactions require **direct wallet signatures**
* SafePulse servers cannot trigger on-chain actions independently

---

## 4. Smart Contract Architecture

### Upgradeability

* Smart contracts are **upgradeable**
* Upgrade mechanisms exist to:

  * Fix security vulnerabilities
  * Patch bugs
  * Add new features

Upgrades are **not used** to:

* Take custody of user funds
* Change ownership or withdrawal rights
* Introduce asset seizure or hidden controls

User-deployed contracts can be upgraded **only by the contract owner**, at their discretion.

### Pausable Functions

Some contracts include **limited pause mechanisms**, strictly for protocol protection.

* Only specific functions (e.g., new deposits or new registrations) may be paused
* Existing user funds remain accessible to their owners
* Withdrawals and user-controlled actions remain available
* No pause function allows SafePulse to move or seize assets

#### Asset Paywall: Content-Based Restrictions

**Only for Asset Paywall contracts**, SafePulse includes a **limited content-based restriction mechanism** designed to mitigate the distribution of clearly illegal material.

In response to **credible reports of illegal content** — for example, sexual exploitation, harassment, or any kind of illegal NSFW material— SafePulse may **temporarily freeze access to funds** held within the affected Asset Paywall contract and **remove the associated media payment gate access**.

This mechanism:

* Applies **exclusively** to Asset Paywall contract
* Does **not** allow SafePulse to withdraw, transfer, or seize user funds
* Does **not** grant ownership or custodial control to SafePulse
* Restricts access **only at the contract level** and **only temporarily**
* Includes removal of references to the offending asset from SafePulse’s off-chain database
* Exists solely for compliance with legal obligations related to unlawful material

Frozen funds remain locked within the smart contract and **cannot be accessed, moved, or repurposed by SafePulse**.

No other SafePulse contract types include content-based restrictions, freeze mechanisms, or discretionary intervention by SafePulse.

This mechanism exists because SafePulse, as the operator of paid content gating, may have legal obligations concerning the distribution of unlawful material.

---

## 5. Escrow & Dispute Handling

* Escrow contracts are **fully peer-to-peer**
* **No arbitration layer**
* **No human intervention**
* **No dispute resolution by SafePulse**

SafePulse does not:

* Act as an arbiter
* Provide legal advice
* Make judgments or rulings

All outcomes are determined by smart-contract logic and cryptographic proofs.

On-chain records and signatures may serve as **cryptographic evidence** that can be used externally (e.g., legal proceedings), but SafePulse does not participate in such processes.

#### Dispute Prevention by Design:

SafePulse contracts are built with automated, rule-based logic that enforces agreement conditions. By encoding obligations, milestones, and verification requirements directly into the contracts, most potential conflicts are resolved automatically. This design minimizes the need for human intervention or arbitration, while ensuring that outcomes are predictable and verifiable by all parties.

---

## 6. Source Code & Intellectual Property

* SafePulse software is **closed-source**
* All components are protected under copyright
* The platform and its contracts are proprietary intellectual property of the platform owner

No developed components are currently open-source.

---

## 7. User Accounts & Data Collection

### Account Creation

* No off-chain accounts are created
* No emails or usernames are collected
* Wallet connection is the only authentication method

### Data Collection

SafePulse does **not** collect:

* Emails
* Names
* Phone numbers
* IP addresses
* Device fingerprints
* Any Sensetive data

SafePulse does **not** use:

* Cookies
* Tracking scripts

### Off-Chain Data

The only off-chain references stored are **user-provided asset identifiers**, such as:

* IPFS CIDs
* Arweave transaction IDs
* Web URLs

These references may be encrypted in a decentralized way. SafePulse does not have access to encrypted content.

---

## 8. Identity, KYC & Compliance

* **No KYC**
* **No AML onboarding**
* **No identity verification**

Authentication is performed using **self-sovereign cryptographic identity**, including:

* W3C Decentralized Identifiers (DIDs)
* ERC-1056 / uPort-compatible identities
* Public or pseudonymous wallet identities

---

## 9. Jurisdiction & Legal Requests

SafePulse operates as a **software platform**, not as a financial or legal intermediary.

* The platform itself is not bound to a specific jurisdiction
* The platform owner is registered as a sole legal business owner

SafePulse policy:

* Publish transparency reports
* Notify users of legal requests when legally permitted
* Do not voluntarily share user data

SafePulse cannot provide private keys, recover funds, or reverse transactions.

---

## 10. Security & Audits

* Smart contracts have undergone security audits
* Audit reports are **not publicly published**
* Security disclosures are accepted via:

**Email:** `security@safepulse.xyz`
**GitHub:** Issues may be submitted to relevant repositories

---

## 11. Platform Limitations

SafePulse explicitly does **not**:

* Hold custody of assets
* Reverse transactions
* Resolve disputes
* Enforce legal agreements
* Recover lost keys
* Freeze or confiscate funds
* Act on behalf of users

Users retain full responsibility for:

* Key management
* Contract configuration
* Jurisdictional compliance
* Legal enforceability

---

## 12. Changes to This Page

This Transparency page may be updated to reflect:

* New features
* Security updates
* Regulatory clarity

Material changes will be documented publicly.
