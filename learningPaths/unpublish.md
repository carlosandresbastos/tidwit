**LEARNING PATHS**
=============

### learningPath.unpublish

Publishes an existing learning Path

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/learningPath.unpublish |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "6d1dd1cf-25e7-49f3-bb5a-a8758e43521b
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |         | Unique identifier of the learning Path |
