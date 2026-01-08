# Decentralized Storage

Decentralized storage refers to a method of **storing digital data across a distributed network** rather than on centralized servers. By leveraging blockchain and peer-to-peer technologies, decentralized storage ensures **data immutability, censorship resistance, and long-term availability**, empowering users with **full control over their data** without relying on any single authority.

In the SafePulse ecosystem, decentralized storage plays a critical role in **storing verifiable documents, smart contract references, and other high-value data assets**, enabling secure and verifiable interactions between users, smart contracts, and third parties. Two of the most widely used decentralized storage protocols are **Arweave** and **IPFS (InterPlanetary File System)**.

---

### **Arweave**

**Arweave** is a **permanent, blockchain-backed storage protocol** designed for long-term, immutable data storage. Data uploaded to Arweave is stored in a distributed network and guaranteed to persist **forever** through a one-time upfront fee. Each piece of data stored is assigned a **unique transaction ID (TxID)**.

The **TxID** serves as a permanent reference to the stored data, allowing it to be **retrieved, verified, and referenced by smart contracts, applications, or users** at any time. Arweave’s storage model ensures that once data is uploaded, it cannot be altered or deleted, providing **tamper-proof auditability** critical for legal, institutional, and contractual documents.

Arweave employs a **blockweave structure**, an evolution of traditional blockchain, which links data together using a combination of cryptographic proofs and consensus mechanisms. This ensures both **data permanence** and **efficient network scalability**.

---

### **IPFS (InterPlanetary File System)**

**IPFS** is a **peer-to-peer distributed file system** that addresses data by its **content hash** rather than its location. Unlike centralized servers where files are located at a fixed URL, IPFS retrieves data from any node storing that content, making the system **resilient and decentralized**.

Every file or folder uploaded to IPFS is assigned a **Content Identifier (CID)**, a cryptographic hash of the file’s contents. The CID ensures **integrity**, meaning any modification to the file results in a different CID. This makes IPFS ideal for **verifiable, tamper-resistant references** in decentralized applications.

IPFS operates with a **distributed hash table (DHT)** to locate nodes storing the requested content. When a user requests a file via its CID, the network identifies peers hosting the file and retrieves it efficiently from multiple sources, ensuring **redundancy and fault tolerance**. Unlike Arweave, IPFS data persistence depends on **pinning services or active hosting**, as files may not remain available unless intentionally preserved.

---

### **Identifiers: Arweave TxID vs IPFS CID**

* **Arweave TxID**: A unique transaction identifier that permanently links to stored data on the Arweave network. Once uploaded, data associated with a TxID is immutable and guaranteed to persist indefinitely.
* **IPFS CID**: A content-based cryptographic hash that identifies a file by its content. Changing the file changes its CID. Data availability depends on nodes hosting or pinning the content.

By combining **Arweave and IPFS**, SafePulse ensures **both permanent and distributed storage options**, allowing users to store critical documents securely, reference them in smart contracts, and verify them without relying on any centralized system. These protocols are essential for **tamper-proof operations, verifiable credentials, and long-term digital record integrity**.
