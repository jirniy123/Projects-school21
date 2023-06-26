# **Activities**

## **1. Activities: GET**

**URL:**
```
{{activity_url}}
```

**Ожидаемый результат:**
``` 
1. Метод GET выполнен.
2. Получен статус-код 200.
3. Получен список Activities.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: cac562a3-85b9-482a-b131-03f6307c1a3c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:55:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-06-06T13:55:37.1512781+00:00",
        "completed": false
    },
    <...>
    {
        "id": 30,
        "title": "Activity 30",
        "dueDate": "2023-06-07T18:55:37.1512939+00:00",
        "completed": true
    }
]
```

## **2. Activities: POST**

**URL:**
```
{{activity_url}}
```

**Ожидаемый результат:**
```
1. Метод POST выполнен.
2. Получен статус-код 200.
3. Введенные данные Activities отправлены на сервер.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 4a1addc4-d2de-4b4b-af86-4a301b577f83
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 85
```

**Тело запроса**
```
{
"id": 31,
"title": "31",
"dueDate": "2023-06-05T08:33:42.835Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:02:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 31,
    "title": "31",
    "dueDate": "2023-06-05T08:33:42.835Z",
    "completed": true
}
```

## **3. Activities: POST - синтаксическая ошибка (нет "," после id)**

**URL:**
```
{{activity_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 2d0e6cb3-b307-4ea0-bc0e-4ed0b15b5bfa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 84
```

**Тело запроса**
```
{
"id": 31
"title": "31",
"dueDate": "2023-06-05T08:33:42.835Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:06:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c15904f755a9b44ea8955f1fd8e1199d-3ffb858af3c3254a-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 0."
        ]
    }
}
```

## **4. Activities: POST - id строка**

**URL:**
```
{{activity_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 0432f89a-2303-428a-9c3b-120c867f16c4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 88
```

**Тело запроса**
```
{
"id": "DDD",
"title": "25",
"dueDate": "2023-06-05T08:33:42.835Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:08:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1940cb9243a99442867ea347e7b0c5fa-df60f001fb747744-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```

## **5. Activities: POST - title число**

**URL:**
```
{{activity_url}}
```

**Ожидаемый результат:** 
```
1. Метод POST не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 0fc5d977-01d4-4613-8ee6-c99be38d0946
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 83
```

**Тело запроса**
```
{
"id": 17,
"title": 17,
"dueDate": "2023-06-05T08:33:42.835Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:10:19 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9fd66c287848844cace7e50bdac7cdec-e76236837674b74b-00",
    "errors": {
        "$.title": [
            "The JSON value could not be converted to System.String. Path: $.title | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```

## **6. Activities: POST - без тела запроса**

**URL:**
```
{{activity_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 415
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 16c226a7-107d-4c96-9e87-a33b90e3b809
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:12:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-5b5050efacf3dc4897890de58a5e4bbf-7dcb3914d566e344-00"
}
```

## **7. Activities: GET {id}**

**URL:**
```
{{activity_url}}/{{activity_id}}
```

**Ожидаемый результат:**
```
1. Метод GET выполнен.
2. Получен статус-код 200.
3. Получена информация для id=30 из списка Activities.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: bea954ec-0317-4ff3-8776-16a6e6d78a51
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:14:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 30,
    "title": "Activity 30",
    "dueDate": "2023-06-07T19:14:11.0790783+00:00",
    "completed": true
}
```

## **8. Activities: GET {id} отсутствующий id**

**URL:**
```
{{activity_url}}/{{activity_idd}}
```

**Ожидаемый результат:**
```
1. Метод GET не выполнен.
2. Получен статус-код 404 (Not Found)
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 021e444e-9bbe-400c-805c-01feaa756e86
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:15:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-39282dda99836248a337bdd5c869b7c4-1ee1e6e61021464e-00"
}
```

## **9. Activities: PUT**

**URL:**
```
{{activity_url}}/31
```

**Ожидаемый результат:**
```
1. Метод PUT выполнен.
2. Получен статус-код 200.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 67a93e0d-c035-428d-91d9-657bc88cc360
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 94
```

**Тело запроса**
```
{
"id": 31,
"title": "Activity 31",
"dueDate": "2023-06-05T08:42:29.756Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:25:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 31,
    "title": "Activity 31",
    "dueDate": "2023-06-05T08:42:29.756Z",
    "completed": true
}
```

## **10. Activities: PUT - синтаксическая ошибка (нет "," после title)**

**URL:**
```
{{activity_url}}/31
```

**Ожидаемый результат:**
```
1. Метод PUT не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: acaa4ee9-b996-42bf-806d-ea4df5298549
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 93
```

**Тело запроса**
```
{
"id": 31,
"title": "Activity 31"
"dueDate": "2023-06-05T08:42:29.756Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:27:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-67de7d6c82537c4586516f325f9b2766-8017e0d91be35e49-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 0."
        ]
    }
}
```

## **11. Activities: PUT - id строка**

**URL:**
```
{{activity_url}}/31
```

**Ожидаемый результат:**
```
1. Метод PUT не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 421b196f-4b50-4e04-9227-b0bdb672c459
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 94
```

**Тело запроса**
```
{
"id": "Q",
"title": "Activity 31"
"dueDate": "2023-06-05T08:42:29.756Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:29:27 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e2f5f3b38891724da630c3e23074ff17-5fcb189db958f746-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
        ]
    }
}
```

## **12. Activities: PUT - title число**

**URL:**
```
{{activity_url}}/31
```

**Ожидаемый результат:**
```
1. Метод PUT не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 1c14d367-677a-4ea6-b891-f94c29f4df40
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 83
```

**Тело запроса**
```
{
"id": 31,
"title": 31,
"dueDate": "2023-06-05T08:42:29.756Z",
"completed": true
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:30:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6852349a89bd7b438c82f9d639e98740-0cb324d4ab489341-00",
    "errors": {
        "$.title": [
            "The JSON value could not be converted to System.String. Path: $.title | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```

## **13. Activities: PUT - без тела запроса**

**URL:**
```
{{activity_url}}/31
```

**Ожидаемый результат:**
```
1. Метод PUT не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 541458d2-21b1-4280-a066-6a66cf82ca61
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:32:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-9c162bc9eb74694a9a8d627e07cc271e-ad39283fded3254b-00"
}
```

## **14. Activities: DELETE**

**URL:**
```
{{activity_url}}/20
```

**Ожидаемый результат:**
```
1. Метод DELETE выполнен.
2. Получен статус-код 200.
3. Из списка Activities удалены данные id=20
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 8f9a6bfa-f366-46c2-b050-cb9c84034e49
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 13:33:35 GMT
Server: Kestrel
api-supported-versions: 1.0
```

## **15. Activities: DELETE - отсутствующий id БАГ**

**URL:**
```
{{activity_url}}/50
```

**Ожидаемый результат:**
```
1. Метод DELETE не выполнен.
2. Получен статус-код 404 (Not Found).
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: fbb7fa4a-abb9-49e9-b555-3eee028e43be
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 13:35:08 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# **Authors**

## **1. Authors: GET**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
1. Метод GET выполнен.
2. Получен статус-код 200.
3. Получен список Authors.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: b58eac4b-0eb5-4a9b-b4ee-e58da9f046ae
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:36:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },
    <...>
    {
        "id": 592,
        "idBook": 200,
        "firstName": "First Name 592",
        "lastName": "Last Name 592"
    }
]
```

## **2. Authors: GET - повторный запрос "Execute" БАГ**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
Получен тот же список Authors, что и в "1. Authors: GET"
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: c5e43dab-536f-486b-97af-d8715d81dd5c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:41:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },
    <...>
    {
        "id": 611,
        "idBook": 200,
        "firstName": "First Name 611",
        "lastName": "Last Name 611"
    }
]
```

## **3. Authors: POST**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
1. Метод POST выполнен.
2. Получен статус-код 200.
3. Введенные данные Authors отправлены на сервер.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 44a18cd3-0ee6-4e3e-b8a6-9581a7224c67
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 73
```
**Тело запроса**  
```
{
"id": 700,
"idBook": 666,
"firstName": "string",
"lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:43:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 700,
    "idBook": 666,
    "firstName": "string",
    "lastName": "string"
}
```

## **4. Authors: POST - синтаксическая ошибка (нет "," после id)**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 6812af6d-91c5-4ce0-b3c5-153fabe5e815
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 72
```
**Тело запроса**  
```
{
"id": 800
"idBook": 555,
"firstName": "string",
"lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:45:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-36e1381448e45f4682847759d20d26e1-3ade5f0ff622994e-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 0."
        ]
    }
}
```

## **5. Authors: POST - id строка**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 75747978-3657-45ab-bdc5-134f65836cb0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 74
```
**Тело запроса**  
```
{
"id": "QW",
"idBook": 555,
"firstName": "string",
"lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:46:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ee7aecbe4e585144a50b2d42c24bb33b-d42c134b9adc2640-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."
        ]
    }
}
```

## **6. Authors: POST - idBook строка**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 400 (Bad Request)
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 7f963cf4-185e-4146-b41d-24f5e676efb5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 75
```
**Тело запроса**  
```
{
"id": 700,
"idBook": "AAA",
"firstName": "string",
"lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:48:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2281b921029b2b4ab1c2f9145f2b9bb5-005d5e6189f1b245-00",
    "errors": {
        "$.idBook": [
            "The JSON value could not be converted to System.Int32. Path: $.idBook | LineNumber: 2 | BytePositionInLine: 15."
        ]
    }
}
```

## **7. Authors: POST - без тела запроса**

**URL:**
```
{{authors_url}}
```

**Ожидаемый результат:**
```
1. Метод POST не выполнен.
2. Получен статус-код 415
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: bcbf780d-1182-4111-a125-74da18e0e24f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:49:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-bc2ac3c2d9b04e47903f4be0389b23ba-49aef329cd56004e-00"
}
```

## **8. Authors: GET {idBook} БАГ**

**URL:**
```
{{authorsBook_url}}/100
```

**Ожидаемый результат:**
```
1. Метод GET выполнен.
2. Получен статус-код 200.
3. Получена информация для idBook=100 из списка Authors.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: f877fe52-7c04-4b7b-b7d8-2970bd903df4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:50:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[
    {
        "id": 307,
        "idBook": 100,
        "firstName": "First Name 307",
        "lastName": "Last Name 307"
    },
    {
        "id": 308,
        "idBook": 100,
        "firstName": "First Name 308",
        "lastName": "Last Name 308"
    },
    {
        "id": 309,
        "idBook": 100,
        "firstName": "First Name 309",
        "lastName": "Last Name 309"
    }
]
```

## **9. Authors: GET {idBook} отсутствующий id БАГ**

**URL:**
```
{{authorsBook_url}}/800
```

**Ожидаемый результат:**
```
1. Метод GET не выполнен.
2. Получен статус-код 404 (Not Found)
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 7852f66b-72c9-403d-ba0b-9b5a60acebbd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:52:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[]
```

## **10. Authors: GET {id} БАГ**

**URL:**
```
{{authors_url}}/30
```

**Ожидаемый результат:**
```
1. Метод GET выполнен.
2. Получен статус-код 200.
3. Получена информация для id=30 из списка Authors.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 74fa162b-d725-4914-a606-96f049ea23f3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:54:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 30,
    "idBook": 10,
    "firstName": "First Name 30",
    "lastName": "Last Name 30"
}
```

## **11. Authors: GET {id} отсутствующий id**

**URL:**
```
{{authors_url}}/800
```

**Ожидаемый результат:**
```
1. Метод GET не выполнен.
2. Получен статус-код 404 (Not Found)
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 0a377947-527d-4df7-9c49-4f30ec3aa01f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:55:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-40cc3b21df036c419fbda6f382cc061f-9ee14283e2d99148-00"
}
```

## **12. Authors: PUT - успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 200
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: e3f62181-f500-43fa-98b4-03ed3f78dc56
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 80
```

**Тело запроса**
```
{
 "id": 26,
 "idBook": 26,
 "firstName": "string",
 "lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:39:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 26,
    "idBook": 26,
    "firstName": "string",
    "lastName": "string"
}
```

## **13. Authors: PUT - некорректный JSON**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: d95269a3-1565-4e91-9642-692c6d12bc86
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 90
```

**Тело запроса**
```
{
 "id": 26,
 "idBook": 26,
 {}}}{^&
 "firstName": "string",
 "lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:44:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-01f061c10290d54aa1e7fd7048197891-901d2650d46e134d-00",
    "errors": {
        "$": [
            "'{' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 3 | BytePositionInLine: 1."
        ]
    }
}
```

## **14. Authors: PUT - изменения типа значений**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 46b96e60-3eae-428e-9154-4de46aece7eb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 88
```

**Тело запроса**
```
{
 "id": "null",
 "idBook": "null",
 "firstName": "string",
 "lastName": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:48:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-218f6d3fa78ee64aa60bd51939bd2a80-e4b20bc3e705af41-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 13."
        ]
    }
}
```

## **15. Authors: PUT - отправка пустых строк**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 7125b764-d4f4-4bee-aabf-e942abbde38d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 60
```

**Тело запроса**
```
{
 "id": ,
 "idBook": ,
 "firstName": ,
 "lastName": 
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:50:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3fe7268f3885e2438169ab958a1d61ec-95273873cd177242-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```

## **16. Authors: PUT - введение некорректного id**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id_neg}}
```
**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 6d3a9cc2-e299-4f4a-8e57-7b2c2563c331
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 90
```

**Тело запроса**
```
{
 "id": 45144165878,
 "idBook": 1,
 "firstName": "string",
 "lastName": "string"

}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:52:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b20a1756ac271d4f9b36e2d9548bd0d4-360feb4e849cb942-00",
    "errors": {
        "id": [
            "The value '45144165878' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```

## **17. Authors​: DELETE {id} - успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id}}
```

**Ожидаемый результат:**
```
Запрос успешно обработан, статус-код: 200 ОК
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 84ea6ce1-1340-469d-98ad-fb769592ae7a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**  `отсутствует`

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 13:16:19 GMT
Server: Kestrel
api-supported-versions: 1.0
```

**Тело ответа:** `отсутствует`

## **18. Authors​: DELETE{id}  - введение некорректного id**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{authors_id_neg}}
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f2c84a0c-e007-44dc-aa59-6042ae39a042
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:** `отсутствует`

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:19:40 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-695c7cb9ba62004ba21323c57a9fb4db-5f48e6f5f6448d47-00",
    "errors": {
        "id": [
            "The value '45144165878' is not valid."
        ]
    }
}
```

## **19. Authors: DELETE - отсутствующий id БАГ**

**URL:**
```
{{authors_url}}/777
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 66271951-feb2-4414-bf06-3e9a7e73a8f5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 13:26:43 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# **Books**

## **1. Books: GET - успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books
```

**Ожидаемый результат:**
```
Запрос успешно обработан, статус-код: 200 ОК
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5fd511fa-ef38-4f39-8d71-f28632b228f1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:29:47 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```

    {
        "id": 1,
        "title": "Book 1",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 100,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-06-05T13:29:47.2308596+00:00"
    },<...>
```

## **2. Books: POST - успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books
```

**Ожидаемый результат:**
```
Запрос успешно обработан, статус-код: 200 ОК
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7bce5699-e2be-4659-91d2-3233dd46f3d9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 156
```

**Тело запроса:**
```
{
  "id": 500,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T08:05:06.586Z"
}
``` 

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:33:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 500,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-06T08:05:06.586Z"
}
```

## **3. Books: POST - некорректный JSON**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0ebddfe3-881d-40ec-917c-8095e7a7fdef
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 167
```

**Тело запроса:**
```
{
  "id": 500,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  {}}}{^&
  "excerpt": "string",
  "publishDate": "2023-06-06T08:05:06.586Z"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:35:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7b30256c80ed844d8a844d0bd4b829f0-571035f253149a44-00",
    "errors": {
        "$": [
            "'{' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 5 | BytePositionInLine: 2."
        ]
    }
}
```

## **4. Books: POST - изменения типа значений**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 52f78fa9-4f1f-41f3-a561-cd25ffca1966
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 159
```

**Тело запроса:** 
```
{
  "id": "null",
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T08:05:06.586Z"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:38:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b49037d37e06504e96ef1c5592710ec7-56df1c6a81ede846-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 14."
        ]
    }
}
```

## **5. Books: POST - отправка пустых строк**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 079f308d-6ce6-4592-a6ec-9d7527a3d9dc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 101
```

**Тело запроса:** 
```
{
  "id": ,
  "title": ,
  "description": ,
  "pageCount": ,
  "excerpt": ,
  "publishDate":
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:41:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d7a8fee316f90c4195ca2b2e7f558511-074855f647b85946-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
        ]
    }
}
```

## **6. Books: GET {id}- успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id}}
```

**Ожидаемый результат:**
```
Запрос успешно обработан, статус-код: 200 ОК
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9a1bd503-8405-40b2-af52-a849ca94e272
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:43:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 26,
    "title": "Book 26",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 2600,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-11T13:43:01.3497348+00:00"
}
```

## **7. Books: GET {id}- введение некорректного id**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id_neg}}
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fed0feae-d827-4fc3-9eca-8ebd2ed643d6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:45:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-377e9ade67d3b247a62e6e38351d18db-b26005fe8281e946-00",
    "errors": {
        "id": [
            "The value '334568096635' is not valid."
        ]
    }
}
```

## **8. Books: PUT {id}- успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id}}
```

**Ожидаемый результат:**
```
Запрос успешно обработан, статус-код: 200 ОК
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: cdcea1a1-775a-4b3e-80cd-5ae03673b343
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 149
```

**Тело запроса:** 
```
{
 "id": 26,
 "title": "string",
 "description": "string",
 "pageCount": 0,
 "excerpt": "string",
 "publishDate": "2023-06-05T07:20:56.645Z"
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:47:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 26,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-05T07:20:56.645Z"
}
```

## **9. Books: PUT {id}- некорректный JSON**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id}}
```
**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fd13970c-8104-4451-9251-308a317f5041
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 159
```

**Тело запроса:** 
```
{
 "id": 26,
 "title": "string",
 "description": "string",
 "pageCount": 0,
 {}}}{^&
 "excerpt": "string",
 "publishDate": "2023-06-05T07:20:56.645Z"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:49:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9c2d4d80cac49a4ba1ebff598f2698e6-7bb800faac3d3845-00",
    "errors": {
        "$": [
            "'{' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 5 | BytePositionInLine: 1."
        ]
    }
}
```

## **10. Books: PUT {id}- изменения типа значений**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id}}
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 68f2c1c7-2591-4c63-829f-cb1901b0fac6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 153
```

**Тело запроса: **
```
{
 "id": "null",
 "title": "string",
 "description": "string",
 "pageCount": 0,
 "excerpt": "string",
 "publishDate": "2023-06-05T07:20:56.645Z"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:51:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b437aa02fde84545b546581a915efa3c-f3ae4e890143af4c-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 13."
        ]
    }
}
```

## **11. Books: PUT {id}- отправка пустых строк**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id}}
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: db2505ed-92b2-46cd-837d-b00d9ebb2130
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 96
```

**Тело запроса: **
```
{
 "id": ,
 "title": ,
 "description": ,
 "pageCount": ,
 "excerpt": ,
 "publishDate": 
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:53:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-397d3de725022b4db773c92150d63efe-51ca3cddf3eb7946-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```

## **12. Books: PUT {id}- введение некорректного id**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id_neg}}
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a4afdcee-981b-4b07-af1a-0e50a03d1fc6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 159
```

**Тело запроса:**
```
{
 "id": 616411674641,
 "title": "string",
 "description": "string",
 "pageCount": 0,
 "excerpt": "string",
 "publishDate": "2023-06-05T07:28:04.194Z"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:55:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4541cdfc3985044491cb5b1bac04b455-e19b477520ec0747-00",
    "errors": {
        "id": [
            "The value '334568096635' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 19."
        ]
    }
}
```

## **13. Books: DELETE {id}- успешный запрос**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id}}
```

**Ожидаемый результат:**
```
Запрос успешно обрабатывается, статус-код: 200 ОК
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7bcd8f98-84d8-4315-86a2-c83d36ca7398
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 13:04:08 GMT
Server: Kestrel
api-supported-versions: 1.0
```

## **14. Books: DELETE {id}- введение некорректного id**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/{{books_id_neg}}
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ea4ccbf3-e283-4b0a-ba05-e662f6d35923
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:59:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a000c7c56e02864fbedc984adea5ae2c-9338305b60e26a4c-00",
    "errors": {
        "id": [
            "The value '334568096635' is not valid."
        ]
    }
}
```

## **15. Books: DELETE {id}- отсутствующий id БАГ**

**URL:**
```
https://fakerestapi.azurewebsites.net/api/v1/Books/201
```

**Ожидаемый результат:**
```
Запрос с некорректными данными, статус-код: 400 Bad Request
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 1860174d-c0e2-43c5-afeb-10e10177764c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 14:02:01 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# **CoverPhotos**

## **1. CoverPhotos: GET - успешный запрос**

**URL:**
```
{{cover_url}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 200
3. Получен Response body
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 28ea7448-2ec8-4e3b-9f8d-dfe566271fd9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 07:54:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    <...>
    {
        "id": 200,
        "idBook": 200,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
    }
]
```

## **2. CoverPhotos: POST - успешный запрос**

**URL:**
```
{{cover_url}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 200
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: da70c627-f92e-487c-a759-7f41692ec401
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 46
```
**Тело запроса**
```
{
 "id": 26,
 "idBook": 26,
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:51:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 26,
    "idBook": 26,
    "url": "string"
}
```

## **3. CoverPhotos: POST - некорректный JSONс**

**URL:**
```
{{cover_url}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 2bee099f-060a-47ec-973d-dc80eae1d444
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 54
```
**Тело запроса**
```
{
 "id": 26,
 "idBook": 26,
{}}}{^&
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:53:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-23d9264379aef84eb1f4e06a53f26634-97e840921393d347-00",
    "errors": {
        "$": [
            "'{' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 3 | BytePositionInLine: 0."
        ]
    }
}
```

## **4. CoverPhotos: POST - изменения типа значений**

**URL:**
```
{{cover_url}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 56de22fa-d527-4296-b04d-637f5edccf7a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 50
```
**Тело запроса**
```
{
 "id": null,
 "idBook": null,
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:56:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e176fc7c012de545b9a0fa38dc1e35c2-279b0d6794fc9f4b-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```

## **5. CoverPhotos: POST - отправка пустых строк**

**URL:**
```
{{cover_url}}
```

**Ожидаемый результат:**
```
1. Запрос отправлен
2. Получен статус - код 400
3. Получен Response body
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 1aee4f36-8fb4-482e-b6b5-2ca7444f33df
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 34
```
**Тело запроса**
```
{
 "id": ,
 "idBook": ,
 "url": 
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:00:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c699b43a3f2ebf4ebf90ab3e2dfb79d1-4f77934e77049f44-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```

## **6. CoverPhotos Get /api/v1/CoverPhotos/books/covers/{idBook}-успешный запрос, код 200**

**URL:**
```
{{coverBook_url}}/1
```

**Ожидаемый результат:**
```
Запрос успешно прошел. Код-200
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: cf462020-7657-4c98-9776-b502fe5b123e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 07:54:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    }
]
```

## **7. CoverPhotos: GET /api​/v1​/CoverPhotos​/books​/covers​/{idBook} - Неверное значение id,Код 400**

**URL:**
```
{{coverBook_url}}/11111111111
```

**Ожидаемый результат:**  
```
Запрос не проходит. Выдает ошибку код - 400.
```

**Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d8d49045-ede6-4910-829d-1179f59500eb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 07:58:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-45dcb4de99c8c0489dff26a26ed5e4d1-8abe66fc7cde6841-00",
    "errors": {
        "idBook": [
            "The value '11111111111' is not valid."
        ]
    }
}
```

## **8. CoverPhotos: GET /api​/v1​/CoverPhotos​/{id} - успешный запрос, Код 200**

**URL:**
```
{{cover_url}}/22
```

**Ожидаемый результат:**  
```
Запрос успешно прошел. Код-200
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5f881be5-4783-4e0a-87c8-002cf7d294cd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 08:02:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 22,
    "idBook": 22,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 22&w=250&h=350"
}
```

## **9. CoverPhotos:  - GET/api/v1/CoverPhotos/{id} -Неверное значение id, Код 404**

**URL:**
```
{{cover_url}}/500
```

**Ожидаемый результат:**  
```
При введении неверного значение id, запрос не проходит и выдает ошибку - код 404.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d5eca211-3223-4e2c-9504-a00033c914a3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 09:16:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-4c3b8271395e5647a53e2be823131a74-e04889c5ac721943-00"
}
```

## **10. CoverPhotos: PUT/api/v1/CoverPhotos/{id} - успешный запрос, Код 200**

**URL:**
```
{{cover_url}}/3
```

**Ожидаемый результат:**  
```
Запрос успешно прошел. Код - 200. 
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2a817bba-2d0c-453e-99a8-c010cc96f849
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": 3,
 "idBook": 0,
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 09:15:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "id": 3,
    "userName": null,
    "password": null
}
```

## **11. CoverPhotos: PUT/api/v1/CoverPhotos/{id} - изменение типов значений, код 400**

**URL:**
```
{{cover_url}}/3
```

**Ожидаемый результат:**  
```
При измененении значения id, запрос выдает ошибку  - код 404.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d2bb92bc-fe58-412a-b142-028928ceece0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": one,
 "idBook": 0,
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 09:15:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c6905e26618e6a4bb01ab2bdb8093e9b-52aea1f28308374c-00",
    "errors": {
        "$.id": [
            "'o' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```

## **12. CoverPhotos: PUT/api/v1/CoverPhotos/{id} - внесение пустых строчек, код 400**

**URL:**
```
{{cover_url}}/3
```

**Ожидаемый результат:**  
```
При внесении пустых строчек, запрпос выдает ошибку код 400. 
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5204ee13-b306-4082-ba39-e7760e189372
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": " ",
 "idBook": " ",
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 09:15:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-934063fe78db07408cb4a7c4f8955508-8814818c072fdf41-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."
        ]
    }
}
```

## **13. CoverPhotos: PUT/api/v1/CoverPhotos/{id} - некорректный JSON, код 400**

**URL:**
```
{{cover_url}}/3
```

**Ожидаемый результат:**  
```
При введении некорректного JSON, запрос выдает ошибку код 400.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f8ff4dfe-a9ab-44be-b454-7f6a51b301fb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": 3,
 "idBook": 3((()))%,
 "url": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 10:37:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d745226200bdb3408a3e3a75c9d05670-65800785453c8643-00",
    "errors": {
        "$.idBook": [
            "'(' is an invalid end of a number. Expected a delimiter. Path: $.idBook | LineNumber: 2 | BytePositionInLine: 12."
        ]
    }
}
```

## **14. CoverPhotos: DELETE/api/v1/CoverPhotos/{id} - успешный запрос- Код 200**

**URL:**
```
{{cover_url}}/10
```

**Ожидаемый результат:**  
```
Запрос прошел успешн. Код- 200.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 78de3b2d-ed51-4079-9ea4-408d44e3b6e7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 09:19:36 GMT
Server: Kestrel
api-supported-versions: 1.0
```

## **15. CoverPhotos: DELETE/api/v1/CoverPhotos/{id} - Неверное значение id, Код 400**

**URL:**
```
{{cover_url}}/2222222222
```

**Ожидаемый результат:**  
```
При внесении неверного значание id, запрос выдает ошибку - код 400
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a54433a5-cf0a-4f53-a0fd-b6191bfdc545
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 09:15:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-07d89f38dc79534cb07948e867927d90-6c7b6f32a499024c-00",
    "errors": {
        "id": [
            "The value '2222222222' is not valid."
        ]
    }
}
```

## **16. CoverPhotos: GET /api​/v1​/CoverPhotos​/books​/covers​/{idBook} - Баг**

**URL:**
```
{{coverBook_url}}/500
```

**Ожидаемый результат:**  
```
При внесении неверного id- запрос выдаед ошибку - 400.
```

**Фактический результат:**  
```
Запрос успешно проведен, код 200.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 278c4337-d0f0-4245-ae9f-3089ae3a69c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 10:46:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
[]
```

## **17. CoverPhotos: DELETE/api/v1/CoverPhotos/{id} - Баг**

**URL:**
```
{{cover_url}}/500
```
**Ожидаемый результат:**  
```
При введении неверного id, запрос выдаедт ошибку- код 400
```

**Фактический результат:**  
```
Запрос  прошел, код 200. 
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ea3f5d0a-fa16-4087-b4e6-b898e9d4f414
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 10:52:08 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# **Users**

## **1. Users GET/api/v1/Users - успешный запрос, код 200**

**URL:**
```
{{users_url}}
```

**Ожидаемый результат:**  
```
Успешный запрос, код 200
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 521af75d-701c-4c6f-9fd9-f957833ced53
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 09:20:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```

    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
    {
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
    },
```

## **2. Users - POST/api/v1/Users- успешный запрос, код 200**

**URL:**
```
{{users_url}}
```

**Ожидаемый результат:**  
```
Успешный запрос. 
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 8eb38f31-54cf-44cf-a076-59d1c0bbb6fc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": 0,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 09:11:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```

## **3. Users - POST/api/v1/Users- некорректный JSON, код 400**

**URL:**
```
{{users_url}}
```

**Ожидаемый результат:**  
```
Запрос выдает ошибку - код 400
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ecc64b37-12fe-48bb-adc4-e1b14431db7f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": 11111111111,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:02:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6f2237d522671f4f900630c5f5491360-d8961c890ed7374e-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```

## **4. Users - POST/api/v1/Users- пустая строка, код 400**

**URL:**
```
{{users_url}}
```

**Ожидаемый результат:**  
```
При внесении пустой сроки запрос выдает ошибку - код 400
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 026ba7fc-022b-4133-864e-f5b4cb5739a3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id":  ,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:05:22 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1ac2f90fb590cc43880f2257ab488607-a87fd2adcbe29842-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```

## **5. Users - POST/api/v1/Users- изменение типа значения, код 400**

**URL:**
```
{{users_url}}
```

**Ожидаемый результат:**  
```
Запрос выдает ошибку - код 400
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 87a840cf-88f6-46f5-bead-5ddc347684ec
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": null,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:09:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0e104fff98cf8a42aba5587d76d0fb70-b7ca89a740a12b46-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```

## **6. Users - GET/api/v1/Users/{id}- успешный запрос, код 200**

**URL:**
```
{{users_url}}/5
```

**Ожидаемый результат:**  
```
Успешно пройденный запрос. Код - 200.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 392d582f-c329-478f-8c2d-bb26f968be50
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:10:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 5,
    "userName": "User 5",
    "password": "Password5"
}
```

## **7. Users - GET/api/v1/Users/{id}- неверный id, код 404**

**URL:**
```
{{users_url}}/99090999
```

**Ожидаемый результат:**  
```
Запрос выдает ошибку - код 404. 
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7daa0d50-5173-49ab-9397-4bbefe973457
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:14:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-2b52a2669da0314c9733df561e03d1a4-00d7588bdcf6a043-00"
}
```

## **8. Users - PUT/api/v1/Users/{id}- успешный запрос, код 200**

**URL:**
```
{{users_url}}/5
```

**Ожидаемый результат:** 
``` 
Запрос прошел успешно - код 200.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 344edc4a-7f62-4570-a11c-9e5407ea2754
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": 5,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:16:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

**Тело ответа:**
```
{
    "id": 5,
    "userName": "string",
    "password": "string"
}
```

## **9. Users - PUT/api/v1/Users/{id}-некорректный JSON, код 400**

**URL:**
```
{{users_url}}/5
```

**Ожидаемый результат:**  
```
При некорректном JSON  запрос выдает ошибку - 400.
```

**Заголовки запроса:**
```
ontent-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 97829397-a780-4c36-8d49-c87414062c38
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": 09,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:18:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8e1ee931b27fd64c820b314485b8d08f-6757a1a60ee0054f-00",
    "errors": {
        "$.id": [
            "Invalid leading zero before '9'. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
        ]
    }
}
```

## **10. Users - PUT/api/v1/Users/{id} - пустая срока, код 400**

**URL:**
```
{{users_url}}/5
```

**Ожидаемый результат:**  
```
Запрос  выдает ошибку - код 400.
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 114c3bb1-badd-45a5-ba69-beed1687b01a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{
 "id": ,
 "userName": "string",
 "password": "string"
}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:21:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f5870bcea54d9f489cfa2bed635d8943-faf6727ab52af24a-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```

## **11. Users - PUT/api/v1/Users/{id} - изменения типа значений, код 400**

**URL:**
```
{{users_url}}/5
```

**Ожидаемый результат:**  
```
Запрос выдает ошибку - код 400
```

**Заголовки запроса:**
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4f0b8e6e-9e9c-4b3b-a07c-b08f9c7997e6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Тело запроса:**
```
{

 "id": null,

 "userName": "string",

 "password": "string"

}
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:24:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1459d07f05c89c4788f25a60628b4ee7-10f5110172338249-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```

## **12. Users - DELETE/api/v1/Users/{id}- успешный запрос, код 200**

**URL:**
```
{{users_url}}/5
```

**Ожидаемый результат:**  
```
Запрос прошел успешно - код 200.
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 741773cb-831e-420b-b106-8bc362e47130
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 09:16:32 GMT
Server: Kestrel
api-supported-versions: 1.0
```

## **13. Users - DELETE/api/v1/Users/{id}- неверный id , код 400**

**URL:**
```
{{users_url}}/11111111111
```

**Ожидаемый результат:**  
```
Запрос выдает ошибку - код 400. 
```

**Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0755a2db-db34-4875-972c-0e2870968b6d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:28:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5d7edd0e19ed70418cf8940479a9626d-00529067baaaf747-00",
    "errors": {
        "id": [
            "The value '11111111111' is not valid."
        ]
    }
}
```

## **14. Users - DELETE/api/v1/Users/{id}- Баг**

**URL:**
```
{{users_url}}/99090999
```

**Ожидаемый результат:**  
```
Запрос выдает ошибку- код 400.
```

**Фактический результат:**  
```
Запрос прошел успешно -код 200. 
```

**Заголовки запроса:**
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c0ab12db-6494-42d5-b8f2-6b8aefe831e9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

**Заголовки ответа:**
```
Content-Length: 0
Date: Tue, 06 Jun 2023 11:30:55 GMT
Server: Kestrel
api-supported-versions: 1.0
```