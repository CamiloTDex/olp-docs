# Companies

### Overview

Companies are the main bussiness participants of the network.\
The companies are the ones that actually negotiates, book and track shipments in the network.

All companies have their own ethereum address that is independent of the node, each company must notify the [registry-contract.md](ethereum-contracts/registry-contract.md "mention") who is their **parent node**, so the node can route the incoming requests for the company.

### Parent Nodes

Parent nodes are the ones that are allowed to receive requests and notifications for a company, it is defined as a did:node:0x... that resolves to a node multiaddress as defined in: [nodes.md](nodes.md "mention")

This node is the one that is responsible to resolve company information and do all the required p2p off-chain transactions.

### Identity

A company DID can be related to many services in the network, but their identity will always be its DID.

The DID of the company is defined in the following format:

did:company:\<company\_ethereum\_address>

### Sending messages to a company

Companies itself cannot receive messages through the network, but their **parent node** will handle the requests for them.  To send p2p messages to a company, you must resolve their **parent node** first.\
\
**Note:** All off-chain messages are done by the nodes, not by the company itself. On the other side, all on-chain transactions are signed by the company address, this

<figure><img src="https://mermaid.ink/img/pako:eNqNkbFOAzEMhl_l5IlKrRA3ZugCGxJFdCSoshL3OOmSHI4znKq-O05LBYITkCG29Nuf_8QHcMkTGMj0Vig6uuuxYww2NnoeVLtZrddP1PVZeLpNURidmGZEpihVv7Lge29cCiPG6RJ3JK_EVMIOvWfK2cLizPzOWin_NMc0lRM1PV3tT8QfnjqSDzO_Qf7h49wZyiD97Oga22oXh0dOklwammse3WdV-4W2uZ_tfub641le5rtUzmOKmVSHJQTigL3XRR1qvQV9ViALRlNPe1SvFmw8aikWSdspOjDChZZQRo9y2SuYPQ6Zju-146zk?type=png" alt=""><figcaption></figcaption></figure>

