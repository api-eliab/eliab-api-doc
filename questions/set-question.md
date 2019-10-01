# **Set Question To Owner**

Use this service to set question to a teacher course.

## **Endpoint** 

    GET: /v1.0/teachers/{teacher_id}

## **Request Parameters**

### Path Parameters

| Path Parameter | Description | Type | Rules |
|-----|-------------|------|-------|
| teacher_id | Teacher id | Int64 | (Required) |

### Header Fields

| Header Field | Description | Value | Rules |
|-----|-------------|------|-------|
| Autorization | An autorization Basic | base64 | (Required) |
| SessionID | Session id obtained at login | string | (Required) |
| Content-Type | The content type of the request body | application/json | (Required) |

### Request Body ###

``` json
{
    "requestContent": {
        "question": {
            "title": "Mi titulo",
            "resource": "Tarea preparatoria",
            "message": "Mi mensaje",
            "type": "task"
        }
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| requestContent | Request data | Object | (Required) |
| requestContent.question | Question info | Object | (Required) |
| requestContent.question.title | Description question | String | (Required) |
| requestContent.question.resource | Resource on which the question is being asked, for example: "First preparatory task". They can be the title of the task or course. | String | (Required) |
| requestContent.question.messaje | Question | String | (Required) |
| requestContent.question.type | Type of question | String | (Required) |

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
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| info | Info section is described at requests structure in  [home](../home.md#Response-Structure) page  | Object | (Required) |


< Back to [Classroom](./classroom.md)
