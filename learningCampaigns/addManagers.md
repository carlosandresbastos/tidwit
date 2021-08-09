**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.addManagers

Adds managers to an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.addManagers      |
|----------------------------|----------------------------------------------------------------|
| **HTTP method**            | POST                                                           |
| **Accepted content types** | application/json                                               |

**Request**

```json
{
  "id": "c91a1717-f20e-432d-b2bc-68b2c290d8f8",
  "managers": [
    {
      "id": "8b1864f2-ece9-4df6-a78a-556caafd9887",
      "roles": [
        "Admin"
      ]
    }
  ]
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type**     | **Length** | **Req** | **Description**                            |
|----------------|--------------|------------|---------|------------------------------------------- |
| id             | guid         |            | Y       | Unique identifier of the learning campaign |
| id             | guid         |            | Y       | Unique identifier of the manager           |
| roles          | string array |            | Y       | Manager roles: Admin or View               |