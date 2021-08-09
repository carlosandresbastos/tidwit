**LIBRARIES**
=============

### libraries.uploadThumbnail

Uploads a thumbnail image for existing library

**Facts**

| **URL**                    |     https://[instance-root-url]/api/v2.0/contentitems.uploadThumbnail  |
|----------------------------|---------------------|
| **HTTP method**            | POST                |
| **Accepted content types** | multipart/form-data |

**Request**

```json
POST /libraries.uploadThumbnail?id=b674afc5-aefa-43d2-a255-4d993f65b9fd HTTP/1.1
Host: acme.ontidwit.com
Content-Type: multipart/form-data;boundary="boundary"

--boundary
Content-Disposition: form-data; name="image.jpp"

<binary data>


```

**Response**

```text
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |         | Unique identifier of the content item |
