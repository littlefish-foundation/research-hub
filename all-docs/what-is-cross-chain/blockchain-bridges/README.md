# Blockchain Bridges

**Author:** _Emir Olgun_

**Date:** _1 July 2023_

A blockchain bridge is a way to transfer assets between different blockchains. This is a very difficult task because most blockchain networks are not compatible and they do not support each other assets. For example, some blockchains support account model and some support utxo model. Their protocols are different, and smart contracts are different. A way to overcome this issue is to wrap a token in another blockchain.

#### Wrapped Token

A wrapped token is like a collateral or a stable coin. It is a token that is pegged to a token in another blockchain. For example, a WBTC or Wrapped Bitcoin is used on Ethereum blockchain and it has the exact same value of Bitcoin. When an asset is wrapped, the original token is either locked in a smart contract or kept in custody by the bridge, so the number of assets in circulation stays the same. When the user wants their original tokens back, the wrapped assets will go back to the bridge pool or be burned and original assets will be released.

Simply, a wrapped token is like a human going underwater. A human naturally needs breathable air to stay alive and he/she wrappes themselves in a suit supplying breathable air. A Bitcoin cannot exist in Ethereum blockchain so we wrap it as an Ethereum token.

#### NFT Bridge

Some bridges also support locking the originals in case the user wants to reclaim them in the future.

Another method is burning the original asset. Unlike locking original tokens in a smart contract and minting wrapped tokens, when transferring an NFT from a chain to another, the original NFT is usually burned and an NFT with exact same traits is minted in destination chain.

There are two dimensions to bridges. One dimension is about the centralization of them and the other dimension is about the way they operate for example, direct bridges or side-chain bridges. There are two types of bridges, centralized and decentralized. Also known as trust-based and trustless.

### Centralized Bridges

These bridges are operated by third party organizations. These organizations are trusted to respect the custody of funds by the users. When using Centralized trust-based bridges, the user gives up control of their assets to the third party. Centralized bridges are as safe as the third party that operates it can be. These bridges usually have pools of wrapped assets on both blockchains to conduct transactions in a short time. The transaction time also depend on how many people use the bridge and how balanced is the traffic between the blockchains. If a pool on one side is empty, the users will have to wait for another user to release their wrapped tokens and these waiting times can be as high as days.

In 2022, hackers infiltrated Axie Infinity's systems by social engineering and got access to more than half of validator keys. By controlling the majority of validators, they sent all the native assets in custody resulting 620 million USD heist.

**Pros**

* Cheap transactions fees
* Fast transactions

**Cons**

* Prone to attacks
* Requires off-chain trust

**Risks**

There is only trust between the centralized bridge and the user. If the bridge operators decide to steal user's funds, there is no way to prevent this. If the operator is compromised, the funds in custody can be stolen. On some bridge attacks, the operator

### Decentralized Bridges

Decentralized bridges rely entirely on smart contracts. When a user go from a chain to another chain, their original assets are locked in a smart contract and issue wrapped tokens to the user. The smart contract can only be accessed by the wrapped tokens and the user who minted them. When the user wants to retrieve their originals assets, the wrapped assets are burned. The transaction fees on decentralized bridges are usually higher than centralized bridges since they also have to pay for the minting process of wrapped assets. These decentralized bridges are as safe as the chains they bridge and their smart contracts.

**Pros**

* Safer than centralized bridges in theory
* Decentralized

**Cons**

* No customer support
* High transaction fees
* Slow Transactions

**Risks**

The smart contracts used for blockchain bridges are more complex and there is a risk of bugs on smart contrac codes which can cause the loss of funds. Since there is not actual backer of these bridges, the chance to save lost funds are almost none.

#### Risks of Using Bridges

Blockchain bridges are more susceptible to malicious attacks. In case of a 51% attack on a blockchain, native assets on a crypto wallet is mostly safe since the malicious attacks will be rejected by the nodes since they do not follow blockchain protocols. In case of a bridge, if the attackers buy the wrapped assets and revert the transaction, the bridge validator on the other chain will still release the wrapped assets to the attackers and there will be more wrapped assets than the actual assets. The bridge users will not be able to go back to their original chain in this situation or the value of their wrapped assets will be significantly lower than the original assets.

### Cardano Bridges

Currently there are not many bridge options for Cardano. Microchain and Milkomeda are current bridges that connect Cardano to other blockchains like EVM based chains. These both bridges are **Centralized** bridges. There is also Wanchain. Wanchain is working with IOHK to make Cardano interoperable with other blockchains and they are online on Cardano Testnet currently.

### Resources

* [Ethereum official Website](https://ethereum.org/en/bridges/)
* [Coindesk](https://www.coindesk.com/learn/what-are-blockchain-bridges-and-how-do-they-work/)
* [Wanchain](https://medium.com/wanchain-foundation/update-cardano-cross-chain-bridges-and-other-interoperability-solutions-f8e8b7e2e77)
* [IOHK on Wanchain](https://iohk.io/en/blog/posts/2022/07/08/bridges-and-sidechains-wanchain-making-cardano-interoperable/)
* [Axie Infinity Hack](https://www.bleepingcomputer.com/news/security/hackers-stole-620-million-from-axie-infinity-via-fake-job-interviews/)
* [Vitalik Buterin on Safety of Bridges](https://old.reddit.com/r/ethereum/comments/rwojtk/ama\_we\_are\_the\_efs\_research\_team\_pt\_7\_07\_january/hrngyk8/)
* [Chainlink](https://chain.link/education-hub/cross-chain-bridge)
* [Blockchain Bridges Youtube Video](https://youtu.be/nT26cIz8HjI)
* [Bridge Hacks](https://limechain.tech/blog/biggest-blockchain-bridge-hacks-2022/)
