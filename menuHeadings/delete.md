**MENU HEADINGS**
=================

### menuHeadings.delete

Updates an existing menu heading.

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/menuHeadings.delete     |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b
}
```

**Response**

```json
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |         | Unique identifier of the menu heading |
