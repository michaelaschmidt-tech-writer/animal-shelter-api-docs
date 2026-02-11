# GET /animals

Retrieve a list of all animals currently registered in the shelter.
You can filter the results using optional query parameters.

---

## Endpoint

`GET /animals`

---

## Query Parameters

| Parameter | Type    | Description                                                   | Required |
|-----------|---------|---------------------------------------------------------------|----------|
| status    | string  | Filter animals by adoption status: available, adopted, foster | No       |
| species   | string  | Filter animals by species: dog, cat, rabbit                   | No       |
| minAge    | integer | Filter animals older than or equal to this age                | No       |
| maxAge    | integer | Filter animals younger than or equal to this age              | No       |

**Example:** 

`GET /animals?status=available`

This request will return all animals that are available for adoption.

**Example of combining multiple filters:**

`GET /animals?status=available&species=dog&minAge=2`

This request will return all animals that:  
- have the status `available`  
- are of species `dog`  
- are at least 2 years old

---

## Response Fields

See [Animals Overview](animals-overview.md) for full field descriptions.

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

>Note: If no animals match the filter criteria, an empty list [] is returned with 200 OK.

## Response Codes

| HTTP Code | Meaning                       |
|-----------|-------------------------------|
| 200       | Successfully returned animals |
| 500       | Server error                  |
