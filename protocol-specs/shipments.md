# Shipments

### Overview

A shipment is the core value unit of the Open Logistics Protocol. In its most basic form, it represents the movement of a freight in a series of steps - from pickup to delivery.

A shipment goes through a series of states from "new" to "closed":

<figure><img src="https://mermaid.ink/img/pako:eNotjr0OwjAQg18lurl9gQxMjEzAmOXIuTQif0oTEKr67oSqnmzZ-uSVbBKQpmfhPKvL1UTVFfFR43hSbC1yhezhkdLrsC7eC8fF1T0JvHujHJ31aYHQQAElsJMOX_9UQ3VGgCHdrWDi5qshE7c-5VbT7Rst6VoaBmpZuOLsuN8KpCf2C7YfRXQ4GQ?type=png" alt=""><figcaption></figcaption></figure>

And it is divided in two main phases:

* Negotiation phase
* Tracking phase

### Roles

In every shipment, there are two main roles:

* Shipper: A company with a load that needs to be transported
* Carrier: A company that physically transports the load

If a company is a broker, it can act as **Shipper** or as a **Carrier** depending of their role in the shipment.

### Negotiation

The negotiation phase is done completely off-chain. It consists of a series of messages that are  exchanged between two companies. These messages will vary depending on the service type (View  [service-types.md](service-types.md "mention")). They end when both companies agrees to transport the load in agreed upon terms.

### Accepted

After a shipment is negotiated, the **Shipper** company will register the shipment on the [logistics-contract.md](ethereum-contracts/logistics-contract.md "mention"), and will wait for the **Carrier** confirmation on-chain.

### Booked

When a shipment is confirmed by the carrier on-chain in the [logistics-contract.md](ethereum-contracts/logistics-contract.md "mention"), the shipment state will be set to **Booked**&#x20;

### inTransit

When the documents has been signed, the shipment will be set to **inTransit**. The carrier can notify the steps until delivery {???}.

### Delivered

When all the steps has been notified by the carrier {??}, the shipment will be set to **Delivered** state and the payment process will automatically start.

### Closed

When the payment process is completed, the shipment is set to **Closed** state and the shipment flow is ended.&#x20;
