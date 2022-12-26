# Interacting with the Node

In order to allow the two-directional communications between the node and your backend services, we provide two main interfaces: An HTTP interface for handling incoming requests and webhooks for requesting data and triggering events in the counterparty.

### Available Interfaces

* **HTTP:** Used for backend-to-node communications, listening by default at port 9560, View: [making-requests](making-requests/ "mention")
* **Webhooks:** Used to pull information and trigger events in the backend, View: [webhooks](webhooks/ "mention")
