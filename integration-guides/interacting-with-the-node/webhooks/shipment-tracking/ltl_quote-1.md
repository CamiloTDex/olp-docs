# ShipmentAccepted

* **Method:** ShipmentAccepted
* **Trigger:** A shipment is confirmed by the carrier on-chain
* **Payload:**

```typescript
{
    method: "ShipmentAccepted";
    data: {
        "shipmentId": string
    }
}
```
