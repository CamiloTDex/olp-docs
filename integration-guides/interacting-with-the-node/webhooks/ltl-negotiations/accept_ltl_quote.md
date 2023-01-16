# ACCEPT\_LTL\_QUOTE

* **Method:** ACCEPT\_LTL\_QUOTE
* **Trigger:** A quote is accepted
* **Payload:**
  * **ID: Quote DID**
  * **User: User DID of the user that is accepting the load**

```typescript
{
    method: "ACCEPT_LTL_QUOTE";
    data: {
        id: string,
        user: string
    }
}
```

* **Expected Response:**&#x20;

```javascript
{ result: boolean }
```
