# Round Table

**Author:** Emir Olgun

**Date:** 31 May 2023

Round Table is an open-source wallet on Cardano blockchain. Unlike any other ordinary wallet on Cardano, Round Table aims at making multisig more accessible to its users. Multisig wallets can be one of the most essential tools for DAOs. DAO treasury management is usually run by a single individual with the wallet credentials. Multisig wallets can distribute the responsibility to a group of people and not a single individiual can override others power. DAOs aim decentralization but normal wallets can not provide the financial decentralization but multisig wallets are a perfect solution to this problem.

### Multisig

In order to understand multisig concept, we need to understand how a normal Cardano wallet works. A Cardano wallet, in most basic terms, is a safe that keeps assets inside. Like a physical safe, accessing the assets inside the wallet, the owner needs a key. When you make a transaction, you create a transaction by the assets in your wallet and then sign this transaction to be processed. Multi-signature or Multisig is a special type of wallet. In order to access the assets in these wallets, you need multiple keys just like those fancy super secure vaults in banks. A multisig wallet needs two or more different keys to sign the same transaction. This significantly increases security and decentralization.

### Features

* Personal Wallet
* Multisig wallet
  * Multisig
  * Timelock
  * Custom multisig logic
  * Nested Policy

#### Personal Wallet

You can use Round Table just like any other Cardano light wallet. Round Table personal wallet only supports 24 words recovery phrases. ADAO has a video tutorial about creating a personal wallet with Round Table.

{% embed url="https://youtu.be/JBJ-VtC6t4I" %}

#### Multisig Wallet

This is where Round Table differs from other Cardano wallets.

**Multisig**

You can add as many signatories as you like for the wallet.

**Timelock**

Timelock is a very useful feature. It is used to limit the timeframe the wallet can be used. You can specify a specific date or even a slot for the wallet to activate and a date or slot for the wallet to lock permanently. Be careful, if the expiry date is passed, all the assets inside the wallet will be irreversibly locked.

**Custom Multisig Policy**

This is a very important feature. With this feature, you can specify how the transaction will be signed. For example, the transaction might require only one of the signatories, at least a number of signatories or all signatories.

**Nested Policy**

With this feature, you can get the customization to the next level. You can give some signatories a specific timeframe to be able to sign transactions, create a requirement of specific signatories and much more. Basically, your imagination is your limit here.

#### Multisig Support

We have tested the multisig wallet with different methods. We have used popular Cardano light wallets, Round Table personal wallet, and cardano-cli wallets. Light wallets are very easy to use with Round Table, the signing process very simple and require no funds from these wallets as the transaction fees are paid by the multisig wallet. These are the light wallets supported by Round Table:

* [nami.md](../../cardano-wallets/nami.md "mention")(no staking)
* [eternl.md](../../cardano-wallets/eternl.md "mention")
* [gerowallet.md](../../cardano-wallets/gerowallet.md "mention")
* [flint-wallet.md](../../cardano-wallets/flint-wallet.md "mention")

Round Table personal wallet works flawlessy with the multisig wallet as expected.

### How to Use Round Table

Using Round Table wallet is quite easy. You can go to it's web app [here](https://roundtable.adaodapp.xyz) and start setting up your wallet. Another way to use it is running its web app on your local machine. How it's done explained in detail [here](https://github.com/ADAOcommunity/round-table). Also you can check this video tutorial about deploying your own Round Table wallet.&#x20;

{% embed url="https://youtu.be/xN9AxiLvqzQ" %}

Using the web app is the most convenient way because setting it up on local machine requires some knowledge about web apps and require installation of various tools. Using the web app for the multisig wallet does not seem to have any security concerns since the signing keys are in your wallet of choice not on Round Table.

Here you can watch this video tutorial about how to use Round Table Wallet.&#x20;

{% embed url="https://youtu.be/j8lKthTURtc" %}

### How DAOs Can Use Round Table

Treasury management is very important for DAOs. It needs to be safe. Not a single individual should be able to in full control of it. The organization might choose how to operate their resources off-chain but without the multisig wallets, these decisions cannot be on-chain in other words, treasury cannot be fully safe. Multisig wallets like Round Table solve the on-chain problem.

DAOs need to be careful using Round Table though. Round Table operates on **Smart Contracts** and by their nature, smart contracts are irreversible. If the organization set wrong timelocks, they might not access their funds until the timeframe begins or if the timeframe ends so soon, they can lose their funds forever. The loss of one of the signatories can also lead to the loss of funds permanently. Organizations should be extremely careful setting multisig wallets up and avoid any mistake to avoid the loss of funds.

**Round Table** is an open-source application. DAOs can customize it to their own interests and integrate it into their own platforms.

### Reviewer's Notes

Round Table is an easy to use wallet but we think it might need some improvements. First one is, there is no option to view transaction history on the app. Platforms like [Cardanoscan](https://cardanoscan.io) are needed to view transaction history of the wallet address. Also, the transaction on signing process can only be accessed via its URL, it would be better to access it on the app. Another possible improvement is, to be able to download the transaction and send it to the signers. The ability to change the signatory information is very convenient. Round Table, in total, is a very easy to use and essential tool for DAOs.

### Summary

Round Table fills a much needed gap in the Cardano Community with its multisig feature. Multisig transactions are usually very complex transactions to build and having a tool that allows multisig conveniently and easily is very important for a lot of DAOs. Multisig wallets hugely improve security of funds and contribute decentralization.

### Additional Links

* [ADAO Discord](https://discord.gg/BGuhdBXQFU)
* [Web App](https://roundtable.adaodapp.xyz)
* [Github](https://github.com/ADAOcommunity/round-table)
* [Twitter](https://twitter.com/ADAOcommunity)

**Author:** Emir Olgun

**Date:** 31 May 2023

Round Table is an open-source wallet on Cardano blockchain. Unlike any other ordinary wallet on Cardano, Round Table aims at making multisig more accessible to its users. Multisig wallets can be one of the most essential tools for DAOs. DAO treasury management is usually run by a single individual with the wallet credentials. Multisig wallets can distribute the responsibility to a group of people and not a single individiual can override others power. DAOs aim decentralization but normal wallets can not provide the financial decentralization but multisig wallets are a perfect solution to this problem.

### Multisig

In order to understand multisig concept, we need to understand how a normal Cardano wallet works. A Cardano wallet, in most basic terms, is a safe that keeps assets inside. Like a physical safe, accessing the assets inside the wallet, the owner needs a key. When you make a transaction, you create a transaction by the assets in your wallet and then sign this transaction to be processed. Multi-signature or Multisig is a special type of wallet. In order to access the assets in these wallets, you need multiple keys just like those fancy super secure vaults in banks. A multisig wallet needs two or more different keys to sign the same transaction. This significantly increases security and decentralization.

### Features

* Personal Wallet
* Multisig wallet
  * Multisig
  * Timelock
  * Custom multisig logic
  * Nested Policy

#### Personal Wallet

You can use Round Table just like any other Cardano light wallet. Round Table personal wallet only supports 24 words recovery phrases. ADAO has a video tutorial about creating a personal wallet with Round Table.

{% embed url="https://youtu.be/JBJ-VtC6t4I" %}

#### Multisig Wallet

This is where Round Table differs from other Cardano wallets.

**Multisig**

You can add as many signatories as you like for the wallet.

**Timelock**

Timelock is a very useful feature. It is used to limit the timeframe the wallet can be used. You can specify a specific date or even a slot for the wallet to activate and a date or slot for the wallet to lock permanently. Be careful, if the expiry date is passed, all the assets inside the wallet will be irreversibly locked.

**Custom Multisig Policy**

This is a very important feature. With this feature, you can specify how the transaction will be signed. For example, the transaction might require only one of the signatories, at least a number of signatories or all signatories.

**Nested Policy**

With this feature, you can get the customization to the next level. You can give some signatories a specific timeframe to be able to sign transactions, create a requirement of specific signatories and much more. Basically, your imagination is your limit here.

#### Multisig Support

We have tested the multisig wallet with different methods. We have used popular Cardano light wallets, Round Table personal wallet, and cardano-cli wallets. Light wallets are very easy to use with Round Table, the signing process very simple and require no funds from these wallets as the transaction fees are paid by the multisig wallet. These are the light wallets supported by Round Table:

* [nami.md](../../cardano-wallets/nami.md "mention")(no staking)
* [eternl.md](../../cardano-wallets/eternl.md "mention")
* [gerowallet.md](../../cardano-wallets/gerowallet.md "mention")
* [flint-wallet.md](../../cardano-wallets/flint-wallet.md "mention")

Round Table personal wallet works flawlessy with the multisig wallet as expected.

### How to Use Round Table

Using Round Table wallet is quite easy. You can go to it's web app [here](https://roundtable.adaodapp.xyz) and start setting up your wallet. Another way to use it is running its web app on your local machine. How it's done explained in detail [here](https://github.com/ADAOcommunity/round-table). Also you can check this video tutorial about deploying your own Round Table wallet.&#x20;

{% embed url="https://youtu.be/xN9AxiLvqzQ" %}

Using the web app is the most convenient way because setting it up on local machine requires some knowledge about web apps and require installation of various tools. Using the web app for the multisig wallet does not seem to have any security concerns since the signing keys are in your wallet of choice not on Round Table.

Here you can watch this video tutorial about how to use Round Table Wallet.&#x20;

{% embed url="https://youtu.be/j8lKthTURtc" %}

### How DAOs Can Use Round Table

Treasury management is very important for DAOs. It needs to be safe. Not a single individual should be able to in full control of it. The organization might choose how to operate their resources off-chain but without the multisig wallets, these decisions cannot be on-chain in other words, treasury cannot be fully safe. Multisig wallets like Round Table solve the on-chain problem.

DAOs need to be careful using Round Table though. Round Table operates on **Smart Contracts** and by their nature, smart contracts are irreversible. If the organization set wrong timelocks, they might not access their funds until the timeframe begins or if the timeframe ends so soon, they can lose their funds forever. The loss of one of the signatories can also lead to the loss of funds permanently. Organizations should be extremely careful setting multisig wallets up and avoid any mistake to avoid the loss of funds.

**Round Table** is an open-source application. DAOs can customize it to their own interests and integrate it into their own platforms.

### Reviewer's Notes

Round Table is an easy to use wallet but we think it might need some improvements. First one is, there is no option to view transaction history on the app. Platforms like [Cardanoscan](https://cardanoscan.io) are needed to view transaction history of the wallet address. Also, the transaction on signing process can only be accessed via its URL, it would be better to access it on the app. Another possible improvement is, to be able to download the transaction and send it to the signers. The ability to change the signatory information is very convenient. Round Table, in total, is a very easy to use and essential tool for DAOs.

### Summary

Round Table fills a much needed gap in the Cardano Community with its multisig feature. Multisig transactions are usually very complex transactions to build and having a tool that allows multisig conveniently and easily is very important for a lot of DAOs. Multisig wallets hugely improve security of funds and contribute decentralization.

### Additional Links

* [ADAO Discord](https://discord.gg/BGuhdBXQFU)
* [Web App](https://roundtable.adaodapp.xyz)
* [Github](https://github.com/ADAOcommunity/round-table)
* [Twitter](https://twitter.com/ADAOcommunity)
