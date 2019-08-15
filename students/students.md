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

### Set Student Icon

Use this service to set student icon.

#### Request

* URL: /v1.0/student/{student_id}/icon/{iconID}
* Method: POST

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