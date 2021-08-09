**LEARNING CAMPAIGNS**
====================== 

### learningCampaigns.getLearningPaths

Returns a list of learning paths in an existing learning campaign.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/learningCampaigns.getLearningPaths |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**


```text
https://<base-url>/api/v2.0/learningCampaigns.getLearningPaths?id=c91a1717-f20e-432d-b2bc-68b2c290d8f8
```


**Arguments**

| **Field Name** | **Type** | **Length** | **Comments**                              |
|----------------|----------|------------|-------------------------------------------|
| **id**         | string   |            | Unique identifier of the learning campaign|


**Response**

[ 
  { 
    "id": "e89da79e-4df7-454b-a617-d5bd7ca8adae", 
    "name": "Testing", 
    "description": "Testing Learning Path" 
    "thumbnail": {
        "type": "default",
        "url": "https://c3devstorage.file.core.windows.net/cachedev/content/images/thumbnail/d0994cc0-8a90-4e84-8255-da314d86c51c?sv=2018-03-28&sr=f&si=c3636753111713397868&sig=n4m044HRyUqUYKz3BYvcn1Piq6xLuulf5xcvxI6zZxs%3D&tk=636860780739679405",
    },
  },
 { 
   "id": "fbf04fcd-7f1c-4c3a-bd23-2f34a5db2cb5", 
   "name": "Training Courses", 
   "description": "More details about course" 
    "thumbnail": {
        "type": "default",
        "url": "https://c3devstorage.file.core.windows.net/cachedev/content/images/thumbnail/d0994cc0-8a90-4e84-8255-da314d86c51c?sv=2018-03-28&sr=f&si=c3636753111713397868&sig=n4m044HRyUqUYKz3BYvcn1Piq6xLuulf5xcvxI6zZxs%3D&tk=636860780739679405",
    },
  }
]

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                             |
|----------------|----------|------------|---------|---------------------------------------------|
| id             | guid     |            | Y       | Unique identifier of the learning path      |
| name           | string   | 256        | Y       | Name of the learning path                   |
| description    | string   |            | N       | Detailed description of the learning path   |
| thumbnail.type | string   |            | N       | Type of the Thumbnail                       |
| thumbnail.url  | string   |            | N       | Thumbnail url                               |