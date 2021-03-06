**CONTENT ITEMS**
=================

### contentitems.get

Gets an existing content item.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/contentitems.get |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```json
https://<base-url>/api/contentitems.get?id=b674afc5-aefa-43d2-a255-4d993f65b9fd
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
    "keywords": "myProduct ACME training",
    "contentType": "Video",
    "number": "AC5560J",
    "version": "2019-Q1",
    "status": "Published",
    "externalContent": {
        "type": "WebSite",
        "url": "https://acme.com/myproduct/training"
    },
    "thumbnail": {
        "type": "default",
        "url": "https://c3devstorage.file.core.windows.net/cachedev/content/images/thumbnail/d0994cc0-8a90-4e84-8255-da314d86c51c?sv=2018-03-28&sr=f&si=c3636753111713397868&sig=n4m044HRyUqUYKz3BYvcn1Piq6xLuulf5xcvxI6zZxs%3D&tk=636860780739679405",
    },
    "options": {
        "allowAnonymousAccess": false,
        "showViews": true,
    },
    "lastUpdatedDate": "2019-02-12T18:25:30.8602458-05:00",
    "link": "https://pub.ontidwitdev.com/content-items/blockchain-document",
}

```

**Fields**

| **Field Name**       | **Type**       | **Length** | **Req** | **Description**                                                           |
|----------------------|----------------|------------|---------|---------------------------------------------------------------------------|
| id                   | guid           |            |         | Unique identifier of the content item                                     |
| name                 | string         | 256        | Y       | Name of the content item                                                  |
| description          | string         |            | N       | Detailed description of the content item                                  |
| author               | String         | 256        | Y       |                                                                           |
| publishedDate        | Date           |            | Y       |                                                                           |
| expirationDate       | Date           |            | N       |                                                                           |
| duration             | int            |            | N       | Duration of content in seconds                                            |
| languageCode         | String         |            | Y       | ISO                                                                       |
| keywords             | string         |            | Y       |                                                                           |
| contentType          | Enum           |            |         | Type of content: Document, Image, Video, MOOC, …                          |
| number               | String         | 20         | N       | Course \# or ID                                                           |
| version              | String         | 20         | N       | Course version                                                            |
| Status               | Enum           |            |         | One of: Published, Unpublished, Expired                                   |
| languageCode         | String         | 2          | Y       | ISO language code                                                         |
| externalContent.type | Enum           |            | N       | One of:                                                                   |
| externalContent.url  | string         |            | N       | URL to the external content                                               |
| allowAnonymousAccess | Bool           |            | Y       | Indicates whether authentication is requires to access the content        |
| showViews            | bool           |            | Y       | Indicates whether to display the number of views on the content item page |
| lastUpdateDate       | datetimeoffset |            |         | Last time the content item was updated                                    |
| link                 | String         |            |         | Link to the content item on the TidWiT platform                           |
