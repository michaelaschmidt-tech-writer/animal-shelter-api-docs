# Success Resource Overview

The Success resource represents all recorded adoption success stories in the animal shelter.
It includes emotional adoption stories, the adopter information, references to the adopted animal, and metadata such as the adoption date and optional photo uploads.
This resource is part of the Animal Shelter Management API and is designed to support internal documentation as well as social‑media‑ready storytelling.

---

## Success Story Object

Each success story has the following structure:

```json
{
  "id": "s789",
  "animalId": "a123",
  "title": "Bella found her forever home!",
  "description": "When Bella first arrived at the shelter, she was so scared she barely lifted her head. She refused food for days and hid in the back of her kennel. But the Müller Family brought patience, calm energy, and kindness. Today, Bella loves long walks in the woods, proudly claims her place on the couch, and has even befriended the family's cats. From a frightened soul to a happy, curious companion — Bella finally found her forever home.",
  "adoptionDate": "2026-02-05",
  "adopter": "Müller Family",
  "photoUrl": null
}
```

## Fields Explanation 

| Field          | Type    | Description                                                            |
|----------------|---------|------------------------------------------------------------------------|
| id             | string  | Unique identifier for the success story                                |
| animalId       | string  | ID of the adopted animal (see [Animals Overview](animals-overview.md)) |
| title          | string  | Short headline summarizing the story                                   |
| description    | string  | Full text describing the animal’s adoption journey                     |
| adoptionDate   | date    | Date when the animal was officially adopted                            |
| adopter        | string  | Name of the person or family who adopted the animal                    |
| photoUrl       | string  | URL of the success story photo (nullable, added via photo upload)      |

## Resource Endpoints Overview

The Success resource supports the following REST operations:

| HTTP Method | Endpoint            | Description                                |
|-------------|---------------------|--------------------------------------------|
| GET         | /success            | Retrieve a list of all success stories     |
| GET         | /success/{id}       | Retrieve details of a single success story |
| POST        | /success            | Create a new success story                 |
| PUT         | /success/{id}       | Update an existing success story           |
| DELETE      | /success/{id}       | Delete a success story                     |
| POST        | /success/{id}/photo | Upload a photo for a success story         |
