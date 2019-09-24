### Get Classroom Detail

Use this service to get the classroom detail.

#### Request

* URL: /v1.0/student/{student_id}/classroom/{classroom_id}
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
                "teachers": [
                    {
                    "id" : 1,
                    "name" : "Odalia",
                    "last_name" : "Ruiz"
                    }
                ],
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
}
```

[Return](#Classroom)


< Back to [Home](../home.md)
