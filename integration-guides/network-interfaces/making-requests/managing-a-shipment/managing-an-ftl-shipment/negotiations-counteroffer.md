# /negotiations/counteroffer 👤

Counteroffers a negotiation for an ftl shipment

```ejs
throw "Shipment not found"
throw "Shipment unavailable"
throw "Invalid value"
throw "You are not in a negotiation"
throw "Shipment service type is not ftl"

/negotiations/counteroffer {
    shipmentId: string,
    value: number,
    token: string
} => void
```
