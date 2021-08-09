**USERS**
=================

### users.update

Updates an existing user.

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/users.update |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
"id": "4f8813cc-ac22-4aa1-bf23-bd15655948c1",
  "firstName": "mateo",
  "lastName": "nichos",
  "email": "mate@tidwit.com",
  "jobTitle": "developer",
  "phoneNumber": "+1 7096265088",
  "status": "enable",
  "defaultLanguageCode": "en",
  "address": {
    "addressLine1": "136 Adams Street NW",
    "addressLine2": "string",
    "city": "New York City",
    "stateOrProvince": "Nueva York",
    "postalCode": "200004",
    "countryCode": "us"
  }
  
}
```

**Response**

```json
{
 "id": "4f8813cc-ac22-4aa1-bf23-bd15655948c1",
  "firstName": "mateo",
  "lastName": "nichos",
  "email": "mate@tidwit.com",
  "jobTitle": "developer",
  "phoneNumber": "+1 7096265088",
  "status": "Enabled",
  "defaultLanguageCode": "en",
  "address": {
    "addressLine1": "136 Adams Street NW",
    "addressLine2": "string",
    "city": "New York City",
    "stateOrProvince": "Nueva York",
    "postalCode": "200004",
    "countryCode": "us"
}
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
|id              |guid      |            |         |Unique identifier of the user          |
|firstName       |string    |            |   y     |First name of user                     |
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
