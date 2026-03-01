# White Paper: On-Chain Context Protocol (OCCP)
**— A New Physics of Information: Equating "Value Transfer" with "Information Persistence" —**

## 1. The Concept

### 1.1 Background: The Limits of Centralized Infrastructure and the "Gravity of Maintenance"
In today's digital infrastructure, information is eternally bound by the gravity of continuous fixed costs—specifically, server maintenance fees. The moment a corporation or individual ceases to bear these costs, even the most valuable records vanish from the network. While many Web3 projects claim decentralization, most still rely on specific servers for front-ends or indexing databases, failing to achieve true **"autonomous permanence."**

### 1.2 The Solution: Self-Financing Infrastructure via "Liquidity"
The On-Chain Context Protocol (OCCP) proposes a paradigm shift: converting **"currency liquidity (transactions)"** itself into the power source for recording and preserving information. By utilizing the transaction fees (network costs) inherent in the transfer of value as a direct mechanism for storage maintenance, a "self-circulating infrastructure" is established. As long as the economic zone (the network) remains active, information is externalized and preserved without the need for anyone's permission or recurring payments.

---

## 2. Core Architecture
This protocol defines the following architectural principles as a universal, decentralized data structure independent of specific blockchain specifications.

### 2.1 Data Encapsulation in Ledger Margins
OCCP utilizes the "arbitrary data fields (metadata or memo fields)" provided by any distributed ledger—be it a public chain, consortium, or currency system—as storage cells for information. By encapsulating encrypted text within the economic activity of a remittance, data preservation rides piggyback on the network's consensus process.

### 2.2 Index Optimization and Context Generation via Native Queries
Given the vastness of public ledger data, full-client-side searching of specific contexts (streams) is impractical. To function as true decentralized infrastructure, a design that **utilizes only the standard APIs (RPC calls) provided by nodes while minimizing client-side filtering** is essential.

OCCP solves this through:

* **Contextual Links (Linked List):** Each transaction embeds the hash of the preceding record (parent pointer). Once an entry point is found, the context (diaries, blogs, etc.) is logically reconstructed by following the chain backward.
* **HEAD Management via State Pointers:** By utilizing resources that can be queried with minimal load (such as account token balances or account states), the "latest transaction hash (HEAD)" of a stream is recorded and updated. This allows the client to locate the latest information with a single query to a node, without relying on external indexing servers.

---

## 3. Empirical Architecture: Hacking and Implementation on XRPL (SUBOS)
This chapter serves as a record of the experimental implementation of OCCP, titled **"SUBOS."** It is an embodiment of Proof of Existence.

To demonstrate how the universal architecture defined in the previous chapter can operate on existing financial infrastructure, we built SUBOS—an integrated terminal that pushes the specifications of the XRP Ledger (XRPL) to their limits. We chose XRP for its ultra-low costs, its ~1kb memo capacity, and its widespread global adoption.

Standard XRPL node (rippled) RPCs lack advanced queries like "search transactions containing specific memo text." We bypassed this limitation through the following "roundabout yet rational hack":

### 3.1 Data Layer: The Shouting (Injection into Memos)
Using XRPL's low-cost `Payment` transactions, text data is converted to HEX and written into the `MemoData` field. By prefixing the data with a protocol identifier and the "parent transaction hash (64 characters)," a robust contextual link is formed.

### 3.2 Indexing Layer: The Pinning (State Pointers via NFT)
One of the fastest, lowest-load commands in the standard XRPL RPC is `account_nfts`, which retrieves a list of NFTs held by an account. We subverted this specification by **redefining NFTs—typically used for art or proof of ownership—as "Index Pointers" indicating the latest position of a stream.**

With each new post, a new NFT is minted with the "Label Name" and "Latest Transaction Hash" encoded in its URI, while the old NFT is burned. This allows the client to render the latest state of countless streams by issuing a single query for the wallet's NFT list.

---

## 4. The Vision
The scope of OCCP is not limited to the XRPL. Organizations issuing centralized currencies (corporate consortia, in-game economies, or national CBDCs) can adopt this "Transaction-Backed Infrastructure Model" to dissolve massive server operation costs into the liquidity of the economic zone. Every economic transaction automatically reinforces and maintains the information infrastructure.

It is also possible to bridge this with centralized servers or optimize the chain by embedding multiple hashes into a single NFT or memo.

We envision a world where data is liberated from the physical cages of servers, circulating eternally through the "blood" (liquidity) of the network. This is the establishment of a new **"Physics of Information"** where "Value Transfer" and "Information Preservation" are perfectly equivalent.

*(There are likely other low-cost decentralized ledgers with superior searchability. But since I have already built this on XRP, please bear with me for now.)*

---

## 5. Origin and Language Authority
This protocol (OCCP) and its experimental implementation "SUBOS" were conceptualized, architected, and documented within a **Japanese linguistic environment.**

The conceptual frameworks, naming conventions, and design philosophies contained herein are not translations of existing Western concepts but are **primary descriptions** formed during the implementation process.

Therefore, the **Japanese version** of this White Paper shall be recognized as the **Primary Definition (Original Text).** All other language versions are provided as reference translations only. While OCCP does not belong to any specific nation or organization, the fact that its initial definition was established in the **Japanese language** is hereby recorded.
