# /users/create 🔒

Creates a user related to an specific company.

```ejs
throw "Forbidden"
throw "Company not found"
throw "User already taken"

/users/create {
    username: string,
    password: string,
    companyDID: string,
    role: "admin" | "user",
    adminToken: string
} => {
    username: string,
    role: string,
    companyDID: string,
    did: string
}
```
