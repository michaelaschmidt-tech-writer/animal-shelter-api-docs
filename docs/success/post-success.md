# POST /success

Create a new success story for an adopted animal.

---

## Endpoint

`POST /success`

---

## Description

Adds a new success story to the shelter system.
Each story links to an existing adopted animal via its animalId.

---

## Request Body

| Field        | Type   | Description                                          | Required |
|--------------|--------|------------------------------------------------------|----------|
| animalId     | string | Unique identifier of the adopted animal              | Yes      |
| title        | string | Short headline describing the story                  | Yes      |
| description  | string | Detailed text about the animal’s adoption journey    | Yes      |
| adoptionDate | date   | Date when the animal was adopted                     | Yes      |
| adopter      | string | Name of the person or family who adopted the animal  | Yes      |

**Example Request Body:**

```json
{
  "animalId": "a123",
  "title": "Bella found her forever home!",
  "description": "When Bella first arrived at the shelter, she was so scared she barely lifted her head. She refused food for days and hid in the back of her kennel. But the Müller Family brought patience, calm energy, and kindness. Today, Bella loves long walks in the woods, proudly claims her place on the couch, and has even befriended the family's cats. From a frightened soul to a happy, curious companion — Bella finally found her forever home.",
  "adoptionDate": "2026-02-05",
  "adopter": "Müller Family"
}
```

---

## Response Fields

See [Success Overview](success-overview.md) for full field descriptions.

---

## Response

### 201 Created

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

## Response Codes

| HTTP Code | Meaning                                 |
|-----------|-----------------------------------------|
| 201       | Success story created successfully      |
| 400       | Invalid request body                    |
| 404       | Animal with the specified ID not found  |
| 500       | Server error                            |
