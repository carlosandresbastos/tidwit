**MENU HEADINGS**
=================

### menuHeadings.create

Creates a new menu heading.

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/menuHeadings.create|
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "name": "Solutions",
    "comments": "For solution architects"
}

```

**Response**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b",
    "name": "Solutions",
    "comments": "For solution architects"
}
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |         | Unique identifier of the menu heading |
| name           | string   | 256        | Y       | Name of the menu heading              |
| comments       | string   |            | N       | Additional info                       |