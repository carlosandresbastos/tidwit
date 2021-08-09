**REPORTS**
=================

### reports.getUsers

Returns a list of users

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/reports.getUsers |
|----------------------------|-------------------------------------------------------------|
| **HTTP method**            | GET                                                         |
| **Accepted content types** | application/json                                            |

**Request**
`
https://<base-url>/api/v2.0/reports.getUsers?status=<status>&format=json&offset=10&limit=1&status=all
`

**Arguments**

| **Field Name** | **Type**       | **Length** | **Comments**                                               |
|----------------|----------------|------------|------------------------------------------------------------|
| **status**     | string         |            |User status. One of these: all, active, disabled|
| **format**     | string         |            |Report format. One of these: json or csv                                                 |


**Response**

**json** 

```json
{
  "offset": 1,
  "limit": 20,
  "totalRecords": 3,
  "data": [
    {
      "firstName": "Martin",
      "lastName": "Nichols",
      "email": "nichols@acme.com",
      "createdDate": "2019-03-27T18:19:54.883"
    },
    {
      "firstName": "Nicos",
      "lastName": "Kerkides",
      "email": "nicos.kerkides@acme.com"
      "createdDate": "2014-12-10T02:33:40.82",
      "lastLoginDate": "2014-12-10T02:36:06.06"
    },
    {
      "firstName": "John",
      "lastName": "Rhodes",
      "email": "John@acme.com",
      "createdDate": "2018-12-13T18:27:09.73"
    },
  ],
  "eTag": "6A623A1971A03B73C4A7D448D23EF69E"
}
```

**Csv**

```text
"FirstName","LastName","Email","SSOID","CreatedDate","LastLoginDate"
"Martin","Nichols","nichols@acme.com","nichols@acme.com","2019-03-27T18:19:54.883",""
"Nicos","Kerkides","nicos.kerkides@acme.com","nicos.kerkides@acme.com","2014-12-10T02:33:40.82","2014-12-10T02:36:06.06"
"John","Rhodes","John@acme.com","John@acme.com","2018-12-13T18:27:09.73",""
```

**Fields**

| **Field Name**   | **Type**       | **Length** | **Req** | **Description**                       |
|------------------|----------------|------------|---------|---------------------------------------|
| firstName        | string         |            | Y       | User’s first name                     |
| lastName         | string         |            | Y       | User’s last name                      |
| email            | string         |            | Y       | User’s email                          |
| ssoID            | string         |            | N       | Unique identifier of user for SSO     |
| createdDate      | datetime       |            | Y       | Date of user's creation               |
| lastLoginDate    | datetime       |            | N       | Last Login Date                        |
