**SECTIONS**
============

### sections.update

Updates an existing section.

**Facts**

| **URL**                    |   https://[instance-root-url]/api/v2.0/sections.update|
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "name": "Data and AI",
    "menuHeadingID": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "comments": "Database / reporting training courses"
}

```

**Response**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "name": "Data and AI",
    "menuHeadingID": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "comments": "Database / reporting training courses"
}
```

**Fields**

| **Field Name**    | **Type** | **Length** | **Comments**                                                           |
|-------------------|----------|------------|------------------------------------------------------------------------|
| **id**            | guid     |            | Unique identifier                                                      |
| **name**          | string   | 256        | Name of the section                                                    |
| **menuHeadingID** | guid     |            | Identifies the menu heading under which the section is to be displayed |
| **comments**      | string   |            | Additional info                                                        |

