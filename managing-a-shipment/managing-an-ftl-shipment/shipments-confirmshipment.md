# /shipments/confirmShipment 👤

As a carrier, manually confirms a shipment on-chain, required when the shipment accepts the shipment, if automatic confirmation is enabled, this step is not required

```ejs
throw "Shipment not found"
throw "Forbidden"
throw "Shipment service type is not ftl"

/negotiations/confirmShipment {
    shipmentId: string,
    token: string
} => void
```

