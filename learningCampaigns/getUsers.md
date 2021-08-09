**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.getUsers

Returns a list of users in an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.getUsers |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**


```text
https://<base-url>/api/v2.0/learningCampaigns.getUsers?id=c91a1717-f20e-432d-b2bc-68b2c290d8f8
```


**Arguments**

| **Field Name** | **Type** | **Length** | **Comments**                              |
|----------------|----------|------------|-------------------------------------------|
| **id**         | string   |            | Unique identifier of the learning campaign|


**Request**

```json
{
  "offset": 1,
  "limit": -1,
  "totalRecords": 2,
  "data": [
    {
      "email": "jdoe@acme.com",
      "firstName": "Jhon",
      "lastName": "Doe",
      "status": "Unsubmitted"
    },
    {
      "email": "jsmith@acme.com",
      "firstName": "Jane",
      "lastName": "Smith",
      "status": "Unsubmitted"
    }
  ],
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                             |
|----------------|----------|------------|---------|---------------------------------------------|
| id             | guid     |            | Y       | Unique identifier of the user               |
|firstName       |string    |            | Y       | First name of user                          |
|lastName        |string    |            | Y       | Last name of user                           |
|email           |string    |            | Y       | User email                                  |
