# DEFINITIONS OF TERMS
Update: December 09, 2022
Reference: https://ethereum.org/en/developers/


## Open Logistics Protocol (OLP) ACCOUNT
An OLP account is an entity that can send/receive transactions on OLP. Accounts are user-controlled. Creating an account costs nothing. Accounts are made up of a cryptographic pair of keys: public and private keys that control account activities. An account is made up of a cryptographic pair of keys: public and private. They help prove that a transaction was actually signed by the sender and prevent forgeries. Your private key is what you use to sign transactions, so it grants you custody over the funds associated with your account. This prevents malicious actors from broadcasting fake transactions because you can always verify the sender of a transaction.

## ETHEREUM VIRTUAL MACHINE
The Ethereum Virtual Machine (EVM) is a piece of software that executes smart contracts and computes the state of the OLP network after each new block is added to the chain. EVM runs on individual OLP nodes.  Its main purpose is to compute the network's state and to run and compile various types of smart contract code into a readable format called 'Bytecode.' This makes it possible for smart contracts deployed on EVM-compatible chains like Polygon or Avalanche to be recognized by OLP nodes. 

## ON-CHAIN TRANSACTIONS
Transactions are cryptographically signed instructions from OLP accounts and executed via smart contracts. Any node can broadcast a request for a transaction to be executed on the EVM. Transactions require a fee (set to 0 for now) and must be included in a validated block. A transaction needs to be signed using the sender's private key. This proves that the transaction could only have come from the sender and was not sent fraudulently. An account will initiate a transaction to update the state of the OLP network. Transactions, which change the state of the EVM, need to be broadcast to the whole network. 
A submitted transaction includes the following information:
recipient – the receiving address. 
signature – the identifier of the sender. This is generated when the sender's private key signs the transaction and confirms the sender has authorized this transaction.
nonce - a sequentially incrementing counter which indicates the transaction number from the account.
data – optional field to include arbitrary data. It may contain specific instructions about shipment attributes, payments, change of ownership etc. depending on the use case. 

## CONSENSUS
The consensus process is controlled by a predefined set of nodes that are trusted. The term 'consensus mechanism' is often used colloquially to refer to 'proof-of-stake', 'proof-of-work' or 'proof-of-authority' protocols. OLP nodes run Hyperledger Besu as an Ethereum client that runs Ethereum protocol in a permissioned environment. Hyperledger Besu implements Proof of Authority consensus protocol which is used when participants are known to each other and there is a level of trust between them. It uses IBFT 2.0 in which networks, transactions and blocks are validated by approved accounts, known as validators. Validators take turns creating the next block. Existing validators propose and vote to add or remove validators. IBFT 2.0 has immediate finality. 

## DECENTRALIZED STORAGE
Unlike a centralized server operated by a single company or organization, in OLP decentralized storage systems consist of a peer-to-peer network of nodes who hold a portion of the transaction data (currently in MongoDB), creating a resilient file storage sharing system. The data shared strictly between the two nodes via p2p method is not replicated in the network. 

## WALLETS
OLP wallets are applications that let you interact and manage your OLP account. It allows you to view and send transactions to the network. Wallets can be implemented as hardware wallets, mobile phones, browser apps, desktop apps etc. 
ON-CHAIN VS OFF-CHAIN
On-chain transactions means transactions that are replicated in each node and executed using OLP’s smart contracts. Off-chain transactions occur between two or more nodes but are not visible to the rest of the nodes in the network and are not executed via smart contracts.   

## BLOCK EXPLORERS
Block explorers are your portal to OLP’s on-chain data. You can use them to see real-time data on blocks, transactions, accounts, and other on-chain activity.

## ORACLES
Oracles are data feeds that bring data from sources outside the blockchain (off-chain) and provide it to the blockchain (on-chain) for smart contracts to use. This is necessary because smart contracts in OLP cannot access information stored outside the network. Giving smart contracts the ability to execute using off-chain data inputs extends decentralized applications' value. For example, a smart contract may use the GPS location of a truck as an external input. 






