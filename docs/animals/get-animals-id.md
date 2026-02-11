# GET /animals/{id}

Retrieve the details of a single animal by its unique ID.

---

## Endpoint

`GET /animals/{id}`

---

**Path Parameter:**

| Parameter | Type   | Description                     | Required |
|-----------|--------|---------------------------------|----------|
| id        | string | Unique identifier of the animal | Yes      |

**Example:** 

`GET /animals/a123`

This request will return the details of the animal with ID a123.

---

## Response Fields

See [Animals Overview](animals-overview.md) for full field descriptions.

---

## Response

### 200 OK

```json
{
  "id": "a123",
  "name": "Bella",
  "species": "dog",
  "age": 4,
  "status": "available",
  "arrivalDate": "2025-01-10",
  "personality": {
    "friendly": true,
    "playful": true
  },
  "technicalData": {
    "size": "medium",
    "weight": 20,
    "color": "brown"
  },
  "medicalStatus": "healthy"
}
```

### 404 Not Found

```json
{
  "error": "Animal with ID 'a999' not found."
}
```

> Note: If the specified ID does not exist, a 404 Not Found response is returned.

## Response Codes

| HTTP Code | Meaning                                |
|-----------|----------------------------------------|
| 200       | Successfully returned the animal       |
| 404       | Animal with the specified ID not found |
| 500       | Server error                           |
