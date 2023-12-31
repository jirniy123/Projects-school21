<font size=2> 

<font color=limegreen>  

### Авторизация </font>

#### Тест-кейс №1. Авторизация для *"standard_user"*  

1. Предшествующие условия:
	- открыть страницу авторизации <https://www.saucedemo.com>
2. Шаги:
	- нажать на область <u>Username</u>
	- набрать логин *"standard_user"*
	- нажать на область <u>Password</u>
	- набрать пароль  *"secret_sauce"*
	- нажать на кнопку <u>Login</u>
2. Ожидаемый результат:
	- после нажатия на область <u>Username</u> можно вводить данные
	- после нажатия на область <u>Password</u> можно вводить данные
	- после ввода данных и нажатия на кнопку <u>Login</u> открывается интернет-магазин

#### Тест-кейс №2. Авторизация для *"locked_out_user"*  

1. Предшествующие условия:
	- открыть страницу авторизации <https://www.saucedemo.com>
2. Шаги:
	- нажать на область <u>Username</u>
	- набрать логин *"locked_out_user"* 
	- нажать на область <u>Password</u>
	- набрать пароль  *"secret_sauce"*
	- нажать на кнопку <u>Login</u>
2. Ожидаемый результат:
	- после нажатия на область <u>Username</u> можно вводить данные
	- после нажатия на область <u>Password</u> можно вводить данные
	- после ввода данных и нажатия на кнопку <u>Login</u> открывается интернет-магазин

#### Тест-кейс №3. Авторизация для *"problem_user"*  

1. Предшествующие условия:
	- открыть страницу авторизации <https://www.saucedemo.com>
2. Шаги:
	- нажать на область <u>Username</u>
	- набрать логин *"problem_user"*
	- нажать на область <u>Password</u>
	- набрать пароль  *"secret_sauce"*
	- нажать на кнопку <u>Login</u>
2. Ожидаемый результат:
	- после нажатия на область <u>Username</u> можно вводить данные
	- после нажатия на область <u>Password</u> можно вводить данные
	- после ввода данных и нажатия на кнопку <u>Login</u> открывается интернет-магазин

#### Тест-кейс №4. Авторизация для *"performance_glitch_user"* 

1. Предшествующие условия:
	- открыть страницу авторизации <https://www.saucedemo.com>
2. Шаги:
	- нажать на область <u>Username</u>
	- набрать логин *"performance_glitch_user"*
	- нажать на область <u>Password</u>
	- набрать пароль  *"secret_sauce"*
	- нажать на кнопку <u>Login</u>
2. Ожидаемый результат:
	- после нажатия на область <u>Username</u> можно вводить данные
	- после нажатия на область <u>Password</u> можно вводить данные
	- после ввода данных и нажатия на кнопку <u>Login</u> открывается интернет-магазин

<font color=limegreen>  

### Работа с корзиной</font>

#### Тест-кейс №5. Добавление товара в корзину

<font size=1> 

         *Вариант 1:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на кнопку <u>Add to cart</u> интересующего товара
2. Ожидаемый результат:
	- после нажатия на кнопку <u>Add to cart</u> товар добавился в корзину

<font size=1> 

         *Вариант 2:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на изображение интересующего товара
	- нажать на кнопку <u>Add to cart</u>
2. Ожидаемый результат:
	- после нажатия на изображение товара открывается страница описания товара
	- после нажатия на кнопку <u>Add to cart</u> товар добавился в корзину

<font size=1> 

         *Вариант 3:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на название интересующего товара
	- нажать на кнопку <u>Add to cart</u>
2. Ожидаемый результат:
	- после нажатия на название товара открывается страница описания товара
	- после нажатия на кнопку <u>Add to cart</u> товар добавился в корзину

#### Тест-кейс №6. Переход в корзину

<font size=1> 

         *Вариант 1:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на кнопку 🛒 в правом верхнем углу
2. Ожидаемый результат:
	- после нажатия на кнопку 🛒 открывается страница корзины

<font size=1> 

         *Вариант 2:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыта страница оформления заказа нажатием кнопки <u>Checkout</u> на странице корзины
2. Шаги:
	- нажать на кнопку <u>Cancel</u>
2. Ожидаемый результат:
	- после нажатия на кнопку <u>Cancel</u> происходит возврат в корзину

<font size=1> 

         *Вариант 3:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто окно описания товара
	- товар добавлен в корзину нажатием на кнопку <u>Add to cart</u>
2. Шаги:
	- нажать на кнопку 🛒 в правом верхнем углу
2. Ожидаемый результат:
	- после нажатия на кнопку <u>Cancel</u> происходит возврат в корзину

#### Тест-кейс №7. Удаление товаров из корзины

<font size=1> 

         *Вариант 1:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- интересующий товар добавлен в корзину нажатием кнопки <u>Add to cart</u> на главной странице интернет-магазина
2. Шаги:
	- нажать на кнопку <u>Remove</u> добавленного товара
2. Ожидаемый результат:
	- после нажатия на кнопку <u>Remove</u> товар удаляется из корзины

<font size=1> 

         *Вариант 2:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто описание товара нажатием на изображение интересующего товара
	- товар добавлен в корзину нажатием кнопки <u>Add to cart</u> на странице описания товара
2. Шаги:
	- нажать на кнопку <u>Remove</u> добавленного товара
2. Ожидаемый результат:
	- после нажатия на кнопку <u>Remove</u> товар удаляется из корзины

<font size=1> 

         *Вариант 3:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто описание товара нажатием на название интересующего товара
	- товар добавлен в корзину нажатием кнопки <u>Add to cart</u> на странице описания товара
2. Шаги:
	- нажать на кнопку <u>Remove</u> добавленного товара
2. Ожидаемый результат:
	- после нажатия на кнопку <u>Remove</u> товар удаляется из корзины

<font size=1> 

         *Вариант 4:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- интересующий товар добавлен в корзину шагами из любого варианта Тест-кейса №5
2. Шаги:
	- нажать на кнопку 🛒 в правом верхнем углу
	- нажать на кнопку <u>Remove</u> товара, который нужно удалить
2. Ожидаемый результат:
	- после нажатия на кнопку 🛒 открывается страница корзины
	- после нажатия на кнопку <u>Remove</u> товара, который нужно удалить, он удаляется из корзины

<font size=1> 

         *Вариант 5:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- интересующий товар добавлен в корзину шагами из любого варианта Тест-кейса №5
2. Шаги:
	- нажать на кнопку "≡" в левом верхнем углу
	- в появившемся меню нажать на кнопку <u>Reset App State</u>
2. Ожидаемый результат:
	- после нажатия на кнопку "≡" открывается боковое меню
	- после нажатия на кнопку <u>Reset App State</u> в открывшемся боковом меню все товары из корзины удаляются

#### Тест-кейс №8. Выхода из корзины

<font size=1> 

         *Вариант 1:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыта страница корзины нажатием на кнопку 🛒 в правом верхнем углу
2. Шаги:
	- нажать на кнопку <u>Continue Shopping</u>
2. Ожидаемый результат:
	- происходит переход со страницы корзины на страницу оформления покупок

<font size=1> 

         *Вариант 2:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыта страница корзины нажатием на кнопку 🛒 в правом верхнем углу
2. Шаги:
	- нажать на кнопку "≡" в левом верхнем углу
	- в появившемся меню нажать на кнопку <u>All Items</u>
2. Ожидаемый результат:
	- после нажатия на кнопку "≡" открывается боковое меню
	- после нажатия на кнопку <u>All Items</u> происходит переход из корзины на главную страницу интернет-магазина

<font size=1> 

         *Вариант 3:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- интересующий товар добавлен в корзину шагами из любого варианта Тест-кейса №5
	- открыта страница корзины нажатием на кнопку 🛒 в правом верхнем углу
2. Шаги:
	- нажать на название добавленного товара
	- нажать на кнопку <u>Back to products</u> под кнопкой "≡"
2. Ожидаемый результат:
	- после нажатия на название товара открывается страница описания товара
	- после нажатия на кнопку <u>Back to products</u> на странице описания товара происходит переход на главную страницу интернет-магазина

<font color=limegreen> 

### Боковое меню</font>

#### Тест-кейс №9. Открытие бокового меню

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на кнопку "≡" в левой верхней части страницы
2. Ожидаемый результат:
	- появляется боковое меню

#### Тест-кейс №10. Закрытие бокового меню

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто боковое меню нажатием на кнопку "≡" в левой верхней части страницы
2. Шаги:
	- нажать на кнопку "Х" в правом верхнем углу бокового меню
2. Ожидаемый результат:
	- боковое меню закрывается

#### Тест-кейс №11. Пункт бокового меню <u>All Items</u>

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто боковое меню нажатием на кнопку "≡" в левой верхней части страницы
2. Шаги:
	- нажать на кнопку <u>All Items</u>
2. Ожидаемый результат:
	- открывается главная страница интернет-магазина с выбором товаров

#### Тест-кейс №12. Пункт бокового меню <u>About</u>

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто боковое меню нажатием на кнопку "≡" в левой верхней части страницы
2. Шаги:
	- нажать на кнопку <u>About</u>
2. Ожидаемый результат:
	- открывается страница с информацией об интернет-магазине

#### Тест-кейс №13. Пункт бокового меню <u>Logout</u>

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто боковое меню нажатием на кнопку "≡" в левой верхней части страницы
2. Шаги:
	- нажать на кнопку <u>Logout</u>
2. Ожидаемый результат:
	- происходит выход из учетной записи интернет-магазина

#### Тест-кейс №14. Пункт бокового меню <u>Reset App State</u>

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- открыто боковое меню нажатием на кнопку "≡" в левой верхней части страницы
2. Шаги:
	- нажать на кнопку <u>Reset App State</u>
2. Ожидаемый результат:
	- происходит сброс состояния приложения

<font color=limegreen> 

### Ссылки в нижней части страницы (footer)</font>

#### Тест-кейс №15. Ссылка на <u>twitter</u> 

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на логотип <u>twitter</u> внизу страницы
2. Ожидаемый результат:
	- происходит переход на страницу социальной сети Twitter

#### Тест-кейс №16. Ссылка на <u>facebook</u>

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на логотип <u>facebook</u> внизу страницы
2. Ожидаемый результат:
	- происходит переход на страницу социальной сети Facebook

#### Тест-кейс №17. Cсылка на <u>linkedin</u>

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на логотип <u>linkedin</u> внизу страницы
2. Ожидаемый результат:
	- происходит переход на страницу социальной сети Linkedin

<font color=limegreen> 

### Сортировка товаров</font>

#### Тест-кейс №18. Проверка сортировки товаров

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать под кнопкой 🛒 на область выбора сортировки
	- выбрать один из видов сортировки:
		- <u>Name (A to Z)</u>
		- <u>Name (Z to A)</u>
		- <u>Price (low to high)</u>
		- <u>Price (high to low)</u>
2. Ожидаемый результат:
	- при выборе сортировки <u>Name (A to Z)</u> происходит сортировка товаров в алфавитном порядке
	- при выборе сортировки <u>Name (Z to A)</u> происходит сортировка товаров в обратном алфавитном порядке
	- при выборе сортировки <u>Price (low to high)</u> происходит сортировка товаров по возрастанию стоимости товаров
	- при выборе сортировки <u>Price (high to low)</u> происходит сортировка товаров по убыванию стоимости товаров

<font color=limegreen> 

### Просмотр товаров</font>

#### Тест-кейс №19. Открытие страницы с описанием товара

<font size=1> 

         *Вариант 1:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на название интересующего товара
2. Ожидаемый результат:
	- происходит переход на страницу с описанием выбранного товара

<font size=1> 

         *Вариант 2:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
2. Шаги:
	- нажать на изображение интересующего товара
2. Ожидаемый результат:
	- происходит переход на страницу с описанием выбранного товара

#### Тест-кейс №20. Выход со страницы с описанием товара

<font size=1> 

         *Вариант 1:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- выполнены шаги из любого варианта Тест-кейса №19
2. Шаги:
	- нажать на кнопку <u>Back to products</u>
2. Ожидаемый результат:
	- происходит переход со страницы с описанием товара на главную страницу интернет-магазина

<font size=1> 

         *Вариант 2:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- выполнены шаги из любого варианта Тест-кейса №19
2. Шаги:
	- нажать на кнопку 🛒
2. Ожидаемый результат:
	- происходит переход со страницы с описанием товара на страницу корзины

<font size=1> 

         *Вариант 3:*</font>
1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- выполнены шаги из любого варианта Тест-кейса №19
2. Шаги:
	- нажать на кнопку "≡" в левой верхней части страницы
	- в появившемся боковом меню нажать на кнопку <u>All Items</u>
2. Ожидаемый результат:
	- после нажатия на кнопку "≡" открывается боковое меню
	- после нажатия на кнопку <u>All Items</u> происходит переход со страницы с описанием товара на главную страницу интернет-магазина

<font color=limegreen> 

### Оформление заказов</font>

#### Тест-кейс №21. Оформление заказа

1. Предшествующие условия:
	- успешно пройдена авторизация на странице <https://www.saucedemo.com>
	- интересующий товар добавлен в корзину шагами из любого варианта Тест-кейса №5
2. Шаги:
	- нажать на кнопку 🛒
	- нажать на кнопку <u>Checkout</u>
	- заполнить поля:
		- <u>First Name</u>
		- <u>Last Name</u>
		- <u>Zip/Postal Code</u>
	- нажать на кнопку <u>Continue</u>
	- нажать на кнопку <u>Finish</u>
	- нажать на кнопку <u>Back Home</u>
2. Ожидаемый результат:
	- после нажатия на кнопку 🛒 открывается страница корзины
	- после нажатия на кнопку <u>Checkout</u> происходит переход со страницы корзины на страницу оформления заказа
		- после нажатия на область <u>First Name</u> можно вводить данные
		- после нажатия на оласть <u>Last Name</u> можно вводить данные
		- после нажатия на область <u>Zip/Postal Code</u> можно вводить данные
	- после ввода данных и нажатия на кнопку <u>Continue</u> открывается страница подтверждения заказа
	- после подтверждения заказа нажатием на кнопку <u>Finish</u> происходит переход на страницу с информацией об успешном оформлении заказа
	- после нажатия на кнопку <u>Back Home</u> происходит переход на главную страницу интернет-магазина