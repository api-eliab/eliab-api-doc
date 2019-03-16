# Colegios - API 1.0.0

## Overview

The following is the web services definition for **Colegios - API 1.0.0**, for front-end.

* [Authentication](#Authentication)  
* [Services](#Services)  
* [Request Structure](#Request-Structure)  
* [Response Structure](#Response-Structure)  
* [Default Headers on Requests](#Default-Headers-on-Requests)  
* [Error Codes](#Error-Codes)  
* [Microservices](#Microservices)  

### Authentication

These services require [Basic HTTP Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication). The credentials are the following:

* User: colegios
* Password: C013g10s@

[Return](#Overview)

### Services

The services were programmed with [REST-JSON](http://jsonapi.org/).

[Return](#Overview)

### Request Structure

You must send the required data on PUT, POST, PATCH, DELETE requests to API using the next body structure:

``` json
{
    "requestContent": {
        ...
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| requestContent | Required data for the service | Object | (Required) |

For GET requests the parameters must be send as **Query Parameters**, followed by the sign **"?"** and separated by the **"&"** sign.

You must also send the default headers explained in the following section.

[Return](#Overview)

### Default Headers on Requests

The API needs some data for taking some decisions about the responses and internal processes. The API requires the data through the request headers, the required headers are:

| Key | Description | Rules |
|-----|-------------|-------|
| Authorization | Used to send the Basic Auth hash for authenticate device on API | (Required) (Format: Basic {{Hash}}) |
| Content-Type | Used to send the request and response body type. The header value must be "application/json" | (Required) |
| Guest | Used to send the user email, for both mobile and web app, When the user logs in the app must send the user email in the Guest header | (Optional) |
| OS | Used to send the user host OS, The parameter must be **web** for all request on web app. For mobile app the parameter must be **android** or **ios**, it depends of the user mobile OS | (Required)  |
| OSVersion | Used to send the user host OS version | (Required) (Format: Semantic Versioning 1.1.1) |
| DeviceUUID | Used to send the user device UUID (Universally unique identifier) | (Required) |
| AppVersion | Used to send the user app versión, for web app must be the internal version number (git tag) | (Required) (Format: Semantic Versioning 1.1.1) |
| Timezone | Used to send the user timezone | (Optional) |
| SessionID | Used to send the user session, created on login or registration. Send this value only when the user already has an open session | (Optional) |

[Return](#Overview)

### Response Structure

The API responses use the next structure:

``` json
{
    "info": {
        "type": "...",
        "messageTitle": "...",
        "message": "...",
        "sessionID": "...",
        "action": "..."
    },
    "responseContent": {
        ...
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| info | Contains messages for users | Object | (Required) |
| info.type | Message type. Possible values are:  | String | (Required) |
||**success** (notifies a successfully completed process), ||
||**info** (additional information for users), ||
||**warning** (notifies warning or danger for user), ||
||**error** (notifies an error in process) ||
| info.messageTitle | Message title | String | (Optional) |
| info.message | Message description | String | (Optional) |
| info.sessionID | Open user session. Only if user already open a session | String | (Optional) |
| info.action | Indicates that the app must do an action based on the response message, the value is a unique key used only for certain app flows | String | (Optional) |
| responseContent | Required data for user, based the on request | Object | (Optional) |

The messages on the info section, may come on any of the services responses, by example, the API can respond with the required data and a warning message, in that moment the app must show the message to the user. That means that the app (iOS, Android, web) must be prepared to show messages at any time that the API responds with one in the info section.

[Return](#Overview)

### Error Codes

The services use [HTTP Status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) to notify errors. The apps must use the **info section** of the services responses, to show error messages (message type "error"), using the **"message_title", "message"** keys data.

The HTTP Status codes use for this services are:

* 400 Bad Request
* 401 Unauthorized: This code means that user has no longer access to session required services, in case of a session expired or is invalid, the services will return this error code and the app must delete the local session and send the user to the login section. If user try to open a session (login) but the credentials are invalid the services will return this error code.
* 403 Forbidden
* 404 Not Found
* 500 Internal Server Error

[Return](#Overview)

## Microservices

* [Session](./session/session.md)  
* [Students](./students/students.md)

[Return](#Overview)