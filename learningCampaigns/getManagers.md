**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.getManagers

Returns a list of managers in an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.getUsers |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**


```text
https://<base-url>/api/v2.0/learningCampaigns.getManagers?id=c91a1717-f20e-432d-b2bc-68b2c290d8f8
```


**Arguments**

| **Field Name** | **Type** | **Length** | **Comments**                              |
|----------------|----------|------------|-------------------------------------------|
| **id**         | string   |            | Unique identifier of the learning campaign|


**Request**

```json
{
  "managers": [
    {
      "id": "8b1864f2-ece9-4df6-a78a-556caafd9887",
      "firstName": "Jhon",
      "lastName": "Doe",
      "email": "jdoe@acme.com",
      "roles": [
        "Admin"
      ]
    },
    {
      "id": "B4443BBF-E30A-4076-8852-905891D55D4B",
      "firstName": "Jane",
      "lastName": "Smith",
      "email": "jsmith@acme.com",
      "roles": [
        "Admin"
      ]
    }
  ],
}
```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type**     | **Length** | **Req** | **Description**                             |
|----------------|--------------|------------|---------|---------------------------------------------|
| id             | guid         |            | Y       | Unique identifier of the User               |
| firstName      | string       |            | Y       | First Name of User                          |
| lastName       | string       |            | Y       | Last name of user                           |
| email          | string       |            | Y       | User-email                                  |
| roles          | string array |            | Y       | Manager roles: Admin or View                |