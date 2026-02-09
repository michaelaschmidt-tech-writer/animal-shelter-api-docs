# Animals Resource Overview

The Animals resource represents all animals currently registered in the animal shelter. It includes basic information, personality traits, technical characteristics, and high-level medical status.

This resource is a core part of the Animal Shelter Management API.

---

## Animal Object

Each animal has the following structure:

```json
{
  "id": "a123",
  "name": "Bella",
  "species": "dog",
  "age": 4,
  "status": "available",
  "arrivalDate": "2025-01-10",
  "personality": {
    "friendliness": "high",
    "energyLevel": "medium",
    "notes": "Very good with children"
  },
  "technicalData": {
    "size": "medium",
    "weightKg": 18.5,
    "color": "brown"
  },
  "medicalStatus": "healthy"
}
```

## Fields Explanation 

| Field          | Type     | Description                                |
|----------------|---------|---------------------------------------------|
| id             | string  | Unique identifier for the animal            |
| name           | string  | Name of the animal                          |
| species        | enum    | Animal species: dog, cat, rabbit            |
| age            | integer | Age in years                                |
| status         | enum    | Current status: available, adopted, foster  |
| arrivalDate    | date    | Date when the animal arrived at the shelter |
| personality    | object  | Character traits and behavior               |
| technicalData  | object  | Size, weight, color of the animal           |
| medicalStatus  | enum    | General health status                       |

## Resource Endpoints Overview

The Animals resource supports the following REST operations:

| HTTP Method | Endpoint       | Description                         |
|-------------|----------------|-------------------------------------|
| GET         | /animals       | Retrieve a list of all animals      |
| GET         | /animals/{id}  | Retrieve details of a single animal |
| POST        | /animals       | Add a new animal                    |
| PUT         | /animals/{id}  | Update an existing animal           |
| DELETE      | /animals/{id}  | Delete an animal                    |
