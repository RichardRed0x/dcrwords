dcrwords

## Decred Glossary

**Distributed ledger:** A ledger recording transactions between addresses, every node on the network holds a copy of the same ledger, commonly referred to as the "blockchain".

**Consensus rules:** There must be consensus between every node on the network about what the rules are, e.g. who can make new blocks, what can blocks contain and how should they be structured.

**Protocol rules:** See consensus rules.

**Block:** Transactions are written to the distributed ledger in blocks. Decred's difficulty adjusts such that new blocks are found every five minutes on average.

Wallet: 

**Seed:** A series of 33 words that is used to generate the private key for a wallet. Anyone who has the seed for a wallet can spend any DCR it holds.

**Private passphrase:** wallet.db files encrypted with a private passphrase cannot be used without that passphrase.

**Account:** A single Decred wallet can be used to operate multiple independent accounts (i.e. DCR transfers between accounts are on-chain transactions).

Address:

Private key:

Public key:

Extended public key:

Watch-only:

Proof-of-Stake voting:

**[Hybrid PoW/PoS:](https://docs.decred.org/research/hybrid-design/)** 

Block reward:

**Ticket**: Decred holders can time-lock DCR in exchange for tickets. Tickets grant their holder votes, and it is through ticket voting that major governance decisions are made. The DCR locked to buy a ticket is unlocked after that ticket is called to vote on-chain (averages around one month, maximum around 4 months), along with a reward. Around 0.5% of tickets are not called before they expire, in this case the DCR is un-locked but  no reward granted.

**[Consensus rules voting](https://docs.decred.org/getting-started/user-guides/agenda-voting/)** : Changes to Decred's consensus rules can only be made through an on-chain voting process which lasts for around one month, the change is made if at least 75% of votes are in favor. 

**Agenda voting:** see consensus rules voting

**Quorum:** A minimum level of participation required in order for a decision-making process to produce a valid outcome. Changes to the consensus rules require at least 10% of votes to be for or against the change in order to be valid.

**Rule change proposal:** Consensus rules votes concern a specific rule change proposal - which must be implemented in latent code within the software that the network's nodes are running. If the proposal passes, the latent code activates one month later.

**[Decred change proposal (DCP)](https://github.com/decred/dcps):**  Design document that describes potential protocol or consensus changes to Decred. DCPs primarily serve for documentation, fostering cross-implementation compatibility, and helping ensure proper engineering rigor is followed.

Stake version interval: 

Rule change interval:

**[Ticket pool](https://docs.decred.org/mining/proof-of-stake/):** Ticket pool refers to live tickets that are available to be called. The target size for the ticket pool is 40,960.

**Ticket price:** The ticket price is the amount of DCR one must time-lock in order to buy a ticket. The ticket price goes up or down depending on whether the ticket pool holds more or less tickets than the target 40,960. The algorithm for setting the ticket price was changed by [DCP-0001](https://github.com/decred/dcps/blob/master/dcp-0001/dcp-0001.mediawiki), the first consensus rules change to be adopted after an on-chain vote. 

**Ticket-splitting:** Refers to buying part of a ticket, which is possible without giving up custody of one's DCR when coordinating with other parties who will buy the other parts of a ticket. Ticket-splitting is currently coordinated through the #ticket-splitting channel.

**Ticket status terms**

​	**Unmined ticket:**  Immediately after a ticket is bought it is unmined until the transaction is included in a block.

​	**Immature ticket:** Once tickets are mined they are immature for 256 blocks (about 20 hours) and cannot be called to vote until after this period elapses.

​	**Live ticket:** Tickets that are waiting to be called.

​	**Voted ticket:** Tickets that have been called and responded with votes, once the ticket has voted the DCR locked to buy it becomes spendable after 256 blocks.

​	**Missed ticket:** Tickets that have been called but did not respond - these can be revoked, but do not grant a reward.

​	**Expired ticket:** Tickets that reached the end of their window without being called to vote - these can be revoked, but do not grant a reward.

​	**Revoked ticket:** When a ticket (that was missed or expired) is revoked, the DCR used to buy it becomes spendable again.

**Block voting:** In each block five tickets are called to vote, in addition to votes on any open consensus rules change proposals each ticket votes to approve or reject the regular transaction tree of the previous block. If a majority of voting tickets vote No, the regular transaction tree of the previous block is rejected and those transactions return to the mempool.

**[Regular transaction tree](https://www.reddit.com/r/decred/comments/66j4l4/decred_proof_of_stake_explained/dgjsyxd):** The normal transactions in a block - sending DCR to an address, coinbase transactions such as PoW Miner reward and Treasury stipend.

**[Stake transaction tree](https://www.reddit.com/r/decred/comments/66j4l4/decred_proof_of_stake_explained/dgjsyxd)**: Transactions relating to ticket buying and ticket voting rewards.

**Mempool**: Transactions waiting to be mined.

**Block header:** 

**Stakepool:** see Voting Service Provider

**Voting Service Provider:** Non-custodial services that can be authorized to vote on behalf of a ticket, usually providing a number of geographically distributed servers to reduce the chance of missed tickets.

**Staking:** Colloquial term for time-locking DCR in exchange for tickets.

**Voters:** People who buy tickets and vote with them.

**Treasury:** The [Decred Treasury](https://explorer.dcrdata.org/address/Dcur2mcGjmENx4DhNqDctW5wJCVyT3Qeqkx) holds funds for use in development of the project, decisions about how to use these funds are made through Politeia proposals and voting.

**[Politeia](https://docs.decred.org/governance/politeia/):** System for facilitating the [submission and discussion of proposals](https://proposals.decred.org/) in an environment with transparent censorship. 

Proof-of-Work mining:

Difficulty:

Transaction fees:

Miners:

Mining Pool:

Hash:

Hashrate:

[**Hash function:**](https://docs.decred.org/research/blake-256-hash-function/) 

**[Constitution](https://docs.decred.org/getting-started/constitution/):** A document which defines the purpose and guiding principles of the Decred project.

**Block explorer:** A tool for inspecting the contents of blocks in a more user-friendly format.

**Confirmations:** Number of blocks that have been mined on top of the block when a transaction was made - more confirmations = greater finality or confidence that the transaction will remain in the Decred blockchain.

**Orphan:** A valid block which is not built upon and thus not included in the definitive blockchain.

**Reorg:** A reorganization of the blockchain in which a set of blocks are replaced by another (longer) set, the number of blocks replaced is the depth of the reorg. 

**[Inflation:](https://docs.decred.org/advanced/inflation/)** Increase in the available supply of Decred as new DCR is minted into existence through the block reward.

**DCR:** Ticker for the decred currency.

**Credits**: Full units of the decred currency, i.e. 1 DCR

**Atom**: Smallest unit of decred currency, one hundred millionth of a single decred (0.00000001 DCR)

**[Decrediton](https://github.com/decred/decrediton/):** GUI (Graphical User Interface) Decred wallet maintained by the core team. 

**CLI:** Command Line Interface - often referring to a CLI wallet which is operated through the use of various tools/commands.

**[Testnet](https://docs.decred.org/getting-started/using-testnet/):** A parallel network used for testing, where DCR can be obtained freely from faucets.

**Faucet:** A mechanism for obtaining (testnet) tokens for free.

**Mainnet:** The proper Decred network, term used to differentiate from testnet.

**[Simnet](https://docs.decred.org/advanced/simnet/):** A simulation network with very low difficulty, such that a developer can mine new blocks locally at will for testing purposes.




