**LIBRARIES**
=============

### libraries.addItems

Adds content items to an existing library

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/libraries.addItems |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "26848f45-aefa-43d2-a255-4d993f65b9fd",
    "items": [
        { 
            "cid": "952e0d33-2a3c-4998-9574-1148aa8d1fde" 
        },
        { 
            "cid": "ff1ab992-56dd-4393-8577-07ee7a7d9d0e" 
        }
    ]
}


```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            | Y       | Unique identifier of the library      |
| cid            | guid     |            | Y       | Unique identifier of the content item |
