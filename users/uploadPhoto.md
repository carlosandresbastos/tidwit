**USERS**
=================

### users.uploadPhoto

Uploads a Photo for an existing users.

**Facts**

| **URL**                    | https://[base-url]/api/v2.0/users.uploadPhoto |
|----------------------------|------------------|
| **HTTP method**            | POST             |
| **Accepted content types** | Multipart/form-data |

**Request**

```text
POST /users.uploadPhoto?id=b674afc5-aefa-43d2-a255-4d993f65b9fd HTTP/1.1
Host: acme.ontidwit.com
Content-Type: multipart/form-data;boundary="boundary"

--boundary
Content-Disposition: form-data; name="image.jpg"

<binary data>

**Arguments**

| **Field Name** | **Type** |**Comments**     |
|----------------|----------|---------------- |
|id              |Guid      | Unique identifier of the user|

**Response**

```text
HTTP 200 OK
```