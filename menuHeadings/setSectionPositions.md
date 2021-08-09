**MENU HEADINGS**
=================

### menuHeadings.setSectionPositions

Updates the positions of sections under a menu heading

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/menuHeadings.setSectionPositions |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
    "sections":[{
        "id": "1b562b42-d56b-4634-8101-4fe2fc6c7648",
        "position": 1
    },
    {
        "id": "5ff689c8-ad0b-40c5-9280-4e486279325e",
        "position": 2
    },
    {
        "id": "6e002b21-561d-414e-9a0e-0bf037ef8930",
        "position": 3
    },
    {
        "id": "0fc92072-86bf-4f62-a8b3-36bd267d6030",
        "position": 4
    }
    ]
}

```

**Response**


```json
HTTP 200 OK
```

**Fields**

| **Field Name**    | **Type** | **Length** | **Req** | **Description**                       |
|-------------------|----------|------------|---------|---------------------------------------|
| id                | guid     |            | Y       | Unique identifier of the menu heading |
| sections.id       | Guid     |            | Y       | Unique identifier of the section      |
| Sections.position | int      |            | Y       | Position of menu heading              |
