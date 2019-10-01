# **Get Responses To Messages**

Use this service to get message to teacher course.

## **Endpoint** 

    GET: /v1.0/messages

## **Request Parameters**

### Header Fields

| Header Field | Description | Value | Rules |
|-----|-------------|------|-------|
| Autorization | An autorization Basic | base64 | (Required) |
| SessionID | Session id obtained at login | string | (Required) |
| Content-Type | The content type of the request body | application/json | (Required) |


## **Response Format**

On success, the response body contains the succes response object in JSON format and the HTTP status code in the response header is 200 (OK) or 201 (Created). 

On error, the header status code is an error code and the response body contains an error object.

## **Response Object**

    HTTP Status: 200 (Ok)

``` json
{
    "info": {
        "type": "success",
        "sessionId": "gTfI0uOuSZzl4d2nA4no5PIqrktzRgXu..."
    },
    "responseContent": {
        "messajes": [
            {
                "title": "Mi titulo",
                "resource": "Tarea preparatoria",
                "message": "Mi mensaje",
                "type": "task",
                "createdAt": "2019-09-27T10:01:19Z",
                "response": "Esta es la respuesta",
                "state": 1,
                "updatedAt": "2019-09-27T10:01:19Z",
            },
           {
                "title": "Mi titulo",
                "resource": "Tarea preparatoria",
                "message": "Mi mensaje",
                "type": "task",
                "createdAt": "2019-09-27T10:01:19Z",
                "response": "",
                "state": 0,
                "updatedAt": "",
            },
        ],
        "limit": 100,
        "next": "/v1.0/messages?offset=100&limit=100",
        "offset": 0,
        "previous": null,
        "total": 105
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| info | Info section is described at requests structure in  [home](../home.md#Response-Structure) page  | Object | (Required) |
| responseContent | Response data | Object | (Required) |
| responseContent.messages[] | messages  | Array(Object) | (Required) |
| responseContent.messages[].title | message info | String | (Required) |
| responseContent.messages[].resourse | Description message | String | (Required) |
| responseContent.messages[].message | message | String | (Required) |
| responseContent.messages[].type | Type of message | String | (Required) |
| responseContent.messages[].createdAt | Date ISO 8601. Layout:   `2019-09-27T10:01:19Z` | Date | (Required) |
| responseContent.messages[].response | Response of message | String | (Required) |
| responseContent.messages[].state | State of message | Int | (Required) |
| responseContent.messages[].updatedAt | Date ISO 8601. Layout:   `2019-09-27T10:01:19Z` | Date | (Required) |
| responseContent.limit | The maximum number of items in the response (as set in the query or by default). | Int | (Required) |
| responseContent.next | URL to the next page of items. ( null if none) | String | (Required) |
| responseContent.offset | The offset of the items returned (as set in the query or by default). | Int | (Required) |
| responseContent.previous | URL to the previous page of items. ( null if none) | String | (Required) |
| responseContent.total | The total number of items available to return. | Int | (Required) |


< Back to [Classroom](./classroom.md)
