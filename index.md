**TIDWIT PLATFORM WEB API**
=================

### Introduction

The TidWiT Platform Web API is a REST API that allows access to the TidWiT application functionality. The API uses standard HTTP GET and POST requests that return JSON responses.


### Basics

The Web API is a collection of HTTP methods all in the form:
https://<instance-root-url>/api/object.method 
Use HTTPS and SSL when calling all methods.
Pass arguments as:

* GET query string parameters
* POST parameters presented as application/x-www-form-urlencoded or a mix of both GET and POST parameters
* Some write methods allow arguments application/json attributes.
* File upload method expect multipart/form-data 

### POST bodies

***JSON-encoded bodies***

For methods that require data POST bodies, you should send your HTTP POST data as Content-type: application/json.
There are some ground rules:
* You must explicitly set the Content-type HTTP header to application/json. We won't interpret your POST body as such without it.
* You must transmit your token as a bearer token in the Authorization HTTP header.
* You cannot send your token as part of the query string or as an attribute in your posted JSON.
* Providing an explicitly null value for an attribute will result in whichever default behavior is assigned to it.

For example, to create a new menu heading with a JSON POST body:
 
```text
POST /api/menuHeadings.create
Content-type: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1laWQiOiJh
{"name":"my-heading"}
```


### TOKENS
You'll need to register your app before getting started. A registered app is assigned a unique Client ID and Client Secret which will be used in the OAuth flow. The Client Secret should not be shared.

To consume the Web API, a token needs to be obtained from the identity provider.  

**Generating Access Token Using the Client Credentials Grant Type**

This flow is primarily used for machine to machine authentication. The client application uses the Client ID and Client Secret to generate an access token. The scope of the access token will be limited to resources that the owner of the API Client ID and Secret has access to. Client ID and Secret can be generated in the Developer section in your TidWiT instance administration interface.

**Endpoint URL**

```text
POST https://<sso-base-url>/oauth/token
```

**Parameters**

Parameters should be passed in the request body using a Content Type: application/x-www-form-urlencoded.

|**Field Name**|**Type**|**Length**|**Comments**|
|-------|----|------|-----|
|grant_type|String||Should be “client_credentials” |
|client_id|String|256|API Client ID|
|client_secret|String|256|API Client Secret|

**Response**

The response will have the following format:
```json
{
    "status": {
    "timestamp": "2018-01-23T14:34:10.6562279Z",
    "code": 200
    },
    "response": { 
        "token_type": "Bearer", 
        "access_token": "eyJhbGciOi-JIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1laWQiOiJhpYXQiOjE1NDgzNTM1OTJ9.HXWvmYOS0W5i5LEkIm8Is",
        "expires_in": 3600
    }
}
```


**Using Tokens in API calls**

Once the token type and access token are received, API calls can be made using the Authorization HTTP header:
Authorization: <token_type> <access_token>

As an example, for the response returned above, the HTTP header would be:

```text
Authorization: Bearer eyJhbGciOi-JIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1laWQiOiJhpYXQiOjE1NDgzNTM1OTJ9.HXWvmYOS0W5i5LEkIm8Is
```


### Endpoints

[Menu Headings](menuHeadings/index.md)