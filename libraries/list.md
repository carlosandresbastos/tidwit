**LIBRARIES**
=============

### libraries.list

Gets a list of libraries based on a search criteria

**Facts**

| **URL**                    |  https://[base-url]/api/v2.0/libraries.list |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```text
https://<base-url>/api/v2.0/libraries.list?name=\<libraryName\>&offset=1&limit=10&sortBy=1
```

**Arguments**

| **Field Name**          | **Type** | **Length** | **Comments**                         |
|-------------------------|----------|------------|--------------------------------------|
| **name**                | string   |            | Library name                         |
| **sectionID**           | guid     |            | Section unique identifier            |
| **parentID**            | guid     |            | Parent library unique identifier     |
| **startPublishedDate**  | date     |            |                                      |
| **endPublishedDate**    | date     |            |                                      |
| **startExpirationDate** | date     |            |                                      |
| **endExpirationDate**   | date     |            |                                      |
| **offset**              | integer  |            | Starting record                      |
| **limit**               | integer  |            | Number of records to return          |
| **sortBy**              | integer  |            | 0,1=Name Ascending                   |
|                         |          |            | -1=Name Descending                   |

**Response**

```json
{
    "offset": 1,
    "limit": 2,
    "totalRecords": 17,
    "data": [{
        "id": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
        "name": "Training",
        "description": "Training courses for myProduct",
        "status": "Unpublished",
        "link": "https://acme.ontidwit.com/librairies/training"
    },
    {
        "id": "3b8ba42d-af29-472f-b448-fd905ec6c355",
        "name": "Featured",
        "description": "All featured content",
        "status": "Published",
        "link": "https://acme.ontidwit.com/librairies/featured"
    }]
}

```

**Fields**

| **Field Name**  | **Type** | **Length** | **Req** | **Description**                                                        |
|-----------------|----------|------------|---------|------------------------------------------------------------------------|
| id              | guid     |            |         | Unique identifier of the library                                       |
| name            | string   | 256        | Y       | Name of the library                                                    |
| description     | string   |            | N       | Detailed description of the library                                    |
| publishedDate   | Date     |            | Y       |                                                                        |
| parentID        | Guid     |            | Y       | References the parent library                                          |
| sectionID       | Guid     |            | Y       | References a section in the left side menu                             |
| defaultTemplate | Enum     |            | Y       | One of: List, TwoColumns, ThreeColumns                                 |
| languageCode    | String   | 2          | Y       | ISO language code                                                      |
| icon            | Enum     |            | Y       | One of:                                                                |
| defaultSort     | Enum     |            | Y       | One of: PublishedDateAsc, PublishedDateDesc, NameAsc, NameDesc, Custom |
| rowsPerPage     | Integer  |            | Y       | Number of record displayed per page                                    |
| thumbnail.url   | String   |            |         | Link to download the thumbnail                                         |
