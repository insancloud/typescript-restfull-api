# User API Spec

## Register User

Endpoint : POST /api/users
Request Body : 

```json
{
    "username" : "insan",
    "pasword" : "secret",
    "name" : "insan ibrahim"
}

```
Response Body (Success) : 

```json
{
    "data": {
        "username" : "insan",
        "name" : "insan ibrahim"
    }
}
```

Response Body (Failed) : 

```json
{
    "errors" : "username must not Blank, ...."
}

```

## Login User

Endpoint : POST /api/users/current

Request Header : 
- X-API-TOKEN : token

Response Body (Success) : 

```json
{
    "data": {
        "username" : "insan",
        "name" : "insan ibrahim",
        "token" : "uuid"
    }
}
```

Response Body (Failed) : 

```json
{
    "errors" : "Unauthorized"
}

```

## Get User

Endpoint : GET /api/users
Request Body : 

```json
{
    "username" : "insan",
    "pasword" : "secret",
    "name" : "insan ibrahim"
}

```
Response Body (Success) : 

```json
{
    "data": {
        "username" : "insan",
        "name" : "insan ibrahim"
    }
}
```

Response Body (Failed) : 

```json
{
    "errors" : "username must not Blank, ...."
}

```

## Update User

Endpoint : PATCH /api/users/current

Request Header : 
- X-API-TOKEN : token

Request Body : 

```json
{
    "pasword" : "secret",
    "name" : "insan ibrahim"
}

```
Response Body (Success) : 

```json
{
    "data": {
        "username" : "insan", // tidak wajib
        "name" : "insan ibrahim" // tidak wajib
    }
}
```

Response Body (Failed) : 

```json
{
    "errors" : "Unauthorized"
}

```

## Logout User

Endpoint : DELETE /api/users/current

Request Header : 
-X-API-TOKEN : token

Response Body (Success) : 

```json
{
    "data": "OK"
}
```

Response Body (Failed) : 

```json
{
    "errors" : "Unauthorized"
}

```