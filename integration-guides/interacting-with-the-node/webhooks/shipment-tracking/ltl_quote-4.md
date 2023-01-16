# ShipmentDelivered

* **Method:** ShipmentDelivered
* **Trigger:** All stops has been confirmed and shipment is now delivered
* **Payload:**

```typescript
{
    method: "ShipmentDelivered";
    data: {
        "shipmentId": string
    }
}
```
