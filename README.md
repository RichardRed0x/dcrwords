dcrwords

## Decred Glossary

**Distributed ledger:** 
A cryptographically secure ledger, compased of nodes in a network, where each node holds a copy of the same ledger. 

**Consensus rules:** 
Rules, encoded in software, that allow a network of nodes to reach an agreement about the state of the ledger. Rules include what data blocks can contain, how block data is structured, and how nodes validate blocks. 

**Protocol rules:** 
See consensus rules. 

**Block:** 
The data structure transactions are bundled into before being written into the distributed ledger. Decred's difficulty adjusts such that new blocks are found every five minutes on average.

**Wallet:**
A file that stores private keys. Wallets allow their owner to view and create transactions on the blockchain. The Decred team maintains a GUI wallet (Decrediton) and Command Line Interface (CLI) wallet tools for advanced users. Decred is also supported by numerous 3rd party wallets.

Wallets allow its owner to view and create transactions on the blockchain. Decred's native wallet daemon can be accesseed via [Decredition](https://docs.decred.org/getting-started/user-guides/decrediton-setup/), which provides a GUI interface, as well as the [Command Line Interface (CLI) wallet](https://docs.decred.org/getting-started/user-guides/cli-installation/) (for advanced users). Decred is also supported by numerous [3rd party wallets](https://decred.org/downloads/).

**Seed:** 
A series of 33 words that is used to generate the private key for a wallet. Anyone who has the seed for a wallet can spend any DCR it holds.

**Private passphrase:** 
A passphrate that is used to encrypt wallet.db files. wallet.db files encrypted with a private passphrase cannot be used without that passphrase.

**Account:** 
Accounts allow you to keep separate records of your DCR funds. Transferring DCR across accounts will create a transaction on the blockchain.

**Address:**
The cryptographic hash of a given public key. Addresses are publicly viewable on the blockchain and can be used to send and receive transactions, similar to an email address. 

**Private key:**
A string of data that allows you to access and spend DCR stored in address associated with the private key. When sending DCR from one address to another, the wallet must use the private key of the sending address to sign the transaction.

**Public key:**
A long string of alphanumeric characters generated algorithmically from a private key. The user’s public key is used to prove that a transaction was signed using their private key.

**Extended public key:**
A public key extended using [Hierarchical Deterministic (HD) key creation](https://bitcoin.org/en/developer-guide#hierarchical-deterministic-key-creation) and transfer protocol, which allows creation of child keys from parent keys in a heirarchy. Wallets using the HD protocol are called HD wallets. 

**Watch-only:**
An address or pubkey script stored in the wallet without the corresponding private key, allowing the wallet to watch for outputs but not spend them.

**Proof-of-Stake (PoS) voting:**
The mechanism by which ticket holders vote to approve blocks confirmed by PoW miners (thus providing a check on PoW miners), earn staking rewards, and vote on consensus rule changes and Politeia proposals. 

**[Hybrid PoW/PoS:](https://docs.decred.org/research/hybrid-design/)** 
In Decred, a [hybrid PoW/PoS system](https://docs.decred.org/research/hybrid-design/) is used, whereby blocks mined by PoW miners must be approved by ticket holders, which are pseudorandomly selected from the ticket pool. This provides a check on PoW miners and increases the overall cost of attacking the network. When a block is approved, 60% of the block reward goes to the PoW miner, 30% goes to the holders of  tickets called to vote (approve blocks), and 10% goes to the Decred Treasury to fund the project's development.

**Block reward:**
A reward (in DCR) split between PoW miners, ticket holders, and the Treasury for successfully approving a block of transactions. As in Bitcoin, the block reward [decays exponentially](https://docs.decred.org/advanced/inflation/) with block height (length of blockchain). However, Decred’s algorithm interpolates this decay over time so as not to produce market shocks, as typically seen when Bitcoin's difficulty halves. The block reward started at 31.19582664 and it adjusts every 6,144 blocks (approximately 21.33 days) by reducing by a factor of 100/1011.

**Ticket**: 
Decred holders can time-lock DCR in exchange for tickets. Tickets grant their holder the ability to vote, and it is through ticket voting that major governance decisions are made. The DCR locked to buy a ticket is unlocked after that ticket is called to vote on-chain (this averages around one month, maximum around 4 months), along with a reward. Around 0.5% of tickets are not called before they expire; in this case the DCR is un-locked but no reward is granted.

**[Consensus rules voting](https://docs.decred.org/getting-started/user-guides/agenda-voting/):** 
Changes to Decred's consensus rules can only be made through an on-chain voting process which lasts for around one month. The change is made only if at least 75% of votes are in favor. 

**Agenda voting:** see consensus rules voting

**Quorum:** 
The minimum level of participation required in order for a decision-making process to produce a valid outcome. Changes to the consensus rules require at least 10% of votes to be for or against the change in order to be valid.

**Rule change proposal:** 
A proposal to change the consensus rules of the Decred blockchain. Rule change proposals must be implemented in latent code within the software running the network's nodes. If the proposal passes, the latent code activates one month later. 

**[Decred change proposal (DCP)](https://github.com/decred/dcps):**  
A design document that describes potential protocol or consensus changes to Decred. DCPs primarily serve for documentation, fostering cross-implementation compatibility and helping ensure proper engineering rigor is followed.

**Stake Version Interval (SVI):** 
An interval of blocks 2016 blocks (~1 week) which is used to determine if a vote on concensus rules can begin. Before a vote on consensus rule changes can begin, 75% of tickets that vote during a Stake Version Interval (SVI) must be using software that contains the latent software change being proposed. 

**Rule Change Interval (RCI):**
An interval of 8064 blocks (~4 weeks) in which ticket holders can vote on consensus rule changes. A Rule Change Interval (RCI) consists of four Stake Version Intervals (SVI), which are 2016 blocks (~1 week). Once the conditions for a vote have been met during an SVI, voting is scheduled to begin on the first block of the next RCI. Because there are four SVIs per RCI, it can take up to 6048 blocks [3 SVIs] for the next RCI to begin.


**[Ticket pool](https://docs.decred.org/mining/proof-of-stake/):** 
The pool of live tickets that are available to be called to vote. The target size for the ticket pool is 40,960.

**Ticket price:** 
The amount of DCR one must time-lock in order to buy a ticket. The ticket price is algorithmically adjusted with the goal of keeping the ticket pool at an optimal size of 40,960 tickets. The algorithm for setting the ticket price was changed by [DCP-0001](https://github.com/decred/dcps/blob/master/dcp-0001/dcp-0001.mediawiki), the first consensus rules change to be adopted using an on-chain vote. 

**Ticket-splitting:** 
The process of buying part of a ticket. This done by coordinating with other parties who will buy the other parts of a ticket. This can be done without giving up custody to your DCR. The minimum amount of DCR that can be put into a split ticket is 5 DCR. Ticket-splitting is currently coordinated through the #ticket-splitting channel on the [Decred slack](https://slack.decred.org/). 

**Ticket status terms**

​	**Unmined ticket:**  Immediately after a ticket is bought it is unmined until the transaction is included in a block.

​	**Immature ticket:** Once tickets are mined they are immature for 256 blocks (about 20 hours) and cannot be called to vote until after this period elapses.

​	**Live ticket:** Tickets that are waiting to be called.

​	**Voted ticket:** Tickets that have been called and responded with votes; once a ticket has voted, the DCR locked to buy it becomes spendable after 256 blocks.

​	**Missed ticket:** Tickets that have been called but did not respond - these can be revoked, but do not grant a reward.

​	**Expired ticket:** Tickets that reached the end of their window without being called to vote - these can be revoked, but do not grant a reward.

​	**Revoked ticket:** When a ticket (that was missed or expired) is revoked, the DCR used to buy it becomes spendable again.

**Block voting:** In each block, five tickets are called to vote. In addition to votes on any open consensus rule change proposals, each ticket votes to approve or reject the regular transaction tree of the previous block. If a majority of voting tickets vote No, the regular transaction tree of the previous block is rejected and those transactions are returned to the mempool.

**[Regular transaction tree](https://www.reddit.com/r/decred/comments/66j4l4/decred_proof_of_stake_explained/dgjsyxd):** 
The normal transactions in a block: sending DCR to an address, coinbase transactions such as PoW Miner reward and Treasury stipend.

**[Stake transaction tree](https://www.reddit.com/r/decred/comments/66j4l4/decred_proof_of_stake_explained/dgjsyxd)**: 
Transactions relating to ticket buying and ticket voting rewards.

**Mempool**: 
Transactions waiting to be mined.

**Block header:** 
Metadata at the beginning of a block that defines information about the block. The hash of a block header is the main way of identifying a block. 

identify a particular block, which is hashed repeatedly to create proof of work for mining rewards. 

**Stakepool:** 
see Voting Service Provider

**Voting Service Provider:** 
Non-custodial services that can be authorized to vote on behalf of a ticket, usually providing a number of geographically distributed servers to reduce the chance of missed tickets.

**Staking:** 
Colloquial term for time-locking DCR in exchange for tickets.

**Voters:** 
People who buy tickets and vote with them.

**Treasury:** 
The [Decred Treasury](https://explorer.dcrdata.org/address/Dcur2mcGjmENx4DhNqDctW5wJCVyT3Qeqkx) holds funds for use in development of the project. Decisions about how to use these funds are made through Politeia proposals and voting.

**[Politeia](https://docs.decred.org/governance/politeia/):** 
A system for facilitating the [submission and discussion of proposals](https://proposals.decred.org/) in an environment with transparent censorship. 

**Difficulty:**
Difficulty is a measure of how difficult it is to mine a new block (i.e. find a hash below a given target). In Decred, the PoW difficulty is calculated from the exponentially weighted average of differences in previous block times.  

**Transaction fees:**
A fee paid to have your transaction included in a block. The default transaction fee for Decred is 0.001 DCR/kB.

**Miners:**
Miners help secure the network via Proof-of-Work (PoW) mining. Miners recieve block rewards and transaction fees for successfully validating blocks. 

**Mining Pool:**
A group of miners who share (pool) their computational resources to mine DCR. When a member of a mining pool successfully mines a block, the rewards are split among all pool members in proportion to their hashpower contributed to the pool. 

**Hash:**
The output of a cryptographic hashing function that produces a fixed-size and unique hash value from variable-size input. 

**Hashrate:**
The number of hashes per second computed by miners on the network. 

[**Hash function:**](https://docs.decred.org/research/blake-256-hash-function/) 
A cryptographic function that produces a fixed-size and unique hash value from variable-size transaction input. Decred uses the [BLAKE-256](https://docs.decred.org/research/blake-256-hash-function/) hashing function. 

**[Constitution](https://docs.decred.org/getting-started/constitution/):** 
A document which defines the purpose and guiding principles of the Decred project.

**Block explorer:** 
A tool for inspecting the contents of blocks in a more user-friendly format. 

**Confirmations:** 
The number of blocks that have been mined on top of the block when a transaction was made; more confirmations = greater finality or confidence that the transaction will remain in the Decred blockchain.

**Orphan:** 
A valid block which is not built upon and therefore not included in the definitive blockchain.

**Reorg:** 
A reorganization of the blockchain in which a set of blocks are replaced by another (longer) set. The number of blocks replaced is the depth of the reorg. 

**[Inflation:](https://docs.decred.org/advanced/inflation/)** 
Increase in the available supply of Decred as new DCR is minted into existence through the block reward.

**DCR:** 
Ticker for the Decred currency.

**Credits**: 
The full unit of the Decred currency (i.e. 1 DCR).

**Atom**: 
The smallest unit of Decred currency. One atom is one hundred millionth of a single DCR (0.00000001 DCR).

**[Decrediton](https://github.com/decred/decrediton/):** 
A GUI (Graphical User Interface) Decred wallet maintained by the core team. 

**Command Line Interface (CLI):** 
An interface a user interacts with via the command line - often referring to a CLI wallet, which is operated using various tools/commands.

**[Testnet](https://docs.decred.org/getting-started/using-testnet/):** 
A parallel network used for testing, where DCR can be obtained freely from faucets.

**Faucet:** 
A mechanism for obtaining (testnet) tokens for free.

**Mainnet:** 
The proper Decred network - a term used to differentiate from testnet.

**[Simnet](https://docs.decred.org/advanced/simnet/):** 
A simulation network with very low difficulty, such that a developer can mine new blocks locally at will for testing purposes.




