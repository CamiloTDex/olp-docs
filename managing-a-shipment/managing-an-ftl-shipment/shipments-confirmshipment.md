# /shipments/confirmShipment 👤

Manually confirms a shipment on-chain, required when the shipment accepts the shipment, if automatic confirmation is enabled, this step is not required

```ejs
throw "Shipment not found"
throw "Shipment unavailable"
throw "Invalid value"
throw "Carrier are not in a negotiation"
throw "Shipment service type is not ftl"

/negotiations/accept {
    shipmentId: string,
    carrierAddress: string,
    token: string
}
```

