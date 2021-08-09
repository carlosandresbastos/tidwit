**CONTENT ITEMS**
=================

### contentitems.getUpdated

Gets a list of content items updated in a period of time. This is useful if you
are keeping a copy of the content item in your local database and want to keep
it up to date.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/contentitems.getUpdated  |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```json
https://<base-url>/api/v2.0/contentitems.getUpdated?beginDate=\<beginDate\>&endDate=\>endDate\>&offset=1&limit=10

```

**Arguments**

| **Field Name** | **Type**       | **Length** | **Comments**                       |
|----------------|----------------|------------|------------------------------------|
| **beginDate**  | datetimeoffset |            | e.g. 2019-02-18T00:00:00.000-05:00 |
| **endDate**    | datetimeoffset |            | e.g. 2019-02-19T00:00:00.000-05:00 |
| **offset**     | Integer        |            | Starting record                    |
| **limit**      | Integer        |            | Number of records to return        |

**Response**

```json
{
  "offset": 1,
  "limit": 2,
  "totalRecords": 2,
  "data": [
    {
      "id": "a35efd04-a3d2-40a3-add4-97545c301a99",
      "author": "Tony M",
      "contentSize": 0,
      "contentType": "None",
      "description": "This is a long description",
      "duration": 3600,
      "languageCode": "en",
      "lastUpdatedDate": "2019-02-18T11:00:36.5044599-05:00",
      "name": "API Test Item 2/18",
      "number": "",
      "publishedDate": "2019-02-18T11:21:28.13",
      "status": "Published",
      "thumbnail": {
        "type": "default",
        "url": "https://c3devstorage.file.core.windows.net/cachedev/content/images/thumbnail/e01661e7-443f-4932-9054-fe410afc576f?sv=2018-03-28&sr=f&si=c3636753111713397868&sig=rtikRLvsRHpRVwyS59yY59GgZhpdaLCPbnDkY3wz%2BU8%3D&tk=636860876688754326"
      }
    },
    {
      "id": "69729111-28f1-49a9-8fa7-79833dc41da6",
      "author": "Tony M",
      "contentSize": 0,
      "contentType": "Url",
      "description": "This is a long description",
      "duration": 3600,
      "externalContent": {
        "type": "WebSite",
        "url": "https://www.acme.com/training"
      },
      "languageCode": "en",
      "lastUpdatedDate": "2019-02-18T11:54:22.3162028-05:00",
      "name": "API Test Item 2/18 - 002",
      "number": "",
      "publishedDate": "2019-02-01",
      "status": "Published",
      "thumbnail": {
        "type": "default",
        "url": "https://c3devstorage.file.core.windows.net/cachedev/content/images/thumbnail/d3f62261-40cf-475f-848e-5bf5ebdd8e3b?sv=2018-03-28&sr=f&si=c3636753111713397868&sig=5wctJQq1VxzGe74YNCNchQkh5dmbnTnmK6ZVtj6dcVs%3D&tk=636860876689565519"
      }
    }
  ],
  "eTag": "F9034BAA9A37D4F2F715390130027501"
}

```

**Fields**

| **Field Name**       | **Type** | **Length** | **Req** | **Description**                                                           |
|----------------------|----------|------------|---------|---------------------------------------------------------------------------|
| id                   | guid     |            |         | Unique identifier of the content item                                     |
| name                 | string   | 256        | Y       | Name of the content item                                                  |
| description          | string   |            | N       | Detailed description of the content item                                  |
| author               | string   |            | N       |                                                                           |
| publishedDate        | Date     |            | Y       |                                                                           |
| expirationDate       | Date     |            | N       |                                                                           |
| duration             | int      |            | N       | Duration of content in seconds                                            |
| languageCode         | String   |            | Y       | ISO                                                                       |
| keywords             | string   |            | Y       |                                                                           |
| contentType          | Enum     |            |         | Type of content: Document, Image, Video, MOOC, …                          |
| number               | String   |            | 20      | Course \# or ID                                                           |
| version              | String   |            | 20      | Course version                                                            |
| status               | Enum     |            |         | One of: Published, Unpublished, Expired                                   |
| languageCode         | String   | 2          | Y       | ISO language code                                                         |
| externalContent.type | Enum     |            | N       | One of:                                                                   |
| externalContent.url  | string   |            | N       | URL to the external content                                               |
| allowAnonymousAccess | Bool     |            | Y       | Indicates whether authentication is requires to access the content        |
| showViews            | bool     |            | Y       | Indicates whether to display the number of views on the content item page |
