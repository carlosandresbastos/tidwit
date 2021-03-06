**MENU HEADINGS**
=================

### menuHeadings.get

Get an existing menu heading.

**Facts**

| **URL**                    |  https://[base-url]/api/v2.0/menuHeadings.get |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```json
https://<base-url>/api/menuHeadings.get?id=6d1dd1cf-25e7-49f3-bb5a-a8758e43521b
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
| id             | guid     |            |         | Unique identifier of the menu heading |
| name           | string   | 256        | Y       | Name of the menu heading              |
| comments       | string   |            |         | Additional info                       |
