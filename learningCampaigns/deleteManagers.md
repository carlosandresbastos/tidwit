**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.deleteManagers

Deletes managers from an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.deleteManagers      |
|----------------------------|-------------------------------------------------------------------|
| **HTTP method**            | POST                                                              |
| **Accepted content types** | application/json                                                  |

**Request**

```json
{
  "id": "c91a1717-f20e-432d-b2bc-68b2c290d8f8",
  "managers": [
    "8b1864f2-ece9-4df6-a78a-556caafd9887"
  ]
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type**  | **Length** | **Req** | **Description**                            |
|----------------|-----------|------------|---------|------------------------------------------- |
| id             | guid      |            | Y       | Unique identifier of the learning campaign |
| managers       | guid array|            | Y       | List of unique identifiers of the managers |