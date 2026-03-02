# GET /success

Retrieve a list of all success stories recorded in the shelter system.
You can filter the results using optional query parameters.

---

## Endpoint

`GET /success`

---

## Query Parameters

| Parameter | Type    | Description                                                 | Required |
|-----------|---------|-------------------------------------------------------------|----------|
| animalId  | string  | Return only stories belonging to the specified animal       | No       |
| fromDate  | date    | Return stories with an adoptionDate on or after this date   | No       |
| toDate    | date    | Return stories with an adoptionDate on or before this date  | No       |
| adopter   | string  | Filter stories by adopter name                              | No       |

**Examples:** 

**Example 1: Get all stories for a specific animal**

`GET /success?animalId=a123`

This request will return all success stories belonging to animal a123.

**Example 2: Get all stories from a time range**

`GET /success?fromDate=2026-01-01&toDate=2026-12-31`

This request will return all success stories created in the year 2026.

**Example 3: Filter by adopter**

`GET /success?adopter=Müller`

This request will return all stories where the adopter's name includes “Müller”.

---

## Response Fields

See [Success Overview](success-overview.md) for full field descriptions.

---

## Response

### 200 OK

```json
[
  {
    "id": "s789",
    "animalId": "a123",
    "title": "Bella found her forever home!",
    "description": "When Bella first arrived at the shelter, she was so scared she barely lifted her head. She refused food for days and hid in the back of her kennel. But the Müller Family brought patience, calm energy, and kindness. Today, Bella loves long walks in the woods, proudly claims her place on the couch, and has even befriended the family's cats. From a frightened soul to a happy, curious companion — Bella finally found her forever home.",
    "adoptionDate": "2026-02-05",
    "adopter": "Müller Family"
  },
  {
    "id": "s790",
    "animalId": "a124",
    "title": "Max is now the king of his castle!",
    "description": "Max quickly settled into his new home and immediately claimed every sunny spot he could find.",
    "adoptionDate": "2026-02-12",
    "adopter": "Thompson Family"
  }
]
```

>Note: If no success stories match the filter criteria, an empty list [] is returned with 200 OK.

## Response Codes

| HTTP Code | Meaning                               |
|-----------|---------------------------------------|
| 200       | Successfully returned success stories |
| 500       | Server error                          |
