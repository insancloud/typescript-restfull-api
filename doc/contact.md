# Contact API Spec

## Create Contact

Endpoint : POST /api/contacts

Request Header : 
- X-API-TOKEN : token

Request Body : 

```json
{
    "first_name" : "insan",
    "last_name" : "ibrahim",
    "email" : "insan5272@gmail.com",
    "phone" : "08212121212"
}
```

Response Body (Success) : 

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "insan",
        "last_name" : "ibrahim",
        "email" : "insan5272@gmail.com",
        "phone" : "12121212"

    }
}
```

Response Body (Failed) : 

```json
    "errors" : "Firs Name must not Blank!"
```

## Get Contact

Endpoint : GET /api/contacts:id

Request Header : 
- X-API-TOKEN : token


Response Body (Success) : 

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "insan",
        "last_name" : "ibrahim",
        "email" : "insan5272@gmail.com",
        "phone" : "12121212"

    }
}
```

Response Body (Failed) : 

```json
    "errors" : "Contact Not Found"
```


## Update Contact

Endpoint : POST /api/contacts

Request Header : 
- X-API-TOKEN : token

Request Body : 

```json
{
    "first_name" : "insan",
    "last_name" : "ibrahim",
    "email" : "insan5272@gmail.com",
    "phone" : "08212121212"
}
```

Response Body (Success) : 

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "insan",
        "last_name" : "ibrahim",
        "email" : "insan5272@gmail.com",
        "phone" : "12121212"

    }
}
```

Response Body (Failed) : 

```json
    "errors" : "First Name must not Blank!"
```

## Remove Contact

Endpoint : DELETE /api/contacts

Request Header : 
- X-API-TOKEN : token


Response Body (Success) : 

```json
{
    "data" : "OK"
}
```

Response Body (Failed) : 

```json
    "errors" : "Contact Not Found"
```

## Search Contact

Endpoint : GET /api/contacts

Query Parameter : 
- name : string, contact  first name or last name, Optional
- phone : string, contact phone, optional
- email : string, contact email, optional
- page : number, default 1
- size : number, default 10


Request Header : 
- X-API-TOKEN : token


Response Body (Success) : 

```json
{
    "data" : [
        {
        "id" : 1,
        "first_name" : "insan",
        "last_name" : "ibrahim",
        "email" : "insan5272@gmail.com",
        "phone" : "12121212"

        },
         {
        "id" : 2,
        "first_name" : "insan",
        "last_name" : "ibrahim",
        "email" : "insan5272@gmail.com",
        "phone" : "12121212"

        }
    ],
    "paging" : {
        "current_page" : 1,
        "total_page" : 10,
        "size" : 10
    }
}
```

Response Body (Failed) : 

```json
    "errors" : "Unauthorized"
```
