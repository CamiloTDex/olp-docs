# /negotiations/decline 👤

Create a negotiation for an ftl shipment

```ejs
throw "Shipment not found"
throw "Carrier are not in a negotiation"
throw "Shipment service type is not ftl"

/negotiations/accept {
    shipmentId: string,
    carrierAddress: string,
    token: string
} => void
```
