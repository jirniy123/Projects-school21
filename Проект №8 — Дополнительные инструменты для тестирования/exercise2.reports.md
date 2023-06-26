# **Баг-репорты**

## **Баг №1**

**Заголовок:**  
При обновлении сайта <https://sbermegamarket.ru/> блокируется сценарий

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
Сценарий с «https://mc.yandex.ru/metrika/tag.js» был заблокирован из-за неразрешенного MIME-типа («image/png»)

**Окружение:** 
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №2**

**Заголовок:**  
При загрузке сайта <https://sbermegamarket.ru/> ReferenceError

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
ReferenceError: overrideNavigatorData is not defined

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №3**

**Заголовок:**  
При загрузке сайта <https://sbermegamarket.ru/> заблокирован запрос из постороннего источника

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
Запрос из постороннего источника заблокирован: Политика одного источника запрещает чтение удаленного ресурса на https://vk.com/rtrg?p=VK-RTRG-1421183-77G99&products_event=view_home&price_list_id=1&e=1&i=0&metatag_url=https%3A%2F%2Fsbermegamarket.ru%2F&metatag_title=%D0%9C%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%20sbermegamarket.ru%20-%20%D0%BC%D0%B5%D1%81%D1%82%D0%BE%20%D0%B2%D1%8B%D0%B3%D0%BE%D0%B4%D0%BD%D1%8B%D1%85%20%D0%BF%D0%BE%D0%BA%D1%83%D0%BF%D0%BE%D0%BA. (Причина: отсутствует заголовок CORS «Access-Control-Allow-Origin»). Код состояния: 499.

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №4**

**Заголовок:**  
window.webim.api неопределен 

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
page url: https://sbermegamarket.ru/; message: watcher callback; details: TypeError, window.webim.api is undefined, resetWebimVisitor@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:403345

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №5**

**Заголовок:**  
Ошибка загрузки библиотеки

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
error loading "library" error="Error: script error "https://cdn.retailrocket.ru/content/javascript/tracking.js""

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №6**

**Заголовок:**  
Ошибка загрузки Uid Etag

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
Error load Uid Etag
```
v               https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
getUids         https://static.terratraf.io/GP/10002472.js:1
(Асинхронный:   promise callback)
getUids         https://static.terratraf.io/GP/10002472.js:1
init            https://static.terratraf.io/GP/10002472.js:1
<анонимный>     https://static.terratraf.io/GP/10002472.js:1
<анонимный>     https://static.terratraf.io/GP/10002472.js:1
```

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №7**

**Заголовок:**  
overrideNavigatorData не определен

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
ReferenceError: overrideNavigatorData is not defined
```
<анонимный>             blob:moz-extension://ca67d94e-6f1f-4342-a72a-7398b2638500/7d0af8c1-c1a6-46d2-a2fb-7171f29197b3:4
inject                  resource://gre/modules/ExtensionContent.jsm:593
AsyncFunctionNext       self-hosted:756
```

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №8**

**Заголовок:**  
Ошибка при попытке изсвлечения ресурса

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
Uncaught (in promise) TypeError: NetworkError when attempting to fetch resource.

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №9**

**Заголовок:**  
Ошибка доступа

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет

**Фактический результат:**  
Open api access error
```
v                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
onerror                 https://vk.com/js/api/openapi.js?169:672
s                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
(Асинхронный:           EventHandlerNonNull)
u                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
d                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
d                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
v                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
makeRequest             https://vk.com/js/api/openapi.js?169:678
ProductEvent            https://vk.com/js/api/openapi.js?169:3137
onViewedPage            https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
onViewedPage            https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
flushQueue              https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
n                       https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
s                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
(Асинхронный:           setInterval handler)
l                       https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
init                    https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
onLoadInitiated         https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
loadIntegration         https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
queueIntegrationLoad    https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
s                       https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
s                       https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
fireEvent               https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
fireEvent               https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
fireUnfiredEvents       https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
fireUnfiredEvents       https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
push                    https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
H                       https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
$                       https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
te                      https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
setLocationInfo         https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
fetchCurrentLocation    https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
fetchLocationData       https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
identifyRegion          https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
mounted                 https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
nn                      https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
zn                      https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
insert                  https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
```

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №10**

**Заголовок:**  
Ошибка синтаксического анализа Строка 5, символ 69:

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Обновить страницу <https://sbermegamarket.ru/>

**Ожидаемый результат:**  
Ошибок нет. Ожидаемый тег: </meta>

**Фактический результат:**  
Ошибка синтаксического анализа XML: несоответствующий тег.
Адрес: https://sbermegamarket.ru/api/fl?u=6efd37c0-6ff6-11ed-a2cf-b37c7b2b7873&cfidsw-smm=Im5Af7doHc6kIt0iE1QCgXURhJtULArCTUB8enVZYaiAvkojjcZ7uW0S3eBfQAwIuPAXww6FI38hgphrHSyla0%2FvfeFBkTXCqAIEvBqhRRPIx%2B30aoGgFWZvD3bL9KK0%2BVog4EFNEHJALcPdYfPB3QnYYyU4zVHcz2Ql91I%3D

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №11**

**Заголовок:**  
Встречен неожиданный тип.

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
Нажать на кнопку `Войти`

**Ожидаемый результат:**  
Ошибок нет.

**Фактический результат:**  
TypeError: obj is null

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №12**

**Заголовок:**  
Uncaught (in promise)

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
В футере нажать на кнопку `СберСпасибо`

**Ожидаемый результат:**  
Ошибок нет.

**Фактический результат:**  
Uncaught (in promise) Error: Redirected when going from "/" to "/landing/bonusy-sberspasibo/" via a navigation guard.

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)

---

## **Баг №13**

**Заголовок:**  
Загружаемый шрифт отклонен

**Предшествующие условия:**  
Открыта страница <https://sbermegamarket.ru/>

**Серьезность:**  
Trivial

**Шаги к воспроизведению:**  
В футере нажать на кнопку `О компании`

**Ожидаемый результат:**  
Ошибок нет.

**Фактический результат:**  
downloadable font: rejected by sanitizer (font-family: "Graphik LCG" style:normal weight:400 stretch:100 src index:0) source: https://main-cdn.sbermegamarket.ru/upload/static_pages/e/ab/738/eab738ad5e489ec2e334cf82dd047923/mobile/fonts/GraphikLCGRegular.eot

**Окружение:**  
Firefox Browser/114.0.1 (64-разрядный)
