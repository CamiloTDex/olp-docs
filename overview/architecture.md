# OLP Architecture

Core services represent foundational elements that the protocol enables applications and business cases mentioned previously. We deem core services as essential functions, very much like an operating system, for the network participants to operate on. The core services layer provides the participants a neutral and unbiased playground for the participants to perform businesses via applications built. 

Please note that the protocol may add more services as it evolves over time. Also, the actual implementation of the services may differ from originally planned. 



{Insert figure}

Other physical components of the network include peer to peer nodes that participants run on top of their existing ERP solution or a separate application provided to the participants by a third party. These nodes exchange information with transacting parties to share pricing, bids, documents, sign contracts, and issue payments. However, these nodes need the support of an underlying blockchain to persistently verify identities (ID verification) of other parties before and during transactions. The ID then ties to the transacting parties on chain reputation because parties may decide to transact only with reputable companies (e.g., carriers whose operating authority have not lapsed). 
 
The side chain or Layer 2 is optional however it serves an important interim purpose to “host” several core services related smart contracts such that the nodes receive transaction confirmations much quicker than using public permissionless blockchain such as Ethereum. The side chain is anchored to Ethereum or Bitcoin at predefined intervals using trusted relays. 
