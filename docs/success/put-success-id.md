# PUT /success/{id}

Update an existing success story in the shelter system.

---

## Endpoint

`PUT /success/{id}`

---

## Path Parameters

| Parameter | Type   | Description                            | Required |
|-----------|--------|----------------------------------------|----------|
| id        | string | Unique identifier of the success story | Yes      |

---

## Request Body

| Field        | Type   | Description                                          | Required |
|--------------|--------|------------------------------------------------------|----------|
| animalId     | string | Unique identifier of the adopted animal              | Yes      |
| title        | string | Short headline describing the story                  | Yes      |
| description  | string | Detailed text about the animal’s adoption journey    | Yes      |
| adoptionDate | date   | Date when the animal was adopted                     | Yes      |
| adopter      | string | Name of the person or family who adopted the animal  | Yes      |

> Note: This endpoint performs a full update. All required fields must be included in the request body.

**Example Request Body:**

```json
{
  "animalId": "a123",
  "title": "Bella found her forever home!",
  "description": "When Bella first arrived at the shelter, she was frightened and withdrawn. But with patience and love from the Müller Family, she slowly opened up and is now a happy and confident companion.",
  "adoptionDate": "2026-02-05",
  "adopter": "Müller Family"
}
```

---

## Response Fields

See [Success Overview](success-overview.md) for full field descriptions.

---

## Response

### 200 OK

```json
{
  "id": "s789",
  "animalId": "a123",
  "title": "Bella found her forever home!",
  "description": "When Bella first arrived at the shelter, she was frightened and withdrawn. But with patience and love from the Müller Family, she slowly opened up and is now a happy and confident companion.",
  "adoptionDate": "2026-02-05",
  "adopter": "Müller Family"
}
```

> Note: The response returns the updated success story object.

## Response Codes

| HTTP Code | Meaning                                       |
|-----------|-----------------------------------------------|
| 200       | Successfully updated the success story        |
| 400       | Invalid request body                          |
| 404       | Success story with the specified ID not found |
| 500       | Server error                                  |
