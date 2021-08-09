**LEARNING PATHS**
=============

### learningPath.getItems

Returns a list of content items in an existing learning Path

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningPath.getItems |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**


```text
https://<base-url>/api/v2.0/learningPath.getItems?id=\<learningPathID\>&offset=1&limit=10
```


**Arguments**

| **Field Name** | **Type** | **Length** | **Comments**                           |
|----------------|----------|------------|----------------------------------------|
| **id**         | string   |            | Unique identifier of the learning Path |
| **offset**     | integer  |            | Starting record                        |
| **limit**      | integer  |            | Number of records to return            |

**Request**

```json
{
    "offset": 1,
    "limit": 2,
    "totalRecords": 17,
    "data": [
    {
        "itemID": "ebc11c6c-9695-49a0-a5e6-c0098af82957",
        "cid": "a9bd03fd-9730-0c2c-df2f-1e199d578c5c",
        "name:: "Course 1",
        "description": "Course 1 Description",
        "thumbnail": {
            "type": "default",
            "url": "https://blob.ontidwit.com/image/e0a3710c-7255-fd62-77d6-7b50af6c848f"
        }
    },
    {
        "itemID": "14f54cae-373a-5df9-dad1-97d3ae933dda",
        "cid": "861e9ea0-656d-3c71-a636-b1abc7053063",
        "name:: "Course 2",
        "description": "Course 2 Description",
        "thumbnail": {
            "type": "default",
            "url": "https://blob.ontidwit.com/image/fc69a928-2011-2791-b91c-9a67d3a840d8"
        }
    }
    ]
}

```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                             |
|----------------|----------|------------|---------|---------------------------------------------|
| id             | guid     |            | Y       | Unique identifier of the learning Path      |
| itemID         | guid     |            | Y       | Unique identifier of the learning Path item |
| cid            | guid     |            | Y       | Unique identifier of the content item       |
| name           | gtring   |            | Y       | Name of content item                        |
| description    | string   |            | N       | Description of the content item             |
| url            | string   |            | N       | Link to the thumbnail image                 |

