# DELETE /animals/{id}

Delete an existing animal from the shelter.

---

## Endpoint

`DELETE /animals/{id}`

---

## Path Parameters

| Parameter | Type   | Description                     | Required |
|-----------|--------|---------------------------------|----------|
| id        | string | Unique identifier of the animal | Yes      |

---

## Response

### 204 No Content

*No response body*

> Note: The animal is permanently removed from the system.

## Response Codes

| HTTP Code | Meaning                                |
|-----------|----------------------------------------|
| 204       | Animal successfully deleted            |
| 404       | Animal with the specified ID not found |
| 500       | Server error                           |
