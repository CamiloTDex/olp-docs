# /shipments/confirmStop 👤

Confirms an stop, when all stops are confirmed, the shipment will be setup as delivered

```ejs
throw "Shipment not found"
throw "Forbidden"
throw "Shipment is not available to confirm stops"

/negotiations/confirmStop {
    shipmentId: string,
    token: string
} => void
```

