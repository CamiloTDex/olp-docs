# Negotiating an LTL Shipment

### LTL Flow

The process of booking an LTL shipment follows the following steps:

1. **As seller**
   1. The seller quotes an ltl shipment using [ltl-quoteallpeers.md](managing-an-ltl-shipment/ltl-quoteallpeers.md "mention") and receives back a list of quotes for each node in the network
   2. The seller accepts a quote and receives back a shipment, this shipment will be published on-chain and then can be tracked as described at: [managing-shipments](../managing-shipments/ "mention") with the seller acting as the shipper.
2. **As Buyer**
   1. When a quote request is received, the node will send an [ltl\_quote-webhook.md](../webhooks/ltl\_quote-webhook.md "mention") webhook to the Buyer Backend.  The backend must response with a list of quotes as described in [ltl\_quote-webhook.md](../webhooks/ltl\_quote-webhook.md "mention")
   2. When a quote is accepted, the node will send an [accept\_ltl\_quote-webhook.md](../webhooks/accept\_ltl\_quote-webhook.md "mention") webhook to the Buyer Backend.  The backend must response with a full shipment body, similar to [shipments-create.md](managing-an-ftl-shipment/shipments-create.md "mention") as described in [accept\_ltl\_quote-webhook.md](../webhooks/accept\_ltl\_quote-webhook.md "mention")
   3. This shipment will be sent to the seller and after being created on-chain, the buyer will act as carrier and can track the shipment as described at: [managing-shipments](../managing-shipments/ "mention")

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
