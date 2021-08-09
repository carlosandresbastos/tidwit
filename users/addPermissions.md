**USERS**
=================

### users.addPermissions

Assigns Permissions of existing users.

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/users.addPermissions |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | application/json |

**Request**

```json
{
  "userID": "4f8813cc-ac22-4aa1-bf23-bd15655948c1",
  "permissions": [
    "Administrator",
    "CommerceManagement",
    "ContentManagement",
    "Developer",
    "LearningManagement",
    "OutboundSyndication",
    "PartnerManagement",
    "Reports",
    "SiteManagement",
    "Support",
    "UserManagement"
  ]
}
```

**Response**

```text
HTTP 200 OK 
```

**Fields**

| **Field Name** | **Type** |  **Description**                      |
|----------------|----------|---------------------------------------|                   
|userID          |guid      |Unique identifier of the user          |
|permissions     |Array[string] |List of permissions                |