**SECTIONS**
============

### sections.list

Gets a list of sections based on a search criteria

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/sections.list |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```text
https://<base-url>/api/v2.0/sections.list?name=\<sectionname\>&offset=1&limit=10&sortBy=1
```

**Arguments**

| **Field Name** | **Type** | **Length** | **Comments**                         |
|----------------|----------|------------|--------------------------------------|
| **name**       | string   |            | Unique identifier                    |
| **offset**     | Integer  |            | Starting record                      |
| **limit**      | Integer  |            | Number of records to return          |
| **sortBy**     | Integer  |            | 0,1=Name Ascending                   |
|                |          |            | -1=Name Descending                   |

**Response**

```json
{
    "offset": 1,
    "limit": 2,
    "totalRecords": 17,
    "data": [{
        "id": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
        "name": "Training",
        "menuHeadingID": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
        "comments": ""
    },
    {
        "id": "3b8ba42d-af29-472f-b448-fd905ec6c355",
        "name": "Featured",
        "menuHeadingID": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
        "comments": ""
    }]
}

```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                                                        |
|----------------|----------|------------|---------|------------------------------------------------------------------------|
| id             | guid     |            |         | Unique identifier of the menu heading                                  |
| name           | string   | 256        | Y       | Name of the menu heading                                               |
| menuHeadingID  | guid     |            |         | Identifies the menu heading under which the section is to be displayed |
| comments       | string   |            |         | Additional info                                                        |

