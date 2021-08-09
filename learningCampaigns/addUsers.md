**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.addUsers

Adds users to an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.addUsers         |
|----------------------------|----------------------------------------------------------------|
| **HTTP method**            | POST                                                           |
| **Accepted content types** | application/json                                               |

**Request**

```json
{
  "id": "c91a1717-f20e-432d-b2bc-68b2c290d8f8",
  "users": [
    "jdoe@acme.com",
    "msmith@acme.com"
  ]
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type**    | **Length** | **Req** | **Description**                            |
|----------------|-------------|------------|---------|------------------------------------------- |
| id             | guid        |            | Y       | Unique identifier of the learning campaign |
| users          | string array|            | Y       | List of user emails                        |
