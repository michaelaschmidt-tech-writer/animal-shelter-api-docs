# GET /success/{id}

Retrieve the details of a single success story by its unique ID.

---

## Endpoint

`GET /success/{id}`

---

## Path Parameter:

| Parameter | Type   | Description                            | Required |
|-----------|--------|----------------------------------------|----------|
| id        | string | Unique identifier of the success story | Yes      |

**Example:** 

`GET /success/s789`

This request will return the success story with ID s789.

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
  "description": "When Bella first arrived at the shelter, she was so scared she barely lifted her head. She refused food for days and hid in the back of her kennel. But the Müller Family brought patience, calm energy, and kindness. Today, Bella loves long walks in the woods, proudly claims her place on the couch, and has even befriended the family's cats. From a frightened soul to a happy, curious companion — Bella finally found her forever home.",
  "adoptionDate": "2026-02-05",
  "adopter": "Müller Family"
}
```

### 404 Not Found

```json
{
  "error": "Success story with ID 's999' not found."
}
```

> Note: If the specified ID does not exist, a 404 Not Found response is returned.

## Response Codes

| HTTP Code | Meaning                                        |
|-----------|------------------------------------------------|
| 200       | Successfully returned the success story        |
| 404       | Success story with the specified ID not found  |
| 500       | Server error                                   |
