# /ltl/quote 👤

Retrieves LTL quotes from your node, this endpoint does not fetch quotes from the network.\
If you are looking for fetching quotes from the network, consider using: [ltl-quoteallpeers.md](ltl-quoteallpeers.md "mention")

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
