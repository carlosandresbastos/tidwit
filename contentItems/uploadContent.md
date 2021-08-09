**CONTENT ITEMS**
=================

### contentitems.uploadContent

Uploads a thumbnail image for existing content item

**Facts**

| **URL**                    | https://[instance-root-url]/api/v2.0/contentitems.uploadContent |
|----------------------------|---------------------|
| **HTTP method**            | POST                |
| **Accepted content types** | Multipart/form-data |

**Request**

```text
POST /contentitems.uploadContent?id=b674afc5-aefa-43d2-a255-4d993f65b9fd HTTP/1.1
Host: acme.ontidwit.com
Content-Type: multipart/form-data;boundary="boundary"

--boundary
Content-Disposition: form-data; name="video.mp4"

<binary data>
```

**Response**

```json
HTTP 200 OK
```

**Fields**

| **Field Name** | **Type** | **Length** | **Req** | **Description**                       |
|----------------|----------|------------|---------|---------------------------------------|
| id             | guid     |            |         | Unique identifier of the content item |
