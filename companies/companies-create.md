# /companies/create 🔒

Register a company

```ejs
throw "Forbidden"
throw "Company already exists"

/companies/create {
    name: string,
    adminToken: string,
    
    uniqueId?: string,
    dot?: string,
    mc?: string
} => {
    did: string,
    name: string,
    dot: string?,
    mc: string?
}
```
