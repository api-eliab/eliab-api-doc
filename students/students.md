# Students

The document content definition servicies from **Students** microservice

## Services

* [Set Student Icon Service](#Set-Student-Icon-Service)  

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

[Return](#Services)

### Send question

Use this service to send question to teacher.

#### Request

* URL: /v1.0/responsibles/{responsible_id}/questions
* Method: POST
* Body:

``` json
{
    "requestContent": {
        "teacher_id": 100,
        "question": "Hola que hace seño?"
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

[Return](#Services)

< Back to [Home](../home.md)