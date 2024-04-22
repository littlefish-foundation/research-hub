# Voteaire

**Author:** _Donald_

**Date:** _19 Apr 2023_

## Voteaire Protocol

### Democratizing Governance Through Blockchain: Introducing Voteaire

Democratizing governance through blockchain technology has become an exciting endeavor, championing the principles of decentralization and transparency. Enter Voteaire, a user-friendly platform designed to facilitate the creation and operation of on-chain voting systems within the Cardano ecosystem. As an embodiment of these principles, it is transforming traditional governance models, highlighting transparency, decentralization, and accessibility for all, while eliminating the need for central authorities.

### Decentralization and Transparency

By employing blockchain's decentralization feature, Voteaire helps protect the voting process against undue influence or manipulation, distributing decision-making power across a vast network of participants. Moreover, the platform ensures accountability and openness by permanently recording all transactions, including proposals and votes, on the blockchain. Every piece of information, including data specifications, are openly accessible in a public, open-source repository for verification purposes.

### Redefining On-Chain Voting

Voteaire redefines on-chain voting, leveraging the immutable nature of blockchain technology. Based on the initial concept introduced by SPOCRA for their board of directors' vote, it operates by extending this fundamental principle. The platform employs transaction metadata to permanently store ballot proposals and votes on-chain, with the 'metadata key 1916' as an homage to the year Canadian women first gained suffrage. Anyone with the necessary technical proficiency can probe the blockchain directly to validate the voting results, ensuring transparency and immutability.

### User-Friendliness and Accessibility

In terms of accessibility, Voteaire stands out by prioritizing user-friendliness, enabling even non-technical users to create and participate in proposals effortlessly. By connecting their wallets and submitting a transaction, users can actively engage in community decision-making processes. Voteaire supports three different wallet types: GeroWallet, Eternl, or Nami, with a minimum of 1 ADA to cover transaction fees.

#### Voting Process

For voting, the process starts with the user signing in to Voteaire using a compatible wallet. After signing in, the user views the list of submitted ballots, selects a ballot, reads its description, and chooses their preferred option before submitting their vote. Note that users can only vote for ballots marked as "ACTIVE."

Voteaire offers three types of ballots — SIMPLE, DELEGATED, and POLICYID — each with slightly different voting procedures and weightings. In a SIMPLE ballot, the vote's weight depends on the amount of ADA in the user's wallet at the time of the snapshot. A DELEGATED ballot requires delegation to a specified pool for the vote to count, with the vote's weight depending on the size of the user's delegation to the pool. In a POLICYID ballot, the vote's weight is determined by the number of tokens associated with a specific POLICYID in the user's wallet at the snapshot.

### Security Measures

The platform addresses the so-called "Franken-Address Vulnerability," which could allow a malicious user to manipulate voting results. By requiring votes to be attached to a delegation transaction rather than a standard payment transaction, it ensures that voters cannot misrepresent the amount of funds they control, adding another layer of security to the process.

#### Voting Periods and Conditions

Voteaire employs Cardano epochs to define voting periods, providing flexibility to voters. It uses snapshot dates in the Cardano blockchain ledger to weight the votes for SIMPLE and DELEGATED ballots. For POLICYID ballots, snapshots are directly taken by the platform itself.

Moreover, Voteaire has established essential conditions to ensure vote validity and maintain user delegation status and rewards integrity. It only recognizes the first vote if a user attempts to cast multiple ones, and it requires votes to be part of a delegation transaction. Also, when a vote is cast, Voteaire re-delegates to the same pool the user is currently affiliated with, avoiding any negative impacts on delegation status or rewards.

### Conclusion

In conclusion, Voteaire is leading the blockchain-powered shift toward more democratic governance models. By utilizing blockchain's transparency and immutability, it offers an innovative platform for voting, emphasizing the significance of each vote while ensuring users maintain control over their delegation status and rewards. As the platform evolves, it promises to become an indispensable tool for those aiming to shape a more equitable future through the power of blockchain technology.

#### Additional information

Relevant Links:

[**Official Voteaire Website**](https://voteaire.io/)

[**Official Voteaire Github Account**](https://github.com/voteaire/)
