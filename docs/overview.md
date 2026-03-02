# API Overview

The Animal Shelter Management API provides access to data and operations related to animals, success stories, adoptions, and overall shelter management.

The API follows REST principles and uses standard HTTP methods and response codes.

---

## Base URL

https://api.animalshelter.example/v1

> Note: This API is fictional. The base URL is provided for documentation purposes only.

---

## Core Resources

The following core resources are available:

- **Animals**  
  Animals currently registered in the shelter, including basic information, personality traits, technical data, medical status, and optionally a photo uploaded via the photo upload endpoint.

- **Success Stories**  
  Adoption success stories that highlight positive outcomes for animals after they find their new homes.  
  Stories include emotional descriptions, adopter information, adoption dates, optional photos, and a reference to the adopted animal.

- **Adopters**  
  Individuals interested in adopting animals.  
  *(This resource is planned and may be expanded in future versions.)*

- **Adoptions**  
  Adoption processes linking animals and adopters.  
  *(This resource is planned and may be expanded in future versions.)*

- **Medical Records**  
  Medical history entries associated with animals.  
  *(This resource is planned and may be expanded in future versions.)*

- **Staff**  
  Employees working at the animal shelter.  
  *(This resource is planned and may be expanded in future versions.)*

---

## Data Formats

- All request and response bodies use **JSON**
- Dates and times follow the **ISO 8601** standard
- **UTF‑8** encoding is used throughout the API
