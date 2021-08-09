**REPORTS**
=================

### reports.getLearningPathsCompletions

Returns a list of learning paths completions in a period of time

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/reports.getLearningPathsCompletions |
|----------------------------|-------------------------------------------------------------------|
| **HTTP method**            | GET                                                               |
| **Accepted content types** | application/json                                                  |

**Request**
`
https://<base-url>/api/v2.0/reports.getLearningPathsCompletions?beginDate=<beginDate>&endDate=<endDate>offset=10&limit=1&status=all&format=json
`

**Arguments**

| **Field Name** | **Type**       | **Length** | **Comments**                                                           |
|----------------|----------------|------------|----------------------------------------------------------------------- |
| **beginDate**  | datetimeoffset |            | e.g. 2019-02-18T00:00:00.000-05:00                                     |
| **endDate**    | datetimeoffset |            | e.g. 2019-02-19T00:00:00.000-05:00                                     |
| **format**     | string         |            | json or csv                                                             |

**Response**

**Json**

```json
{
    "offset": 1,
    "limit": 20,
    "totalRecords": 2,
    "data": [
    {
        "user": {
            "firstName": "Anil ",
            "lastName": "Sooraj",
            "email": "asooraj@tidwit.com",
            "ssoID": "a12jf78"
        },
        "learningPath": {
            "id": "a26348cd-7dd9-4ead-8764-4fec8ad8e31b",
            "name": "Database Design"
        },
        "completionDate": "2019-01-02T15:34:04.667+00:00",
        "status": "Completed"
    },
    {
        "user": {
            "firstName": "John",
            "lastName": "Milhorn",
            "email": "jmilhorn@acme.com",
            "ssoID": "h67kl45"
        },
        "learningPath": {
            "id": "d6ea7c46-63be-4ace-8661-cf73c5da5bb0",
            "name": "Blockchain development"
        },
        "completionDate": "2019-01-03T02:36:19.397+00:00",
        "status": "Completed"
    }],
    "eTag": "DC0C5AD6F520B7093640400A0CEE9676"
}

```

**Csv**

```text
"FirstName","LastName","Email","SSOID","LearningPathID","LearningPathTitle","EnrolledDate","CompletionDate","Status"
"John Doe ","MPN","mpnuser@tidwit.com","","7cbc41b3-e804-4611-b699-a64f72506ad3","LearningPathTitle","5/15/2018 2:45:50 AM +00:00","","Started"
"John Doe ","MPN","mpnuser@tidwit.com","","0ac649fe-e40d-45c1-b13b-25ed86acc345","LearningPathTitle","5/15/2018 3:01:01 AM +00:00","","Started"
"John Doe ","Acce","useracme@tidwit.com","","0ac649fe-e40d-45c1-b13b-25ed86acc345","LearningPathTitle","6/11/2018 4:17:07 PM +00:00","","Started"
"John Doe ","test","useracme02@tidwit.com","","9620544c-d788-4a98-ade0-068784edf608","LearningPathTitle","3/6/2019 11:55:53 PM +00:00","","Started"

```

**Fields**

| **Field Name**   | **Type**       | **Length** | **Req** | **Description**                        |
|------------------|----------------|------------|---------|----------------------------------------|
| firstName        | string         |            | Y       | User’s first name                      |
| lastName         | string         |            | Y       | User’s last name                       |
| email            | string         |            | Y       | User’s email                           |
| ssoID            | String         |            | N       | Unique identifier of user for SSO      |
| id               | Guid           |            | Y       | Unique identifier of the learning path |
| Name             | String         |            | Y       | Name of content item                   |
| completionDate   | Datetimeoffset |            | Y       | Date of completion                     |
| status           | string         |            | Y       | Assigned, Started, In Progress, Completed  |
