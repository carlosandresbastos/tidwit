**LIBRARIES**
=============

### libraries.create

Creates a new library

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/libraries.create|
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "name": "Training Courses",
    "description": "More details about the training courses library",
    "publishedDate": "2019-01-10",
    "parentID": "00000000-0000-0000-0000-000000000000",
    "sectionID": "24e46716-7849-4d30-9593-6470563465cf",
    "defaultTemplate": "TwoColumns",
    "languageCode": "en",
    "appearance": {	
        "icon": "Videos",
        "defaultSort": "Custom",
        "rowsPerPage": 10
    }
}

```

**Response**

```json
{
    "id": "26848f45-aefa-43d2-a255-4d993f65b9fd",
    "name": "Training Courses",
    "description": "More details about the training courses library",
    "publishedDate": "2019-01-10",
    "parentID": "00000000-0000-0000-0000-000000000000",
    "sectionID": "24e46716-7849-4d30-9593-6470563465cf",
    "defaultTemplate": "TwoColumns",
    "languageCode": "en",
    "appearance": {
        "icon": "Videos",
        "defaultSort": "Custom",
        "rowsPerPage": 10
    }
}

```

**Fields**

| **Field Name**  | **Type** | **Length** | **Req** | **Description**                                                        |
|-----------------|----------|------------|---------|------------------------------------------------------------------------|
| id              | guid     |            |         | Unique identifier of the library                                       |
| name            | string   | 256        | Y       | Name of the library                                                    |
| description     | string   |            | N       | Detailed description of the library                                    |
| publishedDate   | date     |            | Y       |                                                                        |
| parentID        | guid     |            | Y       | References the parent library                                          |
| sectionID       | guid     |            | Y       | References a section in the left side menu                             |
| defaultTemplate | enum     |            | Y       | One of: List, TwoColumns, ThreeColumns                                 |
| languageCode    | string   | 2          | Y       | ISO language code                                                      |
| icon            | enum     |            | Y       | One of:                                                                |
| defaultSort     | enum     |            | Y       | One of: PublishedDateAsc, PublishedDateDesc, NameAsc, NameDesc, Custom |
| rowsPerPage     | integer  |            | Y       | Number of record displayed per page                                    |
