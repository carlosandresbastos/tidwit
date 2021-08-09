**REPORTS**
=================

### reports.getContentCompletions

Returns a list of course completions in a period of time

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/reports.getContentCompletions |
|----------------------------|-------------------------------------------------------------|
| **HTTP method**            | GET                                                         |
| **Accepted content types** | application/json                                            |

**Request**
`
https://<base-url>/api/v2.0/reports.getContentCompletions?beginDate=<beginDate>&endDate=<endDate>offset=10&limit=1&format=json
`

**Arguments**

| **Field Name** | **Type**       | **Length** | **Comments**                                               |
|----------------|----------------|------------|------------------------------------------------------------|
| **beginDate**  | datetimeoffset |            | e.g. 2019-02-18T00:00:00.000-05:00                         |
| **endDate**    | datetimeoffset |            | e.g. 2019-02-19T00:00:00.000-05:00                         |
| **format**     | string         |            |json or csv                                                 |


**Response**

**json** 

```json
{
  "offset": 1,
  "limit": 20,
  "totalRecords": 151,
  "data": [
	{
	  "user": {
		"firstName": "Anil ",
		"lastName": "Tester",
		"email": "mpnadmin@tidwit.com"
	  },
	  "content": {
		"cid": "6ea74eef-b57c-4eaa-9b03-5279c1b7e139",
		"name": "Course A"
	  },
	  "status": "Started"
	},
	{
	  "user": {
		"firstName": "Anil ",
		"lastName": "Tester",
		"email": "mpnadmin@tidwit.com"
	  },
	  "content": {
		"cid": "2db291f8-0a19-4dec-a979-2cb8b088858a",
		"name": "Course B"
	  },
	  "status": "Started"
	},
	{
	  "user": {
		"firstName": "Anil ",
		"lastName": "Tester",
		"email": "mpnadmin@tidwit.com"
	  },
	  "content": {
		"cid": "1baa3d5d-1d30-4c43-acab-e822e7e61861",
		"name": "Course C"
	  },
	  "status": "Compled",
	  "completionStatus": "Success"
	},

  ],
  "eTag": "6FA6F70B79D33308AD8AEA4B0FF581CF"
}
```

**Csv**

```text
"FirstName","LastName","Email","SSOID","ContentID","ContentTitle","StartedDate","CompletionDate","Status","CompletionStatus"
"John","Doe","mpn@tidwit.com","E2712","82c67e37-394a-4c50-a252-d8b39f0d4571","Course A","4/13/2018 5:39:15 PM +00:00","","Started","Success"
"John","Doe","mpn@tidwit.com","E2712","406751da-6385-454c-98d2-d951241c3b89","Course B","4/13/2018 5:42:31 PM +00:00","","Started","Success"
"John","Doe","mpn@tidwit.com","E2712","b002856f-e027-450c-ba79-cd49cfcfd7fe","Assessment A","12/20/2017 10:33:00 PM +00:00","","Started","Success"

```

**Fields**

| **Field Name**   | **Type**       | **Length** | **Req** | **Description**                       |
|------------------|----------------|------------|---------|---------------------------------------|
| firstName        | string         |            | Y       | User’s first name                     |
| lastName         | string         |            | Y       | User’s last name                      |
| email            | string         |            | Y       | User’s email                          |
| ssoID            | String         |            | N       | Unique identifier of user for SSO     |
| cid              | Guid           |            | Y       | Unique identifier of content item     |
| Name             | String         |            | Y       | Name of content item                  |
| completionDate   | Datetimeoffset |            | Y       | Date of completion                    |
| status           | String         |            | Y       | Status				                   |
| completionStatus | String         |            | N       | Only valid for assessments. Indicates whether user passed or failed the assessment				                   |
