**USERS**
=================

### users.getPermissions

Gets permissions for an existing user.

**Facts**

| **URL**                    |  https://[base-url]/api/v2.0/users.getPermissions |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```text
https://<base-url>/api/v2.0/users.getPermissions?id=4f8813cc-ac22-4aa1-bf23-bd15655948c1
```

**Response**

```json
{
  "permissions": [
    "Reports"
  ],
  "eTag": "80946C5BCB00728529EA9E3CD3F31264"
}
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |    y    | Unique identifier of the user         |