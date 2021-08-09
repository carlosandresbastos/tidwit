**USERS**
=================

### users.get

Gets an existing user.

**Facts**

| **URL**                    |  https://[base-url]/api/v2.0/users.get |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```text
https://<base-url>/api/v2.0/users.get?id=4f8813cc-ac22-4aa1-bf23-bd15655948c1
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
  },
  "eTag": "B609D5C8FF348AA4E6806207669BFCB8"
}
```

**Fields**


| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
|id              |guid      |            |    y    |Unique identifier of the user          |
|firstName       |string    |            |         |First Name of User                     |
|lastName        |string    |            |         |Last name of user                      |
|email           |string    |            |         |User-email                             |
|jobTitle        |string    |            |         |Job title                              |
|phoneNumber     |string    |            |         |User phone number                      |
|status          |string    |            |         |One of: enable, diasable               |
|defaultLanguageCode|string |            |         |ISO language code                      |
|addressLine1    |userAddress|           |         |Address first line                     |
|addressLine2    |userAddress|           |         |Address first line                     |
|city            |string    |            |         |City                                   |
|stateOrProvince |string    |            |         |State Or Province                      |
|postalCode      |string    |            |         |User's postal code                     |
|countryCode     |string    |            |         |ISO country code                       |
