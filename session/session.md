# Session

The document content definition servicies from **Session** microservice

## Services

* [Login](#Login)  
* [Registration](#Registration)  
* [First Login](#First-Login)  

### Login

Use this service to create a session for App movile.

#### Request

* URL: /v1.0/session
* Method: POST
* Body:

``` json
{
    "requestContent": {
        "credentials": {
            "user": "firulais@colegios.edu",
            "password": "MyPassword"
        }
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| requestContent | Request data | Object | (Required) |
| requestContent.credentials | Content user credential info | Object | (Required) |
| requestContent.credentials.user | User email | String | (Required) |
| requestContent.credentials.password | User password | String | (Required) |

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
        "user": {
            "id": 1821,
            "firstName": "Firulais",
            "lastName": "Canelo",
            "email": "firulais@colegios.edu",
            "phone": "12345678",
            "address": "12av. 19-33, Zona 12",
            "sons": [
                {
                    "id": 1892,
                    "firstName": "Manchas",
                    "lastName": "Canelo",
                    "avatar": 3
                },
                {
                    "id": 1893,
                    "firstName": "Perla",
                    "lastName": "Canelo",
                    "avatar": 4
                },
                ...
            ]
        }
    }
}
```

| Key | Description | Type | Rules |
|-----|-------------|------|-------|
| info | [Structure defined in Home Page](../home.md) | Object | (Required) |
| responseContent | Response data | Object | (Required) |
| responseContent.user | Created user data | Object | (Required) |
| responseContent.user.id | User unique identifier | Int64 | (Required) |
| responseContent.user.firstName | User first name| String | (Required) |
| responseContent.user.lastName | User last name | String | (Required) |
| responseContent.user.email | User email | String | (Required) |
| responseContent.user.address | User home addres | String | (Required) |
| responseContent.user.sons[] | Sons list | Array(Object) | (Required) |
| responseContent.user.sons[].id | User first name | Int64 | (Required) |
| responseContent.user.sons[].firstName | User first name | String | (Required) |
| responseContent.user.sons[].lastName | User last name | String | (Required) |
| responseContent.user.sons[].avatar | User avatar id | Int | (Required) |

[Return](#Session)

### Registration

[Return](#Session)

### First Login

[Return](#Session)

< Back to [Home](../home.md)