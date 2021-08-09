**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.get

Gets an existing learning campaign.

**Facts**

| **URL**                    |   https://[base-url]/api/v2.0/learningCampaigns.get |
|----------------------------|-----------------------------------------------------|
| **HTTP method**            | GET                                                 |
| **Accepted content types** | application/json                                    |

**Request**


```text
https://\<base-url\>/api/v2.0/learningCampaigns.get?id=c91a1717-f20e-432d-b2bc-68b2c290d8f8
```

**Response**

```json
{
  "id": "c91a1717-f20e-432d-b2bc-68b2c290d8f8",
  "name": "mjuan",
  "startDate": "2019-03-21",
  "endDate": "2019-03-21",
  "status": "Unsubmitted",
  "emailSettings": {
    "subject": "NEW ACME CONTENT",
    "header": "This is new content released by acme",
    "footer": "Enjoy your learning..."
  }
}
```

**Fields**

| **Field Name**  | **Type** | **Length** | **Req** | **Description**                                                        |
|-----------------|----------|------------|---------|------------------------------------------------------------------------|
| id              | guid     |            |         | Unique identifier of the learning campaign                             |
| name            | string   | 256        |         | Name of the learning campaign                                          |
| startDate       | string   |            |         | Start date of learning campaign                                        |
| endDate         | string   |            |         | End date of learning campaign                                          |
| status          | string   |            |         | Status of learning campaign                                            |
| subject         | string   |            |         | Subject of learning campaign email                                     |
| header          | string   |            |         | Heder of learning campaign email                                       |
| footer          | string   |            |         | Footer of learning campaign email                                      |

