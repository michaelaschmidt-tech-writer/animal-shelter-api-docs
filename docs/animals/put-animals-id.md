# PUT /animals/{id}

Update an existing animal in the shelter.

---

## Endpoint

`PUT /animals/{id}`

---

## Path Parameters

| Parameter | Type   | Description                     | Required |
|-----------|--------|---------------------------------|----------|
| id        | string | Unique identifier of the animal | Yes      |

---

## Request Body

| Field         | Type    | Description                                 | Required |
|---------------|---------|---------------------------------------------|----------|
| name          | string  | Name of the animal                          | Yes      |
| species       | enum    | Animal species: dog, cat, rabbit            | Yes      |
| age           | integer | Age in years                                | Yes      |
| status        | enum    | Current status: available, adopted, foster  | Yes      |
| arrivalDate   | date    | Date when the animal arrived at the shelter | Yes      |
| personality   | object  | Character traits and behavior               | No       |
| technicalData | object  | Size, weight, color of the animal           | No       |
| medicalStatus | enum    | General health status                       | No       |

> Note: This endpoint performs a full update. All required fields must be included in the request body.

**Example Request Body:**

```json
{
  "name": "Charlie",
  "species": "dog",
  "age": 4,
  "status": "adopted",
  "arrivalDate": "2026-02-11",
  "personality": {
    "friendly": true,
    "playful": true
  },
  "technicalData": {
    "size": "medium",
    "weight": 19,
    "color": "black"
  },
  "medicalStatus": "healthy"
}
```

---

## Response Fields

See [Animals Overview](animals-overview.md) for full field descriptions.

---

## Response

### 200 OK

```json
{
  "id": "a125",
  "name": "Charlie",
  "species": "dog",
  "age": 4,
  "status": "adopted",
  "arrivalDate": "2026-02-11",
  "personality": {
    "friendly": true,
    "playful": true
  },
  "technicalData": {
    "size": "medium",
    "weight": 19,
    "color": "black"
  },
  "medicalStatus": "healthy"
}
```

> Note: The response returns the updated animal object.

## Response Codes

| HTTP Code | Meaning                                |
|-----------|----------------------------------------|
| 200       | Successfully updated the animal        |
| 400       | Invalid request body                   |
| 404       | Animal with the specified ID not found |
| 500       | Server error                           |
