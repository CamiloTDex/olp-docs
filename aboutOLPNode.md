# About OLP Node

## What is an OLP Node?

OLP is a distributed network of computers (known as nodes) running software that can verify blocks and transaction data.
An OLP node connects to a private network consisting of other OLP nodes. A node is a peer entity of the OLP network that  provides methods to create, exchange, and use the data that exists in local storage. It also tracks the state of the OLP blockchain. A node is any instance that is connected to other computers also running OLP nodes, forming a network. Nodes verify data against the protocol rules and keeps the network secure.Clients interact with the blockchain via OLP nodes. 

Each Node comprises several logical components:

  JSON-RPC service

  Mempool

  Storage

  Consensus (only validators)

  Execution

  State synchronizer

  Virtual machine

The OLP network is not connected to Ethereum Mainnet or an Ethereum testnet at the moment. 
Private networks typically use a different chain ID and consensus protocol. Participation in private networks is typically restricted in some way, so the volume of traffic is much lower than Mainnet, resulting in lower system requirements.
 
Private network system requirements depend on many factors, including:

  Size of the world state for the network.

  Number of transactions submitted to the network.

  Block gas limit.

  Number and complexity of JSON-RPC, PubSub, or GraphQL queries handled by the node.
  
## Why should my company run a node?

Think of your node as a gateway to the rest of the network that comprises of other nodes. By running nodes, you can directly interact with one or more nodes without one-off integrations, which substantially reduces the cost of integration. If you are a TMS that needs trucks, then you can use your node to request truck availability from nodes run by marketplaces, fleet management systems, trucking companies etc. 
More nodes there are more decentralized the protocol will be and more secure. 
By running a node you become part of a global network of logistics from Day 1.


## Does my company have to be a freight tech or logistics company to run a node?

No. As long as you have signed an NDA with dexFreight and agreed to the terms of use you can run a node. In that case, your interest should be to help the network scale and make it more secure. 


## What does it mean to "run a node"?
(Source: ethereum.org) 

Nodes download a copy of the OLP blockchain and verifies the validity of every block, then keeps it up-to-date with new blocks and transactions, and helps others download and update their own copies.

OLP is designed to run a node on average consumer-grade computers. You can use any personal computer, but most users opt to run their node on dedicated hardware to eliminate the performance impact on their machine and minimize node downtime.

Running an OLP node may sound complicated at first, but it's merely the act of continuously running client software on a computer while connected to the internet. While offline, your node will simply be inactive until it gets back online and catches up with the latest changes.

## Local or cloud?
(Source: ethereum.org)

OLP nodes are able to run on consumer grade computers and don't require any special hardware, like mining machines for example. Therefore, you have various options for deploying the node based on your needs. To simplify, let's think about running a node on both a local physical machine and a cloud server:

Cloud:
  Providers offer high server uptime and static public IP addresses
  Getting dedicated or virtual server can be more comfortable than building your own
  Trade off is trusting a third party - server provider
  Because of the required storage size for full node, the price of a rented server might get high

Own hardware:
  More trustless and sovereign approach
  One time investment
  An option to buy preconfigured machines
  You have to physically prepare, maintain, and potentially troubleshoot the machine and networking



