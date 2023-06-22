# Learn Substrate

- [Learning Link](https://docs.substrate.io/learn/)


# Welcome Notes

- It allows us to develop the application-specific blockchain that can run as standalone services

There are mainly three components in the substrate, according to development
- Substrate Core Modules
- Substrate and FRAME(custom modules as pallets)
  - the modules, macros, and libraries are the core components of the FRAME development environment.
  - The main purpose of the FRAME to provide the components for building the substrate runtime.
- Node templates(compile and deploy common modules)


### Composing runtime

- Each pallet defines the specific types, storage items, and functions to implement a specific set
  of features of functionality for runtime.
- If application need to manage account balance so it can compose a Balances pallet in your custom
  runtime to suit application.

### Substrate Frame Pallets

- Aura
- Babe
- Grandpa
- Elections
- Utility
- Atomic Swap
- Sudo
- Multisig
- Identity
- Assets
- Contracts
- EVM
- Collective
- Treasury
- Election Phragmen
- Democracy
- Randomness
- Timestamp
- Staking
- ...etc

### Composed Runtime Out of the Above Pallets

- Aura
- Grandpa
- Elections
- Utility
- Timestamp
- Collective


### FRAME

- FRAME system frame_system: provides the low-level types, storage, and functions for the runtime.
- FRAME support frame_support: collection of rust macros, types, traits, and modules that simplify 
  the development of the Substrate pallets.
- FRAME executive pallet frame_executive: orchestrate the execution of the incoming function calls




# Blockchain Basics

> A blockchain is a decentralized ledger that records information in a sequence of blocks. 
> The information contained in a block is an ordered set of instructions that might result 
> in a change in state.


> In a blockchain network, individual computers—called nodes—communicate with each other to 
> form a decentralized peer-to-peer (P2P) network. There is no central authority that controls 
> the network and, typically, each node that participates in block production stores a copy of 
> the blocks that make up the canonical chain.

> In most cases, users interact with a blockchain by submitting a request that might result in 
> a change in state, for example, a request to change the owner of a file or to transfer funds 
> from one account to another. These transactions requests are gossiped to other nodes on the 
> network and assembled into a block by a block author. To ensure the security of the data on 
> the chain and the ongoing progress of the chain, the nodes use some form of consensus to agree 
> on the state of the data in each block and on the order of transactions executed.


## What is a blockchain node?

At a high level, all blockchain nodes require the following core components:

- Data storage for state changes recorded
- peer to peer networking
- consensus methodology
- logic for ordering and processing incoming transactions
- crypto for generating hash and digests for blocks and for signing and verifying the sign


## State transition and conflicts

> A blockchain is essentially a state machine. At any point in time, the blockchain has a 
> current internal state. As inbound transactions are executed, they result in changes to 
> state so the blockchain must transition from its current state to a new state.
> To agree on the state after a transition, all operations within a blockchain must be 
> deterministic. For the chain to progress successfully, a majority of the nodes must 
> agree on all the state transitions, including:
> - The initial state of the chain, called the genesis state or genesis block.
> - The series of state transitions that result from executed transactions that are recorded in each block.
> - A final state for the block to be included in the chain.

> The method that a blockchain uses to batch transactions into blocks and to select which 
> node can submit a block to the chain is called the blockchain's consensus model or 
> consensus algorithm. The most commonly-used consensus model is called the proof-of-work 
> consensus model. With the proof-of-work consensus model, the node that completes a 
> computational problem first has the right to submit a block to the chain.

