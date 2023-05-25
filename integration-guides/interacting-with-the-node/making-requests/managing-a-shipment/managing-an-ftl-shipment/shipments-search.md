# /shipments/search 👤

Searching shipments in the open logistics protocol is a process where you query shipment information from other nodes based on an specific filter.

```ejs
// Note: All fields are optional
POST /shipment/search {
    query: {
        "origin.city": string;
        "origin.state": string;
        "origin.zipCode": string;
        "origin.country": string;
        
        "destination.city": string;
        "destination.state": string;
        "destination.zipCode": string;
        "destination.country": string;
        
        createdAt: { $lt: string, $gt: string } // Filters between posting dates
        
        "payment.negotiable": boolean;
        
        // Filters between rate ranges, note that not all shipments has payment rates
        "payment.rate": { $lt: number, $gt: number }; 
        "payment.rules": "FullTruckload" | "none",
        "payment.processor": "dexFreight" | "none",
        
        // Note that all pi
        "appointment.pickup.from": { $lt: string, $gt: string } // Filters between pickup dates
        "appointment.pickup.until": { $lt: string, $gt: string } // Filters between pickup dates
        "appointment.arrive.from": { $lt: string, $gt: string } // Filters between pickup dates
        "appointment.arrive.until": { $lt: string, $gt: string } // Filters between pickup dates
    
        "weight": { $lt: number, $gt: number }; // Filters weight in lbs
        "equipments": string | { $in: string[] } | { $nin: string[] }; // Filters by specific equipment, or a set of equipments or excluding a set of equipments respectively
    },
    
    token: string;
}
```

\
The response will come in the following format:

```ejs
{
    //? Using the nodeDID you can later fetch the public information about the node
    [nodeDID]: {
        "shipmentId": string;
        "shipper": string; // Shipper's node did, did:node:*
        "origin": {
            "city": string;
            "state": string;
            "zipCode": string;
            "country": string;
        },
        "destination": {
            "city": string;
            "state": string;
            "zipCode": string;
            "country": string;
        },
        "active": boolean;
        "state": string;
        "createdAt": string;
        "payment": {
            "negotiable": boolean;
            "rules": string;
            "rulesAddress": string;
            "processor": string;
            "processorAddress": string;
        },
        "appointment": {
            "pickup": {
                "from": string; // Optional
                "until": string; // Optional
            },
            "arrive": {
                "from": string; // Optional
                "until": string; // Optional
            }
        },
        "equipments": string[],
    }[]
}
```

