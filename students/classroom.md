# Classroom

The document content definition servicies from **Classroom** microservice

## Services

* [Get Classroom list](#ClassroomList)  

### Get Classroom List

Use this service to get the classroom assignments for student.

#### Request

* URL: /v1.0/students/{student_id}/classroom
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
        "classrooms": [{
                "id": 1,
                "name": "Ciencias Naturales"
            },
            {
                "id": 2,
                "name": "Matemáticas"
            }
        ]
    }
}
```

[Return](#ClassroomList)

* [Get Classroom Detail ](#ClassroomDetail)  

### Get Classroom Detail

Use this service to get the classroom detail.

#### Request

* URL: /v1.0/students/{student_id}/{classroom_id}/classroom/detail
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
        "classroom": {
                "name": "Matematicas",
                "teacher": {
                    "id" : 1,
                    "name" : "Odalia",
                    "last_name" : "Ruiz"
                },
                "grade": "Tercero Primaria",
                "course_dist":[{  
                    "perfect" : true,
                    "name" : "Primer Bimestre",
                    "id" : 4,
                    "current_points" : 10,
                    "tasks" : [{
                        "id" : 1,
                        "name" : "Tarea 1",
                        "points" : "5/5 pts",
                        "type" : 1
                       },
                        {
                        "id" : 2,
                        "name" : "Tarea 2",
                        "points" : "5/5 pts",
                        "type" : 1
                        },...
                    ],
            }]
        
    }
}
```

[Return](#ClassroomDetail)


< Back to [Home](../home.md)
