**CONTENT ITEMS**
=================

### contentitems.update

Updates an existing new content items

**Facts**

| **URL**                    |   https://[base-url]/api/v2.0/contentitems.update |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
    "id": "b674afc5-aefa-43d2-a255-4d993f65b9fd",
    "name": "myProduct Training Video",
    "author": "John Doe",
    "description": "A more detailed description about this video",
    "publishedDate": "2018-12-02",
    "expirationDate": "2019-09-22",
    "duration": 3600,
    "languageCode": "en",
    "number": "1234J",
    "version": "2019-Q1",
    "keywords": "myProduct ACME training",
    "externalContent": {
        "type": "YouTube",
        "url": "https://youtube.com?v=1223f12"
    },
    "options": {
        "allowAnonymousAccess": false,
        "showViews": true,
    }
}
```

**Response**

```json
{
    "id": "b674afc5-aefa-43d2-a255-4d993f65b9fd",
    "name": "myProduct Training Video",
    "author": "John Doe",
    "description": "A more detailed description about this video",
    "publishedDate": "2018-12-02",
    "expirationDate": "2019-09-22",
    "duration": 3600,
    "languageCode": "en",
    "number": "1234J",
    "version": "2019-Q1",
    "keywords": "myProduct ACME training",
    "externalContent": {
        "type": "YouTube",
        "url": "https://youtube.com?v=1223f12"
    },
    "options": {
        "allowAnonymousAccess": false,
        "showViews": true,
    }
}

```

**Fields**

| **Field Name**       | **Type** | **Length** | **Req** | **Description**                                                               |
|----------------------|----------|------------|---------|-------------------------------------------------------------------------------|
| id                   | guid     |            |         | Unique identifier of the content item                                         |
| name                 | string   | 256        | Y       | Name of the content item                                                      |
| description          | string   |            | N       | Detailed description of the content item                                      |
| author               | String   |            | N       |                                                                               |
| publishedDate        | Date     |            | Y       |                                                                               |
| expirationDate       | Date     |            | N       |                                                                               |
| duration             | int      |            | N       | Duration of content in seconds                                                |
| number               | String   | 20         | N       | Course \# or ID                                                               |
| version              | String   | 20         | N       | Course version                                                                |
| languageCode         | String   |            | Y       | ISO                                                                           |
| keywords             | string   |            | Y       |                                                                               |
| languageCode         | String   | 2          | Y       | ISO language code                                                             |
| externalContent.type | Enum     |            | N       | One of: YouTube, MicrosoftVirtualAcademy, Channel9, MP4, HandsOnLabs, WebSite |
| externalContent.url  | string   |            | N       | URL to the external content                                                   |
| allowAnonymousAccess | Bool     |            | Y       | Indicates whether authentication is requires to access the content            |
| showViews            | bool     |            | Y       | Indicates whether to display the number of views on the content item page     |

