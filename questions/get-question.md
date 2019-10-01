# **Get Responses**

Use this service to get question to teacher course.

## **Endpoint** 

    GET: /v1.0/questions

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
        "questions": [
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
        ]
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| info | Info section is described at requests structure in  [home](../home.md#Response-Structure) page  | Object | (Required) |
| responseContent | Response data | Object | (Required) |
| responseContent.questions[] | Questions  | Array(Object) | (Required) |
| responseContent.questions[].title | Question info | String | (Required) |
| responseContent.questions[].resourse | Description question | String | (Required) |
| responseContent.questions[].message | Question | String | (Required) |
| responseContent.questions[].type | Type of question | String | (Required) |
| responseContent.questions[].createdAt | Date ISO 8601. Layout:   `2019-09-27T10:01:19Z` | Date | (Required) |
| responseContent.questions[].response | Response of question | String | (Required) |
| responseContent.questions[].state | State of question | Int | (Required) |
| responseContent.questions[].updatedAt | Date ISO 8601. Layout:   `2019-09-27T10:01:19Z` | Date | (Required) |

< Back to [Classroom](./classroom.md)
