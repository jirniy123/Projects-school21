<font size=1>

### Значения полей ввода данных на странице авторизации [интернет-магазина](https://www.saucedemo.com/ "www.saucedemo.com"), которые они могут принимать:

##### Поле **`Username`**:

- пустое
- верное значение:
	- standard_user
	- locked_out_user
	- problem_user
	- performance_glitch_user
- неверное значение

##### Поле **`Password`**:

- пустое
- верное значение
	- secret_sauce
- неверное значение

### Попарное тестирование для полей **`Username`** и **`Password`**

#### Тест-кейс №1. Поля: `Username` - пустое, `Password` - пустое

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- поле `Username` оставить пустым
	- поле `Password` оставить пустым
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username is required` - требуется имя пользователя

#### Тест-кейс №2. Поля: `Username` - пустое, `Password` - верное значение "secret_sauce"

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- поле `Username` оставить пустым
	- в поле `Password` ввести "secret_sauce"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username is required` - требуется имя пользователя

#### Тест-кейс №3. Поля: `Username` - пустое, `Password` - неверное значение

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- поле `Username` оставить пустым
	- в поле `Password` ввести "qwerty"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username is required` - требуется имя пользователя

#### Тест-кейс №4. Поля: `Username` - верное значение "standard_user", `Password` - пустое

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "standard_user"
	- поле `Password` оставить пустым
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Password is required` - требуется пароль

#### Тест-кейс №5. Поля: `Username` - верное значение "standard_user", `Password` - верное значение "secret_sauce"

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "standard_user"
	- в поле `Password` ввести "secret_sauce"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация пройдена
	- открыта главная страница интернет-магазина с товарами

#### Тест-кейс №6. Поля: `Username` - верное значение "standard_user", `Password` - неверное значение

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "standard_user"
	- в поле `Password` ввести "qwerty"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username and password do not match any user in this service` - имя пользователя и пароль не совпадают ни с одним пользователем в этом сервисе

#### Тест-кейс №7. Поля: `Username` - верное значение "problem_user", `Password` - пустое

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "problem_user"
	- поле `Password` оставить пустым
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Password is required` - требуется пароль

#### Тест-кейс №8. Поля: `Username` - верное значение "problem_user", `Password` - верное значение "secret_sauce"

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "problem_user"
	- в поле `Password` ввести "secret_sauce"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация пройдена
	- открыта главная страница интернет-магазина с товарами

#### Тест-кейс №9. Поля: `Username` - верное значение "problem_user", `Password` - неверное значение

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "problem_user"
	- в поле `Password` ввести "qwerty"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username and password do not match any user in this service` - имя пользователя и пароль не совпадают ни с одним пользователем в этом сервисе

#### Тест-кейс №10. Поля: `Username` - верное значение "performance_glitch_user", `Password` - пустое

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "performance_glitch_user"
	- поле `Password` оставить пустым
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Password is required` - требуется пароль

#### Тест-кейс №11. Поля: `Username` - верное значение "performance_glitch_user", `Password` - верное значение "secret_sauce"

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "performance_glitch_user"
	- в поле `Password` ввести "secret_sauce"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация пройдена
	- открыта главная страница интернет-магазина с товарами

#### Тест-кейс №12. Поля: `Username` - верное значение "performance_glitch_user", `Password` - неверное значение

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "performance_glitch_user"
	- в поле `Password` ввести "qwerty"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username and password do not match any user in this service` - имя пользователя и пароль не совпадают ни с одним пользователем в этом сервисе

#### Тест-кейс №13. Поля: `Username` - верное значение "locked_out_user", `Password` - пустое

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "locked_out_user"
	- поле `Password` оставить пустым
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Password is required` - требуется пароль

#### Тест-кейс №14. Поля: `Username` - верное значение "locked_out_user", `Password` - верное значение "secret_sauce"

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "locked_out_user"
	- в поле `Password` ввести "secret_sauce"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Sorry, this user has been locked out.` - извините, этот пользователь был заблокирован

#### Тест-кейс №15. Поля: `Username` - верное значение "locked_out_user", `Password` - неверное значение

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "locked_out_user"
	- в поле `Password` ввести "qwerty"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username and password do not match any user in this service` - имя пользователя и пароль не совпадают ни с одним пользователем в этом сервисе

#### Тест-кейс №16. Поля: `Username` - неверное значение, `Password` - пустое

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "secret_user"
	- поле `Password` оставить пустым
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Password is required` - требуется пароль

#### Тест-кейс №17. Поля: `Username` - неверное значение, `Password` - верное значение "secret_sauce"

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- в поле `Username` ввести "secret_user"
	- в поле `Password` ввести "secret_sauce"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username and password do not match any user in this service` - имя пользователя и пароль не совпадают ни с одним пользователем в этом сервисе

#### Тест-кейс №18. Поля: `Username` - неверное значение, `Password` - неверное значение

1. Предшествующие условия:
	- открыта страница авторизации <https://www.saucedemo.com>
2. Шаги:
	- поле `Username` оставить пустым
	- в поле `Password` ввести "qwerty"
	- нажать на кнопку **`Login`**
2. Ожидаемый результат:
	- авторизация не проходит
	- отображается ошибка: `Epic sadface: Username and password do not match any user in this service` - имя пользователя и пароль не совпадают ни с одним пользователем в этом сервисе