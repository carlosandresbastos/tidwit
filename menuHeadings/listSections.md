**MENU HEADINGS**
=================

### menuHeadings.listSections

Gets the sections under a menu heading

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/menuHeadings.listSections  |
|----------------------------|------------------|
| **HTTP method**            | GET              |
| **Accepted content types** | application/json |

**Request**

```json
https://<base-url>/api/menuHeadings.listSections?id=ebc11c6c-9695-49a0-a5e6-c0098af82957
```

**Response**

```json
[
  {
    "id": "1b562b42-d56b-4634-8101-4fe2fc6c7648",
    "name": "AZURE TRAINING"
  },
  {
    "id": "5ff689c8-ad0b-40c5-9280-4e486279325e",
    "name": "DYNAMICS TRAINING"
  },
  {
    "id": "6e002b21-561d-414e-9a0e-0bf037ef8930",
    "name": "EMS TRAINING"
  },
  {
    "id": "0fc92072-86bf-4f62-a8b3-36bd267d6030",
    "name": "OFFICE 365 TRAINING"
  }
]

```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                  |
|----------------|----------|------------|---------|----------------------------------|
| id             | guid     |            |         | Unique identifier of the section |
| name           | string   | 256        | Y       | Name of the section              |
