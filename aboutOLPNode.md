# About OLP Node

An OLP node connects to a private network consisting of other OLP nodes. A node is a peer entity of the OLP network that  provides methods to create, exchange, and use the data that exists in local storage. It also tracks the state of the OLP blockchain. Clients interact with the blockchain via OLP nodes. 

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
