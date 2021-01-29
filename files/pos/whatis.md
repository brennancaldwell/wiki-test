## What is Proof-of-Stake? {#intro}

Proof-of-Stake (PoS) refers to a category of algorithms that are used to come to consensus in a blockchain system. In precise terms, Proof-of-Stake is a mechanism that prevents Sybil-attacks (i.e. prevents a single participant from masquerading as N others). In a PoS system, a participant's vote in a system is linked directly to the number of coins they have, so that a person who only has 100 coins cannot pretend to be 1000 different people with 100 coins each.

For a blockchain to make progress, new blocks must be created and added to chain. Who has the right to make these new blocks? In a Proof-of-Work system, miners compete for this right by expending computing power to solve random cryptographic puzzles. The winner gets to create the next block, and earns some reward for doing so. In this paradigm, the more computing power a miner has, the more likely they are to create the next block. By contrast, PoS systems revolve around the idea that the more coins a miner/validator/block producer has, the more likely they are to create the next block. 

Broadly, there are 2 classes of proof-of-stake algorithms:

1. **Chain-based Proof-of-Stake**

    As with Bitcoin, one validator is randomly selected in each time slot to create a block that builds on the longest chain (longest/heaviest chain). However, instead of selecting a validator based on who solves the cryptographic puzzles first, the likelihood of selection is weighted according to how many coins they lock-up, or "stake."

2. **Byzantine Fault Tolerant (BFT) Proof-of-Stake**

    Instead of a random validator getting the right to create a block which every other participant must accept, BFT systems introduce the idea of *proposing* and *accepting.* Like the chain-based PoS system, a randomly selected validator (weighted by stake) is chosen to propose a block to the other validators. All the validators must communicate with each other until all honest validators come to agreement. Once they are in agreement, they accept the block and it is finalized as the latest block. 