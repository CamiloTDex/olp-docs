# LTL\_QUOTE

* **Method:** LTL Quote
* **Trigger:** A quote request is received
* **Payload:**

```typescript
{
    method: "LTL_QUOTE";
    data: {
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
    }
}
```

* **Expected Response:**

```javascript
{
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
    }],
    
    errors: [{
        error: true;
        src: string;
        msg: string;
    }]
}
```
