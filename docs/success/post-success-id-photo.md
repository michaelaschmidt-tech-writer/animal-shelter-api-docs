# POST /success/{id}/photo

Upload a photo for an existing success story.

---

## Endpoint

`POST /success/{id}/photo`

---

## Description

Uploads an image file (e.g., JPEG or PNG) and links it to the specified success story.
The file must be sent as multipart/form-data.

---

## Path Parameters

| Parameter | Type   | Description                            | Required |
|-----------|--------|----------------------------------------|----------|
| id        | string | Unique identifier of the success story | Yes      |

---

## Request Body

Content Type: multipart/form-data

| Field         | Type     | Description                                | Required |
|---------------|----------|--------------------------------------------|----------|
| file          | binary   | Image file (JPEG or PNG)                   | Yes      |

**Example Request Body:**

Content-Disposition: form-data; name="file"; filename="success-photo-bella.jpg"
Content-Type: image/jpeg

---

## Response

### 200 OK

```json
{
  "id": "s789",
  "photoUrl": "https://cdn.shelter.com/success/s789.jpg"
}
```

## Response Codes

| HTTP Code | Meaning                                       |
|-----------|-----------------------------------------------|
| 200       | Photo uploaded successfully                   |
| 400       | Invalid or missing file                       |
| 404       | Success story with the specified ID not found |
| 500       | Server error                                  |
