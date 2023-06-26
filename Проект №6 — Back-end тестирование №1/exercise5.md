# **Эндпоинты**

## **Activities**

### **1. GET /api/v1/Activities**

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-01T15:41:30.2371147+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-06-01T16:41:30.2371169+00:00",
    "completed": true
  },

    <...>

  {
    "id": 30,
    "title": "Activity 30",
    "dueDate": "2023-06-02T20:41:30.2371251+00:00",
    "completed": true
  }
]
```

### **2. POST /api/v1/Activities**

1. HTTP-метод: `POST`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities`
3. Заголовки запроса: `accept: text/plain; v=1.0`; `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-01T21:37:48.312Z",
  "completed": true
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-01T21:37:48.312Z",
  "completed": true
}
```

### **3. GET /api/v1/Activities/{id}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/15`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 15,
  "title": "Activity 15",
  "dueDate": "2023-06-02T12:59:47.0939177+00:00",
  "completed": false
}
```

### **4. GET /api/v1/Activities/{id}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/33`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `404`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-a761fc49f5cdd34e81fe13088324438d-5da3a71013596844-00"
}
```

### **5. PUT /api/v1/Activities/{id}** - *успех*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/15`
3. Заголовки запроса: `accept: text/plain; v=1.0`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-01T22:11:33.267Z",
  "completed": true
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-01T22:11:33.267Z",
  "completed": true
}
```

### **6. PUT /api/v1/Activities/{id}** - *провал*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/33333333333`
3. Заголовки запроса: `accept: text/plain; v=1.0`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-01T22:19:15.976Z",
  "completed": true
}
```
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-55c0e7af943eeb468cafb34e408ba286-f41a077b46978048-00",
  "errors": {
    "id": [
      "The value '33333333333' is not valid."
    ]
  }
}
```

### **7. DELETE /api/v1/Activities/{id}** - *успех*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/13`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа: `нет`

### **8. DELETE /api/v1/Activities/{id}** - *провал*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/99999999999999`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-3c1775f6bcd5544aa4d81689968079ad-8e8ab7f59e5eca41-00",
  "errors": {
    "id": [
      "The value '99999999999999' is not valid."
    ]
  }
}
```

---
---
---
## **Authors**

### **9. GET /api/v1/Authors**

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },

    <...>

    {
    "id": 590,
    "idBook": 200,
    "firstName": "First Name 590",
    "lastName": "Last Name 590"
  },
  {
    "id": 591,
    "idBook": 200,
    "firstName": "First Name 591",
    "lastName": "Last Name 591"
  }
]
```

### **10. POST /api/v1/Authors**

1. HTTP-метод: `POST`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors`
3. Заголовки запроса: `accept: text/plain; v=1.0`; `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### **11. GET /api/v1/Authors/authors/books/{idBook}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/101`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
  {
    "id": 297,
    "idBook": 101,
    "firstName": "First Name 297",
    "lastName": "Last Name 297"
  },
  {
    "id": 298,
    "idBook": 101,
    "firstName": "First Name 298",
    "lastName": "Last Name 298"
  },
  {
    "id": 299,
    "idBook": 101,
    "firstName": "First Name 299",
    "lastName": "Last Name 299"
  }
]
```

### **12. GET /api/v1/Authors/authors/books/{idBook}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/10000000000`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-eb0b1d90e8762049b93033db91d8a390-8efac1d1245ba84f-00",
  "errors": {
    "idBook": [
      "The value '10000000000' is not valid."
    ]
  }
}
```

### **13. GET /api/v1/Authors/{id}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/300`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 300,
  "idBook": 94,
  "firstName": "First Name 300",
  "lastName": "Last Name 300"
}
```

### **14. GET /api/v1/Authors/{id}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/600`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `404`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-731e48a7680b7f41a941434f1f12b207-cb49144c0a36724e-00"
}
```

### **15. PUT /api/v1/Authors/{id}** - *успех*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/70`
3. Заголовки запроса: `accept: text/plain; v=1.0`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### **16. PUT /api/v1/Authors/{id}** - *провал*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/666666666666`
3. Заголовки запроса: `accept: text/plain; v=1.0`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-d81107c46915e24ba223baa1ffd51b0d-a0c6256c7bb3f54d-00",
  "errors": {
    "id": [
      "The value '666666666666' is not valid."
    ]
  }
}
```

### **17. DELETE /api/v1/Authors/{id}** - *успех*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/444`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа: `нет`

### **18. DELETE /api/v1/Authors/{id}** - *провал*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/44444444444`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-7cba98e3f4517640acf40da8f9d9d99e-fbcd1dc561006041-00",
  "errors": {
    "id": [
      "The value '44444444444' is not valid."
    ]
  }
}
```
---
---
---
## **Books**

### **19. GET /api/v1/Books**

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-01T06:15:10.737445+00:00"
  },
  {
    "id": 2,
    "title": "Book 2",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 200,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-31T06:15:10.7374602+00:00"
  },

    <...>

  {
    "id": 200,
    "title": "Book 200",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 20000,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2022-11-14T06:15:10.7427991+00:00"
  }
]
```

### **20. POST /api/v1/Books**

1. HTTP-метод: `POST`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books`
3. Заголовки запроса: `accept: */*`; `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-02T06:16:49.272Z"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-02T06:16:49.272Z"
}
```

### **21. GET /api/v1/Books/{id}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/5`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 5,
  "title": "Book 5",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 500,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-05-28T06:19:41.7623867+00:00"
}
```

### **22. GET /api/v1/Books/{id}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/500`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `404`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-ac727529ded50c4a9f66eb01380a6776-e8ec97b4b125a84b-00"
}
```

### **23. PUT /api/v1/Books/{id}** - *успех*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/17`
3. Заголовки запроса: `accept: */*`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-02T06:21:06.937Z"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-02T06:21:06.937Z"
}
```

### **24. PUT /api/v1/Books/{id}** - *провал*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/171717171717`
3. Заголовки запроса: `accept: */*`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-02T06:21:06.937Z"
}
```
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6cbc00d861d3644f8cfff8c1f3ff64d3-60602b35017ef248-00",
  "errors": {
    "id": [
      "The value '171717171717' is not valid."
    ]
  }
}
```

### **25. DELETE /api/v1/Books/{id}** - *успех*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/1`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа: `нет`

### **26. DELETE /api/v1/Books/{id}** - *провал*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/-11100009999`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-26587a195bebf54aa71c9a93b2fcd893-a500874d3479ae49-00",
  "errors": {
    "id": [
      "The value '-11100009999' is not valid."
    ]
  }
}
```
---
---
---
## **CoverPhotos**

### **27. GET /api/v1/CoverPhotos**

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },

    <...>

    {
    "id": 200,
    "idBook": 200,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
  }
]
```

### **28. POST /api/v1/CoverPhotos**

1. HTTP-метод: `POST`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
3. Заголовки запроса: `accept: text/plain; v=1.0`; `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

### **29. GET /api/v1/CoverPhotos/books/covers/{idBook}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/20`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
  {
    "id": 20,
    "idBook": 20,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 20&w=250&h=350"
  }
]
```

### **30. GET /api/v1/CoverPhotos/books/covers/{idBook}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/900090009000`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-4576ba0cab91ec488014f2af4f4a2755-5db11c400819984a-00",
  "errors": {
    "idBook": [
      "The value '900090009000' is not valid."
    ]
  }
}
```

### **31. GET /api/v1/CoverPhotos/{id}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/66`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 66,
  "idBook": 66,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 66&w=250&h=350"
}
```

### **32. GET /api/v1/CoverPhotos/{id}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/-66`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `404`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-76606d374780fd4caacdb6ec1507c1ff-ad9faf205cc11748-00"
}
```

### **33. PUT /api/v1/CoverPhotos/{id}** - *успех*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/700`
3. Заголовки запроса: `accept: text/plain; v=1.0`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

### **34. PUT /api/v1/CoverPhotos/{id}** - *провал*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/-7777777777`
3. Заголовки запроса: `accept: text/plain; v=1.0`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-2081d1448315fc41bc7b7fabc48831ae-a1e9f56377629d45-00",
  "errors": {
    "id": [
      "The value '-7777777777' is not valid."
    ]
  }
}
```

### **35. DELETE /api/v1/CoverPhotos/{id}** - *успех*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/8000`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа: `нет`

### **36. DELETE /api/v1/CoverPhotos/{id}** - *провал*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/8888888888`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6d8dd4a203becd46aeeda126ed1231de-c6441e168b71e54c-00",
  "errors": {
    "id": [
      "The value '8888888888' is not valid."
    ]
  }
}
```
---
---
---
## **Users**

### **37. GET /api/v1/Users**

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users`
3. Заголовки запроса: `accept: text/plain; v=1.0`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
[
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
  {
    "id": 3,
    "userName": "User 3",
    "password": "Password3"
  },
  {
    "id": 4,
    "userName": "User 4",
    "password": "Password4"
  },
  {
    "id": 5,
    "userName": "User 5",
    "password": "Password5"
  },
  {
    "id": 6,
    "userName": "User 6",
    "password": "Password6"
  },
  {
    "id": 7,
    "userName": "User 7",
    "password": "Password7"
  },
  {
    "id": 8,
    "userName": "User 8",
    "password": "Password8"
  },
  {
    "id": 9,
    "userName": "User 9",
    "password": "Password9"
  },
  {
    "id": 10,
    "userName": "User 10",
    "password": "Password10"
  }
]
```

### **38. POST /api/v1/Users**

1. HTTP-метод: `POST`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users`
3. Заголовки запроса: `accept: */*`; `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 12,
  "userName": "user999",
  "password": "pasword999"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 12,
  "userName": "user999",
  "password": "pasword999"
}
```

### **39. GET /api/v1/Users/{id}** - *успех*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/9`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 9,
  "userName": "User 9",
  "password": "Password9"
}
```

### **40. GET /api/v1/Users/{id}** - *провал*

1. HTTP-метод: `GET`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/11`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `404`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-1f9003be95562a41bfbf77c34107f546-5ba9fff71aac2442-00"
}
```

### **41. PUT /api/v1/Users/{id}** - *успех*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/9`
3. Заголовки запроса: `accept: */*`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 9,
  "userName": "user91",
  "password": "pasword77"
}
```
5. Статус-код ответа: `200`
6. Тело ответа:
```
{
  "id": 9,
  "userName": "user91",
  "password": "pasword77"
}
```

### **42. PUT /api/v1/Users/{id}** - *провал*

1. HTTP-метод: `PUT`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/555555555555`
3. Заголовки запроса: `accept: */*`, `Content-Type: application/json; v=1.0`
4. Тело запроса:
```
{
  "id": 55,
  "userName": "user55",
  "password": "pasword55"
}
```
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-45a048e7f3996d47881a33617332a802-eb8a466a38b5fb42-00",
  "errors": {
    "id": [
      "The value '555555555555' is not valid."
    ]
  }
}
```

### **43. DELETE /api/v1/Users/{id}** - *успех*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/4`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `200`
6. Тело ответа: `нет`

### **44. DELETE /api/v1/Users/{id}** - *провал*

1. HTTP-метод: `DELETE`
2. Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/44444444444`
3. Заголовки запроса: `accept: */*`
4. Тело запроса: `нет`
5. Статус-код ответа: `400`
6. Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-f9563b63958c5b4bbae2c61b3ca4a6de-48ed13d79d55b54b-00",
  "errors": {
    "id": [
      "The value '44444444444' is not valid."
    ]
  }
}
```