# Substrate

[Copied From Link](https://docs.substrate.io/quick-start/substrate-at-a-glance/) 

## What is Substrate

It is an SDK to build application specific blockchains from modular and extensible
components. By using it we can mostly focus on application logic.

## What is FRAME

- FRAME provides the core modular and extensible components.
- Most if the modules that FRAME provides takes form of plug-in modules
  called pallets that you can add and configure to your suit.

## Why use Substrate and FRAME?

By using Substrate and FRAME, you can build proof-of-concept application-specific 
blockchains without the complexity of building a blockchain from scratch or the 
limitations of building on a general-purpose blockchain.


## What is Substrate node? 

Every blockchain platform relies on a decentralized network of computers—called 
nodes—that communicate with each other about transactions and blocks.

- Node is a software that is running on connected devices, not the physical device itself.

- Substrate nodes consist of two main parts with separate responsibilities:
  - A core client with outer nodes services to handle network and blockchain infra activity
  - A runtime with business logic for state transition and the current state of the blockchain


# Start a Node

## Clone the repo and build

```sh
git clone https://github.com/substrate-developer-hub/substrate-node-template
cd substrate-node-template
cargo build --package node-template --release
```

### Error: Protobuf error

```shell
brew install protobuf
```

### Error: Wasm Target

```shell
rustup target add wasm32-unknown-unknown
```

## About the node

- Info of the node

```shell
./target/release/node-template --help
```

- View Info about the predefined `Alice`


```shell
./target/release/node-template key inspect //Alice
```

### Start a blockchain

```shell
./target/release/node-template --dev

# OR

cargo run --release -- --dev
```

## Connect to a Node

- Check the predefined Alice Account
- Open index.html
- copy and paste the SS58 address from Alice account and then click on Get Balance


## Explore the Node

Node Template includes
- peer-to-peer networking
- simple consensus
- transaction handling
- working with accounts, balances, transaction fees and performing admin actions
- This core set of functions provided through the several defined modules pallets
  - predefined node templates
    - pallet_balances
    - pallet_transaction_payment
    - pallet_sudo


## Learn

- [Learn Substrate](./learn.md)


## Need to Learn Later

- What is Palkadot: Shared security provider
- libp2p and jsonRPC protocols