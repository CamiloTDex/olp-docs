# ShipmentStop

* **Method:** ShipmentStop
* **Trigger:** The shipment has arrived to a specified stop
* **Payload:**

```typescript
{
    method: "ShipmentStop";
    data: {
        "shipmentId": string,
        "stop": number
    }
}
```
