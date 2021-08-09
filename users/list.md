**USERS**
=================

### users.list

Get a list of existing users.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/users.list |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```text
https://<base-url>/api/v2.0/users.list?firstName=mateo&offset=1&sortBy=1
```

**Arguments**

| **Field Name** | **Type** |**Comments**     |
|----------------|----------|---------------- |
|firstName       |string    |User first name  |
|lastName        |string    |Last name of user|  
|email           |string    |User email       |
|offset          |integer   |Starting record  |
|limit           |integer   |Number of records to return|

|sortBy          |integer   |0,1=Name Ascending, -1=Name Descending|

**Response**

```json
{
  "offset": 1,
  "limit": 20,
  "totalRecords": 35,
  "data": [
    {
      "id": "26f272da-f813-4f77-b77d-96878b252f09",
      "firstName": "mateo",
      "lastName": "Bastos",
      "email": "carlosandresbastos@gmail.com",
      "jobTitle": "",
      "phoneNumber": "8645405463",
      "status": "Enabled"
    },
    {
      "id": "a9a975a4-c59f-4433-83e9-34f9e8f17917",
      "firstName": "mateo",
      "lastName": "LastNameTest",
      "email": "test1b9236fcdfc540b08f365bafa1e73f70@tidwit.com",
      "jobTitle": "",
      "phoneNumber": "8645405463",
      "status": "Enabled"
    },
    {
      "id": "1b1f9e0b-d98d-4a81-b112-6abdfe0d95b6",
      "firstName": "mateo",
      "lastName": "LastNameTest",
      "email": "test22cd35d7-e289-4148-bbf9-b5dd3602246d@tidwit.com",
      "jobTitle": "",
      "phoneNumber": "8645405463",
      "status": "Enabled"
    },
    
  ],
  "eTag": "49E89BDF3105F1EC73E691C96DACC903"
}

```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
|id              |guid      |            |         |Unique identifier of the user          |
|firstName       |string    |            |   y     |First Name of User                     |
|lastName        |string    |            |   y     |Last name of user                      |
|email           |string    |            |   y     |User-email                             |
|jobTitle        |string    |            |         |Job title                              |
|phoneNumber     |string    |            |         |User phone number                      |
|status          |string    |            |         |One of: enable, diasable               |