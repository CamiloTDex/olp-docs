# /ltl/quoteAllPeers 👤

Retrieves LTL quotes from the network.

```ejs
throw "Forbbiden"

/ltl/quote {
    "quote": {
        "origin": {
            "zipCode": string,
            "city": string,
            "state": string
        },
        "destination": {
            "zipCode": string,
            "city": string,
            "state": string
        },
        "items": [{
            "handling": number,
            "packageType": string,
            "pieces": number,
            "totalWeight": number,
            "width": number,
            "length": number,
            "height": number,
            "class": string
        }]
    },

    "token": string
} => {
    success: [{
        company: {
            name: string,
            id: string,
            did: string
        },
        
        expirationDate: Date,
        id: string,
        rate: number,
        transitDays: number,
        notes: string,
        hash: string
    }]
}
```
