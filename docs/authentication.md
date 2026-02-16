# Authentication

All endpoints require an API key in the request header for authorization.

---

## Header

| Header        | Type   | Description                          | Required |
|---------------|--------|--------------------------------------|----------|
| Authorization | string | API key in the format `Bearer <key>` | Yes      |

---

## Example Request

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" https://api.example.com/animals
```
> Replace YOUR_API_KEY with the key provided to you for testing.

---

## Response Codes 

| HTTP Code | Meaning                          |
|-----------|----------------------------------|
| 401       | Unauthorized / Missing API key   |
| 403       |Forbidden / Invalid API key       |
