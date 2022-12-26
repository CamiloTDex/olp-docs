# /auth/generateAdminToken

Generates an admin token, it is required to manage the OLP node, all endpoints marked with the 🔒 icon requires the administrator token.

```ejs
throw "Invalid credentials"

/auth/generateAdminToken {
    username: string,
    password: string
} => string
```
