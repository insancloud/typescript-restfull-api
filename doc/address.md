# Address API Spec

## Crete Address

Endpoint : POST /api/contacts/:idContact/adresses

Request Header : 
- X-API-TOKEN : token

Request Body : '

```json
{
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
}
```

Response Body (Success) :

```json
{
  "data"  : {
    "id" : 1,
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
  }
}

```

Response Body (Failed) : 

```json
{
    "errors" : "Postal Code is Required!"
}
```

## Get Address

Endpoint : GET /api/contacts/:idContact/adresses/:idAddress

Request Header : 
- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data"  : {
    "id" : 1,
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
  }
}

```

Response Body (Failed) : 

```json
{
    "errors" : "Address is not Found"
}
```

## Update Address

Endpoint : PUT /api/contacts/:idContact/adresses/:idAddress

Request Header : 
- X-API-TOKEN : token

Request Body : 

```json
{
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
}
```

Response Body (Success) :

```json
{
  "data"  : {
    "id" : 1,
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
  }
}

```

Response Body (Failed) : 

```json
{
    "errors" : "Postal Code is Required!"
}
```

## Remove Address

Endpoint : DELETE /api/contacts/:idContact/adresses/:idAdress

Request Header : 
- X-API-TOKEN : token


Response Body (Success) :

```json
{
  "data"  : "OK"
}

```

Response Body (Failed) : 

```json
{
    "errors" : "Address Is not Found"
}
```

## List Address

Endpoint : GET /api/contacts/:idContact/adresses

Request Header : 
- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data"  : [
     {
    "id" : 1,
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
     },
    {
    "id" : 2,
    "street" : "jalan Apa",
    "city" : "kota Apa",
    "province" : "Provinsi Apa",
    "country" : "Negara Apa",
    "postal_code" : "12323"
     }
  ]
}

```

Response Body (Failed) : 

```json
{
    "errors" : "Contact is not Found"
}
```