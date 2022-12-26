# Shipments

### Overview

The shipment is the core value unit of the Open Logistics Protocol, in it most basic form, it represents the movement of a freight in a series of stops, normally from pickup to delivery.

All shipments goes through a series of states from new to closed:

<figure><img src="https://mermaid.ink/img/pako:eNotjr0OwjAQg18lurl9gQxMjEzAmOXIuTQif0oTEKr67oSqnmzZ-uSVbBKQpmfhPKvL1UTVFfFR43hSbC1yhezhkdLrsC7eC8fF1T0JvHujHJ31aYHQQAElsJMOX_9UQ3VGgCHdrWDi5qshE7c-5VbT7Rst6VoaBmpZuOLsuN8KpCf2C7YfRXQ4GQ?type=png" alt=""><figcaption></figcaption></figure>

And it is divided in two main phases:

* Negotiation phase
* Tracking phase

### Roles

In every shipment, there are two main roles:

* Shipper: The one that has a load that needs to be moves
* Carrier: The one that actually moves the load

If a company is a broker, it can act as **Shipper** or as a **Carrier** depending of their role in this shipment.

### Negotiation

The negotiation phase is done completely off-chain, it consists in a series of messages that are being exchanged between two companies, this messages will vary depending of the service type (View  [service-types.md](service-types.md "mention")), but at the end, it ends when both companies agrees to move the load at certain terms.

### Accepted

After a shipment is negotiated, the **Shipper** company will register the shipment on the [logistics-contract.md](ethereum-contracts/logistics-contract.md "mention"), and will wait for the **Carrier** confirmation on-chain

### Booked

When a shipment is confirmed by the carrier on-chain in the [logistics-contract.md](ethereum-contracts/logistics-contract.md "mention"), the shipment state will be set to **Booked**&#x20;

### inTransit

When all the documents has been signed, the shipment will be set to **inTransit**, now the carrier can notify the stops until delivery.

### Delivered

When all the stops has been notified by the carrier, the shipment will be set to **Delivered** state, and the payment process will automatically start.

### Closed

When the payment process is completed, the shipment is set to **Closed** state, and the shipment flow is ended.&#x20;
