# **Session Close**

Use this service to close an activate App session.

## **Endpoint**

### Production Enviroment
```
    POST    http://apialfarero.eliabc.com:80/v1.0/session/close
```

### Develpment Enviromment
```
    POST    http://159.203.93.24:8080/v1.0/session/close
```

## **Request Parameters**

### Headers Fields


| HEADER FIELD | VALUE | DESCRIPTION | RULE |
|---|---|---|:---:|
| Content-Type | `application/json; multipart/form-data;` | URL encoded form | *Required* |
| Authorization | `Basic c951985e404309115...` | A valid access token from the eliab API | *Required* |
| SessionID | `c951985e4043091155c660f11ac4c28d4...` | Active session ID | *Required* |
| OS | Device OS version from where the request is made | String | *Optional* |
| AppVersion | Version of the application installed on the device. The version must have the `Semantic Versioning 2.0.0` format. Values: `X.Y.Z`. Example: 1.0.0, 2.0.0, etc  | String | *Optional* |

### Raw Body Content
You must submit an empty `Request Content` object in JSON format.

## **Response Format**

On success, the HTTP status code in the response header is `200` OK and the response body contains an `Info` object in JSON format. On error, the header status code is an `error code` and the response body contains an `Info` object whit error information.

---

## **Request Content Object**

| KEY	 | VALUE | TYPE | RULES |
|-----|-------------|------|-------|
| requestContent | Required data for the service | Object | *Required* |

---

## **Info Object (full)**

| KEY	 | VALUE | TYPE | RULES |
|-----|-------------|------|-------|
| info | Default response content | Object | *Required* |
| info.type | Type of response. Values: `success`, `warning`, `error`, `info` | String | *Required* |
| info.title | Describe the message | String | *Required* |
| info.message | Descriptive information for the user | String | *Required* |
| info.sessionId | Return the session ID | String | *Required* |

---

## **Example**

### Request 

```json
curl --location --request POST '159.203.93.24:8080/v1.0/session/close' \
--header 'Content-Type: application/json; multipart/form-data;' \
--header 'Sessionid: c951985e4043091155c660f11ac4c28d4...' \
--header 'OS: Android' \
--header 'AppVersion: 1.0.10' \
--header 'Authorization: Basic c951985e404309...' \
--data-raw '{
    "requestContent": {
    }
}'

```

### Response

``` json
{
    "info": {
        "type": "success",
        "title": "Session closed!",
        "message": "The session has been closed successfully!",
        "sessionId": "c951985e4043091155c660f11a..."
    },
}
```

< [Home](../home.md)
