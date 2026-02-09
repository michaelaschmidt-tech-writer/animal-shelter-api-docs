# API Overview

The Animal Shelter Management API provides access to data and operations related to animals, adoptions, and shelter management within an animal shelter.

The API is designed according to REST principles and uses standard HTTP methods and response codes.

## Base URL

https://api.animalshelter.example/v1

> Note: This API is fictional. The base URL is provided for documentation purposes only.

## Core Resources

The following core resources are available:

- **Animals**  
  Animals currently registered in the shelter, including basic information, personality traits, and technical data.

- **Adopters**  
  Individuals interested in adopting animals.

- **Adoptions**  
  Adoption processes linking animals and adopters.

- **Medical Records**  
  Medical history entries associated with animals.

- **Staff**  
  Employees working at the animal shelter.

## Data Formats

- All request and response bodies use JSON
- Dates and times follow the ISO 8601 standard
- UTF-8 encoding is used throughout the API
