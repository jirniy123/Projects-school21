<font size=2> 

# Чек-лист

#### Тест-кейс №1. Авторизация для *"standard_user"*  

`Результат:` <font color=limegreen size=3>`пройден`</font>

#### Тест-кейс №2. Авторизация для *"locked_out_user"*  

`Результат:` <font color=red size=3>`провален`</font> `Пользователь заблокирован: "Epic sadface: Sorry, this user has been locked out."`

#### Тест-кейс №3. Авторизация для *"problem_user"*  

`Результат:` <font color=limegreen size=3>`пройден`</font>

#### Тест-кейс №4. Авторизация для *"performance_glitch_user"* 

`Результат:` <font color=limegreen size=3>`пройден`</font>`Неожиданное поведение приложения: наблюдается задержка в переходе на главную страницу интернет-магазина`

#### Тест-кейс №5. Добавление товара в корзину

<font color=black size=1> 

|Вариант №|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|:-:|
| |`Результат`|`Результат`|`Результат`|`Результат`|
|*Вариант 1*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: неверное изображение товаров, товары "Sauce Labs Bolt T-Shirt", "Sauce Labs Fleece Jacket", "Test.allTheThings() T-Shirt (Red)" не добавляются в корзину`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 2*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: открывается страница с описанием не того товара, который выбран`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 3*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: открывается страница с описанием не того товара, который выбран`|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №6. Переход в корзину

<font color=black size=1> 

|Вариант №|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|:-:|
| |`Результат`|`Результат`|`Результат`|`Результат`|
|*Вариант 1*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 2*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 3*|<font color=limegreen size=3>`пройден`|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: после нажатия на название товара "Sauce Labs Fleece Jacket" или его изображение (что тоже неправильное) открывается страница с описанием товара "ITEM NOT FOUND", где после добавления этого товара в корзину нажатием на кнопку "Add to cart" и нажатия на кнопку 🛒 не происходит переход в корзину, а появляется пустая белая страница`|<font color=limegreen size=3>`пройден`|
</font>

#### Тест-кейс №7. Удаление товаров из корзины

<font color=black size=1> 

|Вариант №|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|:-:|
| |`Результат`|`Результат`|`Результат`|`Результат`|
|*Вариант 1*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: не удаляются добавленные товары`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 2*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: не удаляются добавленные товары`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 3*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: не удаляются добавленные товары`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 4*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=orange size=3>`частично пройден`</font><br>`товары "Sauce Labs Bolt T-Shirt", "Sauce Labs Fleece Jacket", "Test.allTheThings() T-Shirt (Red)" не добавляются в корзину`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 5*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=orange size=3>`частично пройден`</font><br>`товары "Sauce Labs Bolt T-Shirt", "Sauce Labs Fleece Jacket", "Test.allTheThings() T-Shirt (Red)" не добавляются в корзину`|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №8. Выхода из корзины

<font color=black size=1> 

|Вариант №|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|:-:|
| |`Результат`|`Результат`|`Результат`|`Результат`|
|*Вариант 1*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 2*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 3*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=orange size=3>`частично пройден`</font><br>`товары "Sauce Labs Bolt T-Shirt", "Sauce Labs Fleece Jacket", "Test.allTheThings() T-Shirt (Red)" не добавляются в корзину`|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №9. Открытие бокового меню

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №10. Закрытие бокового меню

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №11. Пункт бокового меню <u>All Items</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font><br>`Неожиданное поведение приложения: наблюдается задержка в переходе на главную страницу интернет-магазина`|
</font>

#### Тест-кейс №12. Пункт бокового меню <u>About</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: вместо информации об интернет-магазине открывается сторонний сайт https://saucelabs.com`|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: открывается страница 404 https://saucelabs.com/error/404`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: вместо информации об интернет-магазине открывается сторонний сайт https://saucelabs.com`|
</font>

#### Тест-кейс №13. Пункт бокового меню <u>Logout</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №14. Пункт бокового меню <u>Reset App State</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №15. Ссылка на <u>twitter</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №16. Ссылка на <u>facebook</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №17. Cсылка на <u>linkedin</u>

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №18. Проверка сортировки товаров

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: не меняется вид сортировки`|<font color=limegreen size=3>`пройден`</font><br>`Неожиданное поведение приложения: наблюдается задержка после выбора вида сортировки`|
</font>

#### Тест-кейс №19. Открытие страницы с описанием товара

<font color=black size=1> 

|Вариант №|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|:-:|
||`Результат`|`Результат`|`Результат`|`Результат`|
|*Вариант 1*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: открывается описание не того товара, что выбран`|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 2*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Неожиданное поведение приложения: открывается описание не того товара, что выбран`|<font color=limegreen size=3>`пройден`</font>|
</font>

#### Тест-кейс №20. Выход со страницы с описанием товара

<font color=black size=1> 

|Вариант №|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|:-:|
||`Результат`|`Результат`|`Результат`|`Результат`|
|*Вариант 1*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 2*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font>|
|*Вариант 3*|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=limegreen size=3>`пройден`</font>|<font color=limegreen size=3>`пройден`</font><br>`Неожиданное поведение приложения: наблюдается задержка в переходе на главную страницу интернет-магазина после нажатия на кнопку "All Items" в боковом меню`|
</font>

#### Тест-кейс №21. Оформление заказа

<font color=black size=1> 

|standard_user|locked_out_user|problem_user|performance_glitch_user| 
|:-:|:-:|:-:|:-:|
|`Результат`|`Результат`|`Результат`|`Результат`|
|<font color=limegreen size=3>`пройден`</font>|<font color=red size=3>`провален`</font><br>`Авторизация не пройдена, пользователь заблокирован`|<font color=red size=3>`провален`</font><br>`Критическое поведение приложения: в поле "Last Name" невозможно ввести данные, дальнейшее оформление заказа невозможно`|<font color=limegreen size=3>`пройден`</font><br>`Неожиданное поведение приложения: наблюдается задержка в переходе на главную страницу интернет-магазина после нажатия на кнопку "Back Home" на странице с информацией об успешном оформлении заказа`|
</font>