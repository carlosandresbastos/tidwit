**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.submit

Submits an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.submit |
|----------------------------|------------------------------------------------------|
| **HTTP method**            | POST                                                 |
| **Accepted content types** | application/json                                     |

**Request**

```json
{
  "id": "c91a1717-f20e-432d-b2bc-68b2c290d8f8"
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name**  | **Type** | **Length** | **Req** | **Description**                                                        |
|-----------------|----------|------------|---------|------------------------------------------------------------------------|
| id              | guid     |            |         | Unique identifier of the learning campaign                             |
