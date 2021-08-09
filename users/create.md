**USERS**
=================

### users.create

Creates a new user.

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/users.create |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
  "firstName": "martin",
  "lastName": "nichols",
  "email": "nichols@tidwit.com",
  "jobTitle": "developer",
  "phoneNumber": "+1 7096265088",
  "defaultLanguageCode": "en",
  "address": {
    "addressLine1": "136 Adams Street NW",
    "addressLine2": "string",
    "city": "seattle",
    "stateOrProvince": "washington",
    "postalCode": "20001",
    "countryCode": "us"
  },
  "password": "hola12345"
}
```

**Response**

```json
{
  "id": "4f8813cc-ac22-4aa1-bf23-bd15655948c1",
  "firstName": "martin",
  "lastName": "nichols",
  "email": "nichols@tidwit.com",
  "jobTitle": "",
  "phoneNumber": "+1 7096265088",
  "status": "Enabled",
  "defaultLanguageCode": "en",
  "address": {
    "addressLine1": "136 Adams Street NW",
    "addressLine2": "string",
    "city": "seattle",
    "stateOrProvince": "washington",
    "postalCode": "20001",
    "countryCode": "us"
  }
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
|defaultLanguageCode|string |            |   y     |ISO language code                      |
|addressLine1    |userAddress|           |         |Address first line                     |
|addressLine2    |userAddress|           |         |Address first line                     |
|city            |string    |            |         |City                                   |
|stateOrProvince |string    |            |         |State Or Province                      |
|postalCode      |string    |            |         |User's postal code                     |
|countryCode     |string    |            |         |ISO country code                       |
|password        |string    |            |   y     |Password                               |