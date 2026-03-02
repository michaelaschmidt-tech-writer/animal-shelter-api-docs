# DELETE /success/{id}

Delete an existing success story from the shelter system.

---

## Endpoint

`DELETE /success/{id}`

---

## Path Parameters

| Parameter | Type   | Description                            | Required |
|-----------|--------|----------------------------------------|----------|
| id        | string | Unique identifier of the success story | Yes      |

---

## Response

### 204 No Content

*No response body*

> Note: The success story is permanently removed from the system.

## Response Codes

| HTTP Code | Meaning                                       |
|-----------|-----------------------------------------------|
| 204       | Success story successfully deleted            |
| 404       | Success story with the specified ID not found |
| 500       | Server error                                  |
