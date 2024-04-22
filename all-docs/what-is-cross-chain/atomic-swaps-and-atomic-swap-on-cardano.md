# Atomic Swaps and Atomic Swap on Cardano

### Introduction

Atomic swaps are a groundbreaking technology that enables the direct, peer-to-peer exchange of cryptocurrencies between different blockchain networks. They offer a decentralized, secure, and efficient way to trade digital assets without relying on centralized exchanges or third-party intermediaries. This document aims to provide an in-depth understanding of atomic swaps, how they work, and how they compare to other methods like blockchain bridges. We will also delve into the onely atomic Swap service built on the Cardano blockchain which is also called [Atomic Swap](https://atomic-swap.io).

### How It Works

Atomic swaps utilize smart contracts and cryptographic techniques to facilitate asset exchange. The core mechanism involves Hash Time-Locked Contracts (HTLCs), which lock the assets being swapped until certain conditions are met. Both parties create HTLCs on their respective blockchains, and the assets are released simultaneously once the conditions are fulfilled. This ensures that the swap is "atomic," meaning it either happens entirely or not at all.

### Technical Components

* HTLCs: Hash Time-Locked Contracts lock the assets and set conditions for the trade.
* Multisig Transactions: Require multiple signatures to authorize a transaction.
* Time Locks: Ensure that assets are returned if conditions are not met within a specified time.

### Comparison to Bridges

Blockchain bridges are another solution for cross-chain interoperability. Unlike atomic swaps, bridges often involve third-party validators and are not always fully decentralized. Here are some key differences:

* User Experience: Bridges can be more user-friendly but may require trust in third-party validators.
* Complex Transactions: Bridges can support more complex transactions like transferring NFTs or executing smart contracts across chains.
* Security: Bridges introduce potential points of failure, making them less secure than atomic swaps.

### Pros and Cons

**Pros**

* Decentralization: Atomic swaps are fully decentralized, eliminating the need for a trusted third party or centralized exchange.
* Security: The use of cryptographic proofs and smart contracts like HTLCs ensures a secure transaction, minimizing the risk of fraud.
* Privacy: Since transactions are peer-to-peer, there's no need to share personal information with an intermediary, enhancing privacy.
* Reduced Costs: Without the need for third-party services, transaction fees can be significantly lower.
* Interoperability: Atomic swaps facilitate seamless transactions between different blockchains, enhancing the utility of digital assets.
* Transparency: All transactions are recorded on the blockchain, providing a transparent and immutable history.

**Cons**

* Complexity: The underlying technology can be complex, making it less accessible for users who are not tech-savvy.
* Limited Support: Not all blockchains support the features needed for atomic swaps, such as HTLCs, limiting the range of possible swaps.
* Time Sensitivity: The use of time-locked contracts means that both parties need to be online and act within a specific timeframe, which may not always be convenient.
* Liquidity Issues: In a decentralized setting, finding a matching party for a swap can be challenging, especially for less popular assets.
* Risk of Code Flaws: While smart contracts aim to ensure security, they are only as reliable as the code they are written in. Bugs can introduce vulnerabilities.

## Atomic Swap Service on Cardano

The Atomic Swap service built on Cardano, as described in its whitepaper, allows for synchronous P2P trading of any number of assets, including tokens and NFTs. It eliminates the need for smart contracts and escrow services by using multisig transactions.

### How It Works

#### Technical Background

**UTxO Model** Cardano employs the Unspent Transaction Output (UTxO) model to represent assets electronically. Each UTxO can be thought of as a digital coin with a specific value, which can vary from fractions to millions. When you want to make a transaction, you have to use the entire UTxO and then send the change back to yourself. This ensures that the inputs and outputs of a transaction are always balanced.

**Native Assets** Cardano supports native assets that reside in UTxOs. These assets are identified by a policyID and an asset name, making them unique and easily tradable. The policyID is the hash of the script that defines the conditions under which the asset can be minted or burned.

**Min ADA Amount** Every UTxO on Cardano must contain a minimum amount of ADA to prevent network spam. The minimum ADA requirement is dependent on the size of the UTxO and increases with the number of distinct native assets.

**Multi-Signature Transactions** Multisig transactions require multiple keys to authorize a transaction. These keys can be controlled by different wallets, adding an extra layer of security.

#### Algorithmic Steps

The algorithm for executing a swap involves several steps, each serving a specific purpose:

* Add Commission UTxO: The algorithm starts by adding a UTxO to cover the commission fees for the transaction.
* Add Receiver UTxOs: UTxOs containing what each participant will receive are added next.
* Estimate Fee: The network fee is estimated at this stage.
* Add Sender Inputs: Inputs to cover what each participant will be sending are added, along with half of the estimated fee and half of the commission.
* Calculate Change: The algorithm estimates the change that each participant will receive.
* Balance Equation: The algorithm ensures that the equation inputB + inputA == commissionB + commissionA + fee + changeB + changeA + receiveA + receiveB holds true. If it doesn't, the algorithm adjusts the inputs and runs again.

#### Fee Calculation and the "Chicken and Egg" Problem

The algorithm solves a "chicken and egg" problem related to transaction fees. The fee is based on the size of the transaction, which depends on the number of inputs and outputs. However, the size can't be known until all inputs and outputs are added, which in turn depends on the fee. This is resolved by running the algorithm multiple times until it reaches a fixed point.

#### Security Measures

Before finalizing the transaction, users can scrutinize the transaction sign screen to ensure that the transaction details match their expectations. This step is crucial for security and prevents any unauthorized or fraudulent activities.

## Conclusion

The Atomic Swap service on Cardano offers a secure, efficient, and decentralized way to perform complex asset exchanges. It's particularly well-suited for trading low-liquidity assets like NFTs, as it minimizes counterparty risk and eliminates the need for a trusted third party. By understanding its underlying technology and algorithmic steps, users can confidently engage in asset swaps on the Cardano network.

### Resources

* [Atomic Swap Tutorial](https://www.youtube.com/watch?v=XdE0aK5ypWM\&embeds\_referring\_euri=https%3A%2F%2Ftwitter.com%2F\&source\_ve\_path=MjM4NTE\&feature=emb\_title\&themeRefresh=1)
* [What is an Atomic Swap](https://blog.chain.link/atomic-swaps/)
* [What is Atomic Swap and How Does It Work?](https://cointelegraph.com/explained/what-is-an-atomic-swap-and-how-does-it-work)
* [Atomic Swaps](https://www.investopedia.com/terms/a/atomic-swaps.asp)
