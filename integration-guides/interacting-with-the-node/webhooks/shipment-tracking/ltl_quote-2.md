# ShipmentReadyForPickup

* **Method:** ShipmentReadyForPickup
* **Trigger:** All booking steps has been completed and the shipment is ready for pickup
* **Payload:**

```typescript
{
    method: "ShipmentReadyForPickup";
    data: {
        "shipmentId": string
    }
}
```
