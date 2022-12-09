# /shipments/setupDrivers 👤

Assign driver to the shipment, the driver is the responsible of confirming stops, if no driver is present, the carrier address will update

```ejs
throw "Shipment not found"
throw "Forbidden"
throw "Shipment service type is not ftl"

/negotiations/confirmShipment {
    shipmentId: string,
    driverAddresses: string[],
    token: string
} => void
```

