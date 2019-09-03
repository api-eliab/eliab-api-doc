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

< Back to [Home](../home.md)