# DAO Case Studies

### Introduction

#### Background

Decentralized Autonomous Organizations (DAOs) have emerged as a revolutionary model for community-led governance and decision-making in the blockchain space. As DAOs proliferate across various blockchain networks, understanding the tools and workflows that enable their functionality becomes increasingly important. This is particularly true for governance, decentralized finance (DeFi), and treasury management—key pillars that define the effectiveness and sustainability of a DAO.

#### Objective

The primary aim of this research report is to provide an in-depth analysis of the tools and workflows employed by active DAOs on other blockchain networks, specifically Ethereum and Bitcoin. By focusing on governance mechanisms, DeFi applications, and treasury management strategies, we aim to glean insights that could be beneficial for DAOs operating on the Cardano network, including our own.

#### Scope

This report covers an analysis of 10 DAOs selected based on their activity, user base, and token traffic. Each DAO will be examined for the tools they use in governance, DeFi, and treasury management, along with a brief overview of their workflows in these areas.

Here are the DAOs we have focused on:

* [uniswap-dao.md](uniswap-dao.md "mention")
* [decentraland-dao.md](decentraland-dao.md "mention")
* [compound-dao.md](compound-dao.md "mention")
* [bankless-dao.md](bankless-dao.md "mention")
* [makerdao.md](makerdao.md "mention")
* [aave-dao.md](aave-dao.md "mention")
* [lido-dao.md](lido-dao.md "mention")
* [illuvium-dao-research.md](illuvium-dao-research.md "mention")
* [1inch-dao.md](1inch-dao.md "mention")
* [balancer-dao-research.md](balancer-dao-research.md "mention")

#### Significance

The findings from this research will not only serve as a knowledge base but also guide the strategic planning and tool selection for DAOs on the Cardano network. DAOs on some blockchains like Ethereum have a longer history than Cardano DAOs and they have encountered problems Cardano DAOs have yet to experience. Understanding the best practices and effective tools in these areas will enable us to optimize our own operations and contribute to the broader Cardano DAO ecosystem.

### DAO Selection Criteria

To ensure the relevance and applicability of our research findings, we employed a rigorous selection process to identify DAOs for study. The DAOs were chosen based on the following criteria:

#### Activity Level

* We looked for DAOs that have shown consistent activity in terms of proposals, voting, and community engagement. High activity levels often indicate a well-functioning governance system and a committed user base.

#### User Base

* DAOs with a large and diverse user base were prioritized. A broad user base often suggests a more robust ecosystem and provides a wider range of perspectives on governance and treasury management.

#### Token Traffic

* We considered the volume and frequency of token transactions within the DAO. High token traffic is usually a sign of active financial engagement, making the DAO relevant for studying decentralized finance tools and treasury management.

### Tools Used By DAOs.

We have categorized the tools we found into three categories which are **Governance, Decentralized Finance**, and **Treasury Management**.&#x20;

#### Governance Tools

1. **Llama**:&#x20;

Llama is a fullstack platform for onchain governance and access control. Securely take action using onchain policies and custom execution strategies.

**Users**:

* Uniswap

2. **Snapshot**:

A gasless, off-chain governance tool for creating and voting on proposals.

**Users:**

* Uniswap
* Bankless
* Aave
* Lido
* Illuvium
* 1Inch
* Balancer

3. **Aragon**:

Provides a framework for creating and managing DAOs, including governance and voting mechanisms.

**Users:**

* Decentraland
* Lido

4. **Boardroom**:

A governance management platform that allows for proposal creation, voting, and delegation.

**Users:**

* Decentraland
* Compound

#### Decentralized Finance Tools

5. **Spark Protocol**:

Spark is a decentralized non-custodial liquidity market protocol where users can participate as suppliers or borrowers.

**Users:**

* MakerDAO

#### Treasury Management Tools

6. **Parcel**:

A treasury management tool designed for DAOs, offering features like budgeting and financial reporting.

**Users:**

* Compound

7. **Tally**:

A governance and voting platform that also provides treasury management features.

**Users:**

* Compound

#### Infrastructure Tools

8. **Tenderly:**

A monitoring, debugging, and analytics platform for Ethereum smart contracts.

**Users:**

* Aave

9. **Chainlink**:

A decentralized oracle network, often used to provide real-world data to smart contracts.

**Users:**

* MakerDAO

10. **OpenZeppelin**:

A library for secure smart contract development, often used in DeFi projects.

**Users:**

* Compound

#### Additional Tools

11. **Kleoverse**:

Kleoverse is a DAO tooling app and credentialing platform that maximizes the efficiency of developers, community contributors, and DAOs.

**Users:**

* Bankless

### Findings

Our research into 10 DAOs across various blockchain networks has revealed a diverse set of tools and workflows employed. We found that DAOs often use a combination of specialized tools to meet their unique needs and objectives.

#### Governance

In the realm of governance, we observed a focus on postponing on-chain votes as much as possible. This is expected since on some blockchains like Ethereum, gas fees can be very high. DAOs often use a three step votes. These steps are discussion, off-chain vote, and the on-chain votes. The disssuions are done on Discord servers or discussion forums. Off-chain votes are conducted to eliminate unpopular proposals having a cost on DAO.

DAOs often use tools for their governance. As can be seen above, Snapshot is the most popular tool used by the DAOs since it offers off-chain voting capability.

#### Infrastructure

For Infrastructure, smart contract development and oracle solutions are found. Developing smart contracts and oracles are extremely difficult and vulnerable tasks. It is expected to see DAOs use other sources to implement their own infrastructures. Most governance tools also provide the necessary sets of smart contracts to the DAOs.

#### Treasury Management

When it comes to treasury management, analytics and automation features are highly valued. DAOs are leveraging these tools to gain better insights into their financial health and to automate routine treasury tasks. In addition to the tools we found, lots of DAOs use their on multisig wallets for their treasury managements.

### Usage of tools by each DAO



<table><thead><tr><th width="154">DAO</th><th width="105">Tool 1</th><th width="141">Tool 2</th><th width="123">Tool 3</th><th>Tool 4</th></tr></thead><tbody><tr><td>Decentraland</td><td>Aragon</td><td>Boardroom</td><td></td><td></td></tr><tr><td>Compound</td><td>Parcel</td><td>OpenZeppelin</td><td>Boardroom</td><td>Tally</td></tr><tr><td>Bankless</td><td>Snapshot</td><td>Boardroom</td><td>Kleoverse</td><td></td></tr><tr><td>Maker</td><td>Chainlink</td><td>Spark Protocol</td><td></td><td></td></tr><tr><td>Aave</td><td>Snapshot</td><td>Tenderly</td><td></td><td></td></tr><tr><td>Lido</td><td>Snapshot</td><td>Aragon</td><td></td><td></td></tr><tr><td>Illuvium</td><td>Snapshot</td><td></td><td></td><td></td></tr><tr><td>1inch</td><td>Snapshot</td><td></td><td></td><td></td></tr><tr><td>Balancer</td><td>Snapshot</td><td></td><td></td><td></td></tr></tbody></table>

