# Blockchain Oracles

**Author:** _Emir Olgun_

**Date:** 5 October 2023

### Introduction

Blockchains, by their nature, are isolated from the outside world. This isolation is an advantage in most cases such as security and predictability. This isolation also has some disadvantages. For example, interchain operations require different blockchains to communicate or services like DeFi need to access off-chain market data. To address this issue we have blockchain oracles. An oracle is a bridge between a blockchain and the outside world where this outside world can be another blockchain. It provides real-world data to smart contracts on the blockchain, enabling them to make decisions based on external information like stock prices, weather, or sports match scores.

### Types of Oracles

On the top level, there are two types of oracles which are **Software Oracles** and **Hardware Oracles**. The difference between them is the way they interact with the outside world.

#### Software Oracles

Software oracles are programs that connect smart contracts to online resources. They can pull informations like stock prices, weather forecats, or currency exchange rates from various online sources, usually through APIs or they can update online resources according to the outcome of smart contracts.

#### Hardware Oracles

Hardware oracles connect blockchains to the actual real world. They can collect data from physical devices, such as sensors or RFID tags, and provide it to smart contracts on a blockchain. They can also interact with real world machines according to the information on blockchain, for example, a hardware oracle can unlock a rental car when a customer pays for the car on blockchain.

Oracles can also be categorized for the way they operate or their purpose. These are some important types of oracles:

* Input Oracles
* Output Oracles
* Cross-Chain Oracles
* Compute-Enabled Oracles
* Human Oracles

#### Input Oracles

Input oracles are one of the most popular oracles. They fetch data from the off-chain sources and deliver them onto a blockchain network to be used by smart contracts.

#### Output Oracles

The output oracles are the exact opposite of input oracles. These oracles deliver the on-chain data from smart contracts to the off-chain sources. The example mentioned before of a rental car unlocking is an example of an output oracle.

#### Cross-Chain Oracles

Cross chain oracles deliver on-chain information from one chain to a completely different blockchain. They are very important because they are currently the only reliable way to conduct inter-chain operations.

#### Compute-Enabled Oracles

Compute-Enabled Oracles allow smart contracts to use secure off-chain computation for services that are impractiocal to do on-chain due to technical or other constraints.

#### Human Oracles

Human oracles are individuals who manually provide data to smart contracts on a blockchain. They are often used in decentralized prediction markets or voting systems where human judgment or expertise is required. While they add the element of human insight, they also introduce the risk of human error or manipulation.

### How Oracles Work

Oracles can be seperated into two categories based on how they work, **Centralized Oracles** and **Decentralized Oracles**. For anyone who is familiar with the blockchain environment, decentralized oracles might seem to be the better solution and it usually is. Let's take a look at how they work.

#### Centralized Oracles

Centralized oracles provide a single data provider for the on-chain contracts with a set of security features. These oracles are easier to set up and require not much resources to operate. They are as accurate as the reputation of the entity behind it. They always have the risk of single point of failure. They can be vulnerable to common issues centralized etities face like DDOS attacks, downtimes, hacks, accidental incompetence, and malicious intent of the entity.

#### Decentralized Oracles

Decentralized oracles basically use multiple data providers for on-chain smart contracts. Decentralized oracles operate a network of oracles to provide and verify the data provided. There are variety of mechanisms to verify accuracy and incentivize nodes, one popular mechanism is **SchellingCoin Mechanism**. Running decentralized oracles can be costly and slow.

#### SchellingCoin Mechanism

The SchellingCoin mechanism is a game-theoretic model used to incentivize honest reporting in decentralized systems, like oracles. Participants are rewarded for submitting data that aligns with the majority consensus. The idea is that truthful reporting is the most rational strategy because individuals expect others to report truthfully to maximize their own rewards.

* Participants independently and simultaneously report a value (e.g., the current temperature).
* The reports are collected and sorted.
* Rewards are distributed to those whose reports are close to the median or mean, assuming that the majority are honest. **Advantages:**
* Encourages honest reporting.
* Reduces the impact of outliers or malicious actors. Disadvantages:
* Susceptible to "51% attacks" if a majority collude to report false information.
* May not work well for subjective or complex data. Given your interest in building reliable systems, you might find the SchellingCoin mechanism interesting as a way to ensure data integrity in decentralized networks. It's a method to align individual incentives with collective honesty.

### Conclusion

Blockchain oracles are essential for connecting smart contracts to real-world data, making them more versatile and useful across industries like finance and supply chain management. They enhance the trustworthiness of blockchain applications and facilitate interoperability between different networks. However, it's important to note that oracles can introduce risks, such as a single point of failure in centralized setups or potential data inaccuracies. These risks need to be carefully managed to maintain the integrity and security of the blockchain system.

### Resources

* [Blockchain Oracles](https://chain.link/education/blockchain-oracles)
* [Blockchain Oracle Types](https://www.geeksforgeeks.org/blockchain-oracle-types-uses-and-how-it-works/)
* [Guide to Oracles](https://research.aimultiple.com/blockchain-oracle/)
* [What is a Blockchain Oracle](https://www.ledger.com/academy/topics/blockchain/what-is-a-blockchain-oracle)
