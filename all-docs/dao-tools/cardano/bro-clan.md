# Bro Clan

**Author:** Emir Olgun

**Date:** 14 June 2023

Bro Clan is an open-source multisig wallet on Cardano Blockchain. Even if it is called a "wallet", the multisig wallets and normal Cardano wallets are profoundly different and their use cases have almost nothing in common. A multisig wallet opens the possibility of keeping assets in a more secure and, most importantly, a true decentralized safe. A multisig wallet is more like a safe in a bank. These "safes" are essential for DAOs because keeping DAO funds in a normal Cardano wallet would give a single individual a tremendous power and it is against the philophy of decentralization.

Bro Clan wallet currently is in beta test. It supports Mainnet, Pre Production and Preview Testnets. It allows the user to configure the provider. The provides are Blockfrost, BroClan and Kupmios(Kupo and Opmios). The Kupmios choice turns Bro Clan wallet into a full-node wallet.

### Multisig

In order to understand multisig concept, we need to understand how a normal Cardano wallet works. A Cardano wallet, in most basic terms, is a safe that keeps assets inside. Like a physical safe, accessing the assets inside the wallet, the owner needs a key. When you make a transaction, you create a transaction by the assets in your wallet and then sign this transaction to be processed. Multi-signature or Multisig is a special type of wallet. In order to access the assets in these wallets, you need multiple keys very similar to vault in banks. A multisig wallet needs two or more different keys to sign the same transaction. This significantly increases security and decentralization. Also, multisig keys can have time limit. For example, some keys would only work until a specific date or they can be activated after a specific date.

### Wallet

**Multisig**

You can add as many signatories as you like for the wallet.

**Timelock**

Timelock is a very useful feature. It is used to limit the timeframe the wallet can be used. You can specify a specific date or even a slot for the wallet to activate and a date or slot for the wallet to lock permanently. Be careful, if the expiry date is passed, all the assets inside the wallet will be irreversibly locked.

**Custom Multisig Policy**

This is a very important feature. With this feature, you can specify how the transaction will be signed. For example, the transaction might require only one of the signatories, at least a number of signatories or all signatories.

**Nested Policy**

With this feature, you can get the customization to the next level. You can give some signatories a specific timeframe to be able to sign transactions, create a requirement of specific signatories and much more. Basically, your imagination is your limit here. It is a little hard to use this feature, be careful when setting it up.

#### Multisig Support

We have tested the multisig wallet with different light wallets. Light wallets are very easy to use with Bro Clan, the signing process very simple and require no funds from these wallets as the transaction fees are paid by the multisig wallet.

### Reviewer's Notes

Creating the signing logic is a little complicated. \[Round Table] wallet definately does it better. Bro Clan supporting downloading transaction information is useful, but sharing the transaction with other people is difficult. It seems all participants will have to load the wallet and sign. Having a transaction URL to share would be more convenient. Also, we tried to import the transaction on some wallets and failed. Overall, Bro Clan is a wallet with significant potential. We will definately be following it when it becomes live on Cardano Mainnet.

### Additional Links

* [Website](https://broclan.io)
* [Web-app](https://alpha.broclan.io)
* [Github](https://github.com/leo42/BroClanWallet)
* [Twitter](https://twitter.com/BroClanWallet)
