# Students

The document content definition servicies from **Students** microservice

## Services

* [Registration](#Registration)  
* [First Login](#First-Login)  
* [Login](#Login)  

### Login

[Return](#Session)

### Registration

[Return](#Session)

### First Login

[Return](#Session)

### Set Student Icon Service

Use this service to set student icon.

#### Request

* URL: /v1.0/student/{student_id}/icon/{iconID}
* Method: POST
* Body:

``` json
{
    "requestContent": {

    }
}
```

#### Response

* HTTP Status: 200 (Ok)
* Body:

``` json
{
    "info": {
        "type": "success",
        "sessionId": "gTfI0uOuSZzl4d2nA4no5PIqrktzRgXu..."
    },
}
```

[Return](#HomeworkDetail)

### Send question

Use this service to send question to teacher.

#### Request

* URL: /v1.0/student/{student_id}/classroom/{classroom_id}/questions
* Method: POST
* Body:

``` json
{
    "requestContent": {
        "question": "Hola que hace?"
    }
}
```

#### Response

* HTTP Status: 200 (Ok)
* Body:

``` json
{
    "info": {
        "type": "success",
        "sessionId": "gTfI0uOuSZzl4d2nA4no5PIqrktzRgXu..."
    },
}
```

[Return](#HomeworkDetail)



< Back to [Home](../home.md)