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

