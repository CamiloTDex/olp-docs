# Nodes

### Overview

Nodes are the main network participants of the open logistics protocol. They are responsible to expose your resources (e.g., shipments, trucsk) to the network and receive resources.

In order to be considered a node, an application must meet the following requirements:

* Must have an Ethereum private keys, the public address will be their network identity
* Must have a [libp2p](https://libp2p.io/) compatible P2P **multiaddress** and it must be accessible from the network
* The **libp2p multiaddress** MUST be registered in the [registry-contract.md](ethereum-contracts/registry-contract.md "mention")

### DID

The DID of a node is represented in the format did:\<node\_ethereum\_public\_address>

### Connecting to a Node

All comunications between nodes in the network are done by using [libp2p](https://libp2p.io/) connections.

<figure><img src="https://mermaid.ink/img/pako:eNptkD9PAzEMxb9K5AmkVogbM3SBDQlQGQk6mcQ9Ii7J1XGGU9Xvjq8V4o-awYn03vvF9gF8CQQWKu0bZU_3EQfG5LLR86ja7Xqz2dIQq_B8V7IwerFmILlyEGKwWT2n0vUkH8TUUj-19zH6_pNmB9dn1H_EWrEnvDXncGqjRAyBqda_vy93Z02IOD5zkeLLaG548j-u7hft6eFi-pWXAau8XU6pXKeSK6kOK0jECWPQvRwWvwOdLJEDq89AO9ReHbh8VCs2KS9z9mCFG62gTQHle41gdzhWOn4Brjl4qQ?type=png" alt=""><figcaption><p>Open Logistics Protocol Node Requests</p></figcaption></figure>

1. Node 1 resolves the multiaddress of the Node 2 using the registry contract
2. Node 1 connects via p2p to Node 2 using the /rpc protocol
3. Node 1 sends a request as described in: [p2prequest.md](structs/p2prequest.md "mention")
4. Node 2 returns the response as described in: [p2presponse.md](structs/p2presponse.md "mention")
