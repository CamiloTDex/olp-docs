# Connecting OLP Node via HTTP

The Open Logistics Node listens for HTTP requests at port :9560 by default, this requests can be done either as GET requests with named query params or a POST request with JSON body.



When authentication is needed, an argument called token or adminToken will be required



For Example, for creating an user you can either use:

```javascript
GET - /users/create?username=...&password=...&companyId=...&adminToken=...

POST - /users/create {
    username: ...,
    password: ...,
    companyId: ...,
    adminToken: ...
}
```
