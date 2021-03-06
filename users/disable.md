**USERS**
=================

### user.disable

Disables an existing user.

**Facts**

| **URL**                    |  https://[base-url]/api/v2.0/users.disable |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
  "id": "4f8813cc-ac22-4aa1-bf23-bd15655948c1"
}
```

**Response**

```text
HTTP 200 OK 
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |    y    | Unique identifier of the user         |