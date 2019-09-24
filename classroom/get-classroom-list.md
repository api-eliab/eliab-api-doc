# **Get Classroom List**

Use this service to get the classroom assignments for student.

## **Endpoint** 

    GET: /v1.0/student/{student_id}/classrooms

## **Request Parameters**

### Path Parameters

| Path Parameter | Description | Type | Rules |
|-----|-------------|------|-------|
| student_id | Student id | Int64 | (Required) |

### Header Fields

| Header Field | Description | Value | Rules |
|-----|-------------|------|-------|
| Autorization | An autorization Basic | base64 | (Required) |
| SessionID | Session id obtained at login | string | (Required) |
| Content-Type | The content type of the request body | application/json | (Required) |


## **Response Format**

On success, the response body contains the classroom for student object in JSON format and the HTTP status code in the response header is 200 (OK) or 201 (Created). 

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
        "classrooms": [{
                "id": 1,
                "name": "Ciencias Naturales",
                "icon": 5
            },
            {
                "id": 2,
                "name": "Matemáticas",
                "icon": 3
            }
        ]
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| info | Info section is described at requests structure in  [home](../home.md#Response-Structure) page  | Object | (Required) |
| responseContent | Response data | Object | (Required) |
| responseContent.classrooms[] | Classrooms  | Array(Object) | (Required) |
| responseContent.classrooms[].id | Classroom id | Int64 | (Required) |
| responseContent.classrooms[].name | Classroom name | String | (Required) |
| responseContent.classrooms[].icon | Classroom icon | Int64 | (Required) |

< Back to [Classroom](./classroom.md)
