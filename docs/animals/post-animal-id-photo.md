# POST /animals/{id}/photo

Upload a photo for an existing animal.

---

## Endpoint

`POST /animals/{id}/photo`

---

## Description

Uploads an image file (e.g., JPEG or PNG) and links it to the specified animal.
The file must be sent as multipart/form-data.

---

## Path Parameters

| Parameter | Type   | Description                     | Required |
|-----------|--------|---------------------------------|----------|
| id        | string | Unique identifier of the animal | Yes      |

---

## Request Body

Content Type: multipart/form-data

| Field         | Type     | Description                                | Required |
|---------------|----------|--------------------------------------------|----------|
| file          | binary   | Image file (JPEG or PNG)                   | Yes      |

**Example Request Body:**

Content-Disposition: form-data; name="file"; filename="bella.jpg"
Content-Type: image/jpeg

---

## Response

### 200 OK

```json
{
  "animalId": "a123",
  "photoUrl": "https://cdn.shelter.com/photos/a123.jpg"
}
```

## Response Codes

| HTTP Code | Meaning                                |
|-----------|----------------------------------------|
| 200       | Photo uploaded successfully            |
| 400       | Invalid or missing file                |
| 404       | Animal with the specified ID not found |
| 500       | Server error                           |
