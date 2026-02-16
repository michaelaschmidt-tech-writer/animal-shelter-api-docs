# Error Responses

All endpoints return errors in a consistent JSON format.

---

## Error Schema

Each error response follows this structure:

```json
{
  "error": {
    "code": "string",
    "message": "string",
    "details": "optional string"
  }
}
```

## Fields

| Field    | Type   | Description                                              |
|----------|--------|----------------------------------------------------------|
| code     | string | Machine-readable error code (e.g., "404", "400", "500")  |
| message  | string | Human-readable description of the error                  |
| details  | string | Optional additional information for debugging or context |

---

## Common Error Codes

| HTTP Code | Meaning                                 |
|-----------|-----------------------------------------|
| 400       | Invalid request body                    |
| 401       | Unauthorized / Missing API key          |
| 403       | Forbidden / Invalid API key             |
| 404       | Animal with the specified ID not found  |
| 500       | Server error                            |

---

## Example Error Responses

### 400 Bad Request
```json
{
  "error": {
    "code": "400",
    "message": "Invalid request body",
    "details": "The 'age' field must be a positive integer."
  }
}
```

### 401 Unauthorized
```json
{
  "error": {
    "code": "401",
    "message": "Missing API key",
    "details": "Please provide a valid API key in the 'Authorization' header."
  }
}
```

### 403 Forbidden
```json
{
  "error": {
    "code": "403",
    "message": "Invalid API key",
    "details": "Your API key does not have access to this resource."
  }
}
```

### 404 Not Found
```json
{
  "error": {
    "code": "404",
    "message": "Animal with the specified ID not found",
    "details": "No animal exists with the given ID."
  }
}
```

### 500 Internal Server Error
```json
{
  "error": {
    "code": "500",
    "message": "Server error",
    "details": "An unexpected error occurred. Please try again later."
  }
}
```
