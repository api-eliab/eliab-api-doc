# Homework

The document content definition servicies from **Homework** microservice

## Services

* [Get Homework List](#HomeworkList)  

### Get Homework List

Use this service to get the homework assignments for student.

#### Request

* URL: /v1.0/students/{student_id}/homework
* Method: GET

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
        "homeworks": [{
                "id": 1821,
                "points": 5,
                "title": "Cuerpo Humano",
                "short_description": "La tarea consta de realizar una maqueta del cuerpo humano.",
                "long_description" : "Deben utilizar duroport para la base, la maqueta como tal tiene que ser de plastilina.",
                "classroom_id": 3,
                "delivery_date": "12 de Abril",
                "delivery_hour": "11:00 AM"
            },
            {
                "id": 1822,
                "points": 10,
                "title": "Ecuaciones",
                "short_description": "Realizar las primeras 5 ecuaciones del libro...",
                "long_description" : "Deben utilizar duroport para la base, la maqueta como tal tiene que ser de plastilina.",
                "classroom_id": 4,
                "delivery_date": "12 de Abril",
                "delivery_hour": "09:00 AM"
            }
        ]
    }
}
```

[Return](#HomeworkList)

* [Get Homework Detail ](#HomeworkDetail)  

### Get Homework Detail

Use this service to get the homework detail.

#### Request

* URL: /v1.0/students/{student_id}/{homework_id}/homework/detail
* Method: GET

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
        "homework": {
                "id": 1821,
                "points": 5,
                "title": "Cuerpo Humano",
                "short_description": "La tarea consta de realizar una maqueta del cuerpo humano.",
                "classroom_id": 3,
                "classroom_name" : "Ciencias Naturales",
                "teachers_id" : "1",
                "teachers_name" : "Odalia Ruiz",
                "delivery_date": "12 de Abril",
                "delivery_hour": "11:00 AM"
            }
    }
}
```

[Return](#HomeworkDetail)


< Back to [Home](../home.md)
