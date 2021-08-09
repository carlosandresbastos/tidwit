**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.deleteLearningPaths

Deletes learning paths from an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.deleteLearningPaths |
|----------------------------|-------------------------------------------------------------------|
| **HTTP method**            | POST                                                              |
| **Accepted content types** | application/json                                                  |

**Request**

```json
{
  "id": "c91a1717-f20e-432d-b2bc-68b2c290d8f8",
  "learningPaths": [
    "3b8ba42d-af29-472f-b448-fd905ec6c355"
  ]
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type**  | **Length** | **Req** | **Description**                                    |
|----------------|-----------|------------|---------|--------------------------------------------------- |
| id             | guid      |            | Y       | Unique identifier of the learning campaign         |
| learningPaths  | guid array|            | Y       | List of unique identifiers of the learning paths   |