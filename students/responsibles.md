# Responsibles

The document content definition servicies from **Responsibles** microservice

## Services

* [Send Question](#Send-Question)  
* [Get Responses](#Get-Responses)  

### Send Question

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

### Get Responses

Use this service to get responses of the questions.

#### Request

* URL: /v1.0/responsibles/{responsible_id}/questions
* Method: GET
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
    "responseContent": {
        "questions": [{
                "id": 1821,
                "question": "Hola, quisiera saber...?",
                "asked_at": "12 de Abril",
                "answer": "El objetivo de la tarea es...",
                "answer_at" : "13 de Abril",
                "teacher_id": 3,
                "teacher": "Julia Roberts",
                "state": 1,
            },
            {
                "id": 1820,
                "question": "Hola, quisiera saber...?",
                "asked_at": "11 de Abril",
                "answer": "",
                "answer_at" : "",
                "teacher_id": ,
                "teacher": "",
                "state": 0
            },
            ...
        ]
    }
}
```

[Return](#Services)

< Back to [Home](../home.md)