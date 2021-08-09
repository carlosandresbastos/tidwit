**MENU HEADINGS**
=================

### menuHeadings.list

Get a list of existing menu headings.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/menuHeadings.list |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```json
https://<base-url>/api/v2.0/menuHeadings.list?name=\<menuheadingname\>&offset=1&limit=10&sortBy=1
```

**Arguments**

| **Field Name** | **Type** | **Length** | **Comments**                                  |
|----------------|----------|------------|-----------------------------------------------|
| **name**       | string   |            | Unique identifier                             |
| **offset**     | Integer  |            | Starting record                               |
| **limit**      | Integer  |            | Number of records to return                   |
| **sortBy**     | Integer  |            | 0=Position                                    |
|                |          |            | 1=Name Ascending -1=Name Descending           |

**Response**

```json
{
    "offset": 1,
    "limit": 2,
    "totalRecords": 17,
    "data": [
    {
        "id": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
        "name": "Training",
        "comments": "",
        "position": 1
    },
    {
        "id": "3b8ba42d-af29-472f-b448-fd905ec6c355",
        "name": "Featured",
        "comments": "",
        "position": 2
    ]
}

```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                                               |
|----------------|----------|------------|---------|---------------------------------------------------------------|
| id             | guid     |            |         | Unique identifier of the menu heading                         |
| name           | string   | 256        | Y       | Name of the menu heading                                      |
| comments       | string   |            |         | Additional info                                               |
| position       | Integer  |            |         | Controls the order of the menu headings in the user interface |
