# GET /animals

Retrieve a list of all animals currently registered in the shelter.

---

## Endpoint

`GET /animals`

---

## Query Parameters

| Parameter | Type | Description | Required |
|-----------|------|-------------|----------|
| None      | N/A  | This endpoint does not take any parameters | No |

---

## Response

### 200 OK

```json
[
  {
    "id": "a123",
    "name": "Bella",
    "species": "dog",
    "age": 4,
    "status": "available",
    "arrivalDate": "2025-01-10"
  },
  {
    "id": "a124",
    "name": "Max",
    "species": "cat",
    "age": 2,
    "status": "foster",
    "arrivalDate": "2025-01-15"
  }
]
```

## Response Codes

| HTTP Code | Meaning                       |
|-----------|-------------------------------|
| 200       | Successfully returned animals |
| 404       | No animals found              |
| 500       | Server error                  |
