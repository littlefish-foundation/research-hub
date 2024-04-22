# Wanchain

**Author:** Emir Olgun

**Date:** 29 September 2023

### Introduction

Wanchain is a cross-chain bridge. In the most basic terms, Wanchain transfers assets from one blockchain to another.

Wanchain is a layer 1 Blockchain that uses Proof of Stake and a blockchain interoperability solution. Wanchain is EVM compatible. Wanchain is uses a Proof of Stake consensus called [**Galaxy Consensus**](https://docs.wanchain.org/technology/galaxy-consensus) which is a continuation of Cardano’s Ouroboros Protocol. Wanchain currently connects 28 different Blockchains including Cardano and 45 assets.

### How Does It Work

Wanchain's architecture is designed to serve as a robust framework for a decentralized financial ecosystem. At its core, it features a distributed ledger that is compatible with smart contract virtual machines, similar to Ethereum. The native coin of Wanchain, known as WAN, serves as the fuel for transactions and smart contract execution.

The consensus mechanism initially employed by Wanchain was Proof-of-Stake (PoS), but it has transitioned to a Delegated Proof-of-Stake (DPoS) system for better scalability and performance. This consensus mechanism allows for quicker transaction validations and a more secure network.

Wanchain also supports intra-chain transactions, which are transactions within the Wanchain network. However, its unique selling point is its capability for cross-chain integration and transactions. This feature allows Wanchain to connect with other blockchains, be it public, private, or consortium chains, and facilitate asset transfers between them.

#### Cross-Chain Communication Protocol

The Cross-Chain Communication Protocol is the backbone of Wanchain's interoperability feature. It consists of functional modules that handle the locking and unlocking of assets as they move across different blockchains. The protocol also outlines the data transmission process, which ensures that transactions are securely and accurately relayed between the participating blockchains.

Storeman nodes play a crucial role in this protocol. They act as the intermediaries responsible for locking assets in the originating blockchain and minting corresponding proxy assets on the Wanchain network. This ensures that the asset's value is preserved as it crosses from one chain to another.

#### Storemen Nodes

Wanchain utilizes Storemen nodes in order to process cross-chain transactions. Storemen nodes work together to perform cross chain transactions without revealing the private keys of the accounts involved. Node operators must put up collateral which covers the value of transactions they process.

#### Galaxy Consensus

Wanchain employs Galaxy Consensus to ensure a secure and efficient network. Galaxy Consensus is one such technology, which is part of the DPoS system. It ensures that only verified nodes participate in the validation of transactions, thereby enhancing network security.

Incentive mechanisms are also in place for both verification and general nodes. These incentives encourage active participation in the network, which in turn increases network security and efficiency. The system is designed to be fully decentralized, with no need for a trusted third-party, thanks to cryptography-based security guarantees.

Galaxy consensus is explained in more detail later in this document.

#### Locked Account Generation Scheme

The Locked Account Generation Scheme is a pivotal technology that enables the secure transfer of assets across chains. When an asset is to be transferred, it is first locked in the originating blockchain. A corresponding proxy asset is then minted on the Wanchain network. This locked account is generated through a secure cryptographic scheme, ensuring that the original asset can only be unlocked by the rightful owner.

#### Smart Contract Token Transaction Anonymity

Privacy is a significant concern in any financial transaction. Wanchain addresses this by incorporating smart contract token transaction anonymity features. It employs a one-time account system and a ring signature scheme to provide optional transaction privacy.

The one-time account system ensures that each transaction is linked to a unique account, making it difficult to trace back to the original sender. The ring signature scheme adds another layer of anonymity by allowing the sender to hide among a group of users, making it nearly impossible to identify the actual sender.

### Understanding Galaxy Consensus: The Engine Behind Wanchain's Decentralization

Galaxy Consensus is Wanchain's unique consensus algorithm designed to enhance the blockchain's security, scalability, and efficiency. It is a sophisticated mechanism that combines elements of randomness, stake rate, and cryptographic proof to ensure a fair and secure network. Here's how it works:

#### Epochs and EL Groups

The Galaxy Consensus operates in epochs, which are time periods during which a group of nodes, known as the EL group, is responsible for block production. The EL group is a multiset, meaning a single node may appear in it more than once. The nodes in this group are selected based on their stake rate, ensuring that those with higher stakes have a better chance of being chosen.

#### Slot Leader Selection

Within each epoch, the actual block producer for each slot (a smaller time unit within an epoch) needs to be determined. This is where the slot leader selection process comes into play. The algorithm uses a combination of the current random number, the epoch number, and the slot number, hashes them together, and then takes the modulus of the number of EL group nodes to pick the slot leader.

For example, if the hash value is 2019 and there are 50 nodes in the EL group, the modulus result will be 19. The EL node with the number 19 in the order from the previous sorting step is then selected as the valid block producer, also known as the slot leader.

#### Fairness, Verifiability, and Anonymity

The slot leader selection process is designed to be fair, verifiable, and anonymous. It is fair because it considers the stake rate when selecting the EL group nodes, ensuring that the choice of the block producer is made in accordance with the ratio of stake held by consensus participants.

It is verifiable because the valid block producer must provide proof of its validity when proposing a block. This proof is publicly verifiable, guaranteeing the legitimacy of the block.

Lastly, it is anonymous because the secret message array used in the selection of the slot leader is shared only within the EL group. Other nodes have no knowledge of it, ensuring the anonymity of the selection process.

#### ULS Algorithm

The underlying algorithm for this process is known as the ULS (Universal Leader Selection) algorithm. It is a design that fully considers fairness, verifiability, and anonymity. The ULS algorithm plays a crucial role in ensuring the safety and liveness of the Wanchain blockchain.

In summary, Galaxy Consensus is a robust and intricate system that aims to solve many of the challenges faced by traditional consensus algorithms. By incorporating elements of randomness, stake-based selection, and cryptographic proof, it offers a balanced approach to block production that is both secure and efficient.

### Wanchain-Cardano Bridge: A Step Towards Blockchain Interoperability

The Wanchain-Cardano bridge signifies a pivotal moment in the realm of blockchain interoperability. While specific technical details are limited, the bridge aims to connect Cardano, a blockchain platform with a focus on sustainability and peer-reviewed research, with Wanchain's existing cross-chain infrastructure. This move brings Wanchain's vision of a fully interoperable blockchain ecosystem closer to reality.

#### The Role of Storeman Nodes

As explained before Wanchain's cross-chain bridges rely on a set of decentralized nodes known as Storeman nodes. These nodes play a crucial role in facilitating asset transfers between different blockchains. In the context of the Wanchain-Cardano bridge, Storeman nodes are responsible for locking assets like ADA on the Cardano blockchain and minting corresponding proxy assets on the Wanchain network. This mechanism ensures the secure and seamless transfer of value between the two ecosystems.

#### Smart Contracts and Decentralized Applications

Both Wanchain and Cardano have robust smart contract capabilities, which opens the door for more than just simple asset transfers. The bridge could potentially support complex decentralized applications that leverage smart contracts from both ecosystems. This would allow developers and users to engage in more intricate interactions, thereby enriching both the Wanchain and Cardano platforms.

#### Community Involvement

The bridge also aims to foster a community of developers, users, and ambassadors who are interested in blockchain interoperability. By connecting Cardano to Wanchain's existing network of over 20 public blockchains, the bridge not only enhances the utility of both platforms but also creates opportunities for community members to collaborate on cross-chain solutions.

### User Experience

Wanchain is very easy to use. Wanchain supports multiple wallets including its own wallet. WanWallet can be used on Windows, Mac and Linux computers and iOS and Android Mobile Devices. Also users can use Metamask wallet with Wanchain. To use it with Cardano, users can use Nami wallet.

Cross-chain transactions can be costly depending on the chains the user chooses. For example, sending ADA from Cardano to Ethereum costs 50 ADA per transaction or sending BTC from Bitcoin to Ethereum can cost between 0.0005 BTC to 0.5 BTC($13,679). On the other hand, transactions from a blockchain to Wanchain is much cheaper or free. For example sending ADA from Cardano to Wanchain is free but sending ADA from Wanchain to Cardano costs 7.5 WAN($1.38).

The cross-chain transactions usually take around 30 minutes which is impressive compared to other bridge applications. Some bridges can take days to complete transactions.

### Conclusion

Wanchain is an impressive project. The Wanchain cross-chain bridge opens new possibilities for a variety of blockchains and the tools on them. Users can transfer their assets easily to other blockchains to use different services like DeFi applications with Wanchain. The Wanchain-Cardano bridge is a significant milestone in the ongoing efforts to achieve full blockchain interoperability. By leveraging Wanchain's proven cross-chain mechanisms and Cardano's advanced blockchain technology, the bridge promises to offer a range of functionalities that go beyond mere asset transfers. While the specifics are yet to be fully disclosed, the bridge is poised to be a game-changer in how blockchains interact and share value.

### Resources

* [Wanchain Website](https://www.wanchain.org)
