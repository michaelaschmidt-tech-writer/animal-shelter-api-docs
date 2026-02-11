# POST /animals

Add a new animal to the shelter.

---

## Endpoint

`POST /animals`

---

## Request Body

| Field         | Type     | Description                                | Required |
|---------------|---------|---------------------------------------------|----------|
| name          | string  | Name of the animal                          | Yes      |
| species       | enum    | Animal species: dog, cat, rabbit            | Yes      |
| age           | integer | Age in years                                | Yes      |
| status        | enum    | Current status: available, adopted, foster  | Yes      |
| arrivalDate   | date    | Date when the animal arrived at the shelter | Yes      |
| personality   | object  | Character traits and behavior               | No       |
| technicalData | object  | Size, weight, color of the animal           | No       |
| medicalStatus | enum    | General health status                       | No       |

**Example Request Body:**

```json
{
  "name": "Charlie",
  "species": "dog",
  "age": 3,
  "status": "available",
  "arrivalDate": "2026-02-11",
  "personality": {
    "friendly": true,
    "playful": false
  },
  "technicalData": {
    "size": "medium",
    "weight": 18,
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

### 201 Created

```json
{
  "id": "a125",
  "name": "Charlie",
  "species": "dog",
  "age": 3,
  "status": "available",
  "arrivalDate": "2026-02-11",
  "personality": {
    "friendly": true,
    "playful": false
  },
  "technicalData": {
    "size": "medium",
    "weight": 18,
    "color": "black"
  },
  "medicalStatus": "healthy"
}
```

>Note: The response returns the full details of the newly created animal, including the automatically assigned id.

## Response Codes

| HTTP Code | Meaning                       |
|-----------|-------------------------------|
| 201       | Animal successfully created   |
| 400       | Invalid request body          |
| 500       | Server error                  |
