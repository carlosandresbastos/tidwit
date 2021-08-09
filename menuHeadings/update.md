**MENU HEADINGS**
=================

### menuHeadings.update

Updates an existing menu heading.

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/menuHeadings.update    |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "name": "Training",
    "comments": "For sales reps"
}
```

**Response**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "name": "Training",
    "comments": "For sales reps"
}
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            | Y       | Unique identifier of the menu heading |
| name           | string   | 256        | Y       | Name of the menu heading              |
| comments       | string   |            | N       | Additional info                       |
