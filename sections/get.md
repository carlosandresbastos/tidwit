**SECTIONS**
============

### sections.get

Gets an existing section.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/sections.get |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```text
https://<base-url>/api/sections.get?id=6d1dd1cf-25e7-49f3-bb5a-a8758e43521b
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

| **Field Name** | **Type** | **Length** | **Req** | **Description**                                                        |
|----------------|----------|------------|---------|------------------------------------------------------------------------|
| id             | guid     |            |         | Unique identifier of the section                                       |
| name           | string   | 256        | Y       | Name of the section                                                    |
| menuHeadingID  | guid     |            |         | Identifies the menu heading under which the section is to be displayed |
| comments       | string   |            |         | Additional info                                                        |
