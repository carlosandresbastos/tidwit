**MENU HEADINGS**
=================

### menuHeadings.setPositions

Updates the positions of menu headings.

**Facts**

| **URL**                    |  https://[instance-root-url]/api/v2.0/menuHeadings.setPositions |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
[{
    "id": "6D1DD1CF-25E7-49F3-BB5A-A8758E43521B",
    "position", 1
},
{
    "id": "E9E4205E-A1A5-4B4A-811C-5E20E01DB67C",
    "position", 2
}]

```

**Response**

```json
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            | Y       | Unique identifier of the menu heading |
| Position       | int      |            | Y       | Position of menu heading              |
