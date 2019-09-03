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

< Back to [Home](../home.md)