## **Коды ответов**

*`Для кода 201 (Created) - "Создано". Запрос успешно выполнен и в результате был создан ресурс. Этот код обычно присылается в ответ на запрос PUT "ПОМЕСТИТЬ".`*  

1. Код ответа: **200**. Тело ответа:  
```
[
    {
        "name": "Малышева Екатерина Матвеевна",
        "birthday": "1995-06-01",
        "post": "Бухгалтер"
    },
    {
        "name": "Капустин Роман Артёмович",
        "birthday": "1991-01-18",
        "post": "Финансовый аналитик"
    },
    {
        "name": "Касьянов Ярослав Ярославович",
        "birthday": "1989-07-29",
        "post": "Кредитный эксперт"
    },
    {
        "name": "Белова Елизавета Руслановна",
        "birthday": "1997-04-13",
        "post": "Аудитор"
    },
    {
        "name": "Романов Константин Александрович",
        "birthday": "2001-12-14",
        "post": "Кассир"
    },
    ...
]
```
---
*`Для кода 400 (Bad Request) - "Плохой запрос". Этот ответ означает, что сервер не понимает запрос из-за неверного синтаксиса.`*  

2. Код ответа: **401**. Тело ответа:  
```
{
  "message": "Неверные данные для авторизации."
}
```
---
*`Для кода 500 (Inrenal Server Error) - "Внутренняя ошибка сервера". Сервер столкнулся с ситуацией, которую он не знает как обработать.`*  

3. Код ответа: **400**. Тело ответа:  
```
{
  "message": "Неверно составлен запрос."
}
``` 