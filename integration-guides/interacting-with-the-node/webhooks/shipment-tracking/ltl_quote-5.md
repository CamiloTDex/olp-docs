# ShipmentPaymentUpdated

* **Method:** ShipmentPaymentUpdated
* **Trigger:** Shipment payment status updates
* **Payload:**

```typescript
{
    method: "ShipmentPaymentUpdated";
    data: {
        "shipmentId": string,
        "paymentId": number,
        
        // 0 = Invalid,
        // 1 = New,
        // 2 = Processing,
        // 3 = Success,
        // 4 = Failed
        "status": number
    }
}
```
