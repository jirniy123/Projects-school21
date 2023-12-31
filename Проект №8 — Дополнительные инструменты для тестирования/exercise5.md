## **Что такое PowerShell?**

**PowerShell** — это кроссплатформенное решение для автоматизации задач, которое включает оболочку командной строки, скриптовый язык и платформу управления конфигурацией. PowerShell поддерживается в Windows, Linux и macOS.
В отличие от принимающих и возвращающих текстовые данные оболочек, Windows PowerShell работает с классами .NET, у которых есть свойства и методы. PowerShell позволяет выполнять обычные команды, а также дает доступ к объектам COM, WMI и ADSI. В ней используются различные хранилища, вроде файловой системы или реестра Windows, для доступа к которым созданы т.н. поставщики (providers). Стоит отметить возможность встраивания исполняемых компонентов PowerShell в другие приложения для реализации различных операций, в т.ч. через графический интерфейс. Верно и обратное: многие приложения для Windows предоставляют доступ к своим интерфейсам управления через PowerShell.

## **Какие возможности имеет PowerShell?**

**PowerShell позволяет:**

- Менять настройки операционной системы;
- Управлять службами и процессами;
- Настраивать роли и компоненты сервера;
- Устанавливать программное обеспечение;
- Управлять установленным ПО через специальные интерфейсы;
- Встраивать исполняемые компоненты в сторонние программы;
- Создавать сценарии для автоматизации задач администрирования;
- Работать с файловой системой, реестром Windows, хранилищем сертификатов и т.д.

## **Как открыть журнал событий в PowerShell?**

**Способ 1. С помощью кнопки Пуск**
- Нажать ПКМ на кнопку *Пуск* (на панели задач) с логотипом Windows.
- Откроется контекстное меню кнопки *Пуск*
- Нажать в списке на приложение *Windows PowerShell* или *Windows PowerShell (администратор)* - режим с максимальными правами в Windows 10.

**Способ 2. С помощью кнопки или строки поиска на панели задач**
- Нажать на кнопку поиска
- Начать набирать текст *PowerShell*
- Если щелкнуть по ней правой кнопкой мыши, то можно открыть ее от имени администратора.

**Способ 3. С помощью меню Пуск**
- Нажать на кнопку *Пуск* с логотипом Windows
- Найти пункт *Windows PowerShell*, он будет в виде папки, открыть его и запустить соответствующую версию.
- Если кликнуть ПКМ, то возможно запускать оболочку от имени и с правами администратора.

**Способ 4. Через окно "Выполнить"**
- Вызвать окно «Выполнить», нажав на клавиатуре клавиши `WIN+R`.
- Ввести команду `powershell` и нажать `ENTER` или `ОК`.

**Способ 5. Через проводник**
- Открыть приложение *Проводник* (Explorer) или просто щелкнуть по ярлыку *Мой компьютер* на рабочем столе
- Выбрать пункт меню *Файл - запустить Windows PowerShell*.


## **Чем cmd отличается от PowerShell?**

Главное отличие между `PowerShell` и `CMD` является то, что `PowerShell` – это мощный интерфейс командной строки и среда сценариев, которая позволяет выполнять сложные сценарии для простого и эффективного выполнения задач администрирования системы Windows, а `CMD` – интерфейс командной строки, который предоставляет пользователю набор команд для взаимодействия с компьютером для выполнения задач.

**Команды.** Разница между `PowerShell` и `CMD` заключается в том, что `PowerShell` может интерпретировать как пакетные команды, так и команды `PowerShell`, тогда как `CMD` может интерпретировать только пакетные команды.

**Функциональность.** Кроме того, еще одно различие между `PowerShell` и `CMD` заключается в том, что `PowerShell` в основном используется системными администраторами для выполнения административных задач, тогда как `CMD` взаимодействует с пользовательскими программами и выполняет задачи в соответствии с выданными пользователем командами. 

**Сложность** Более того, `PowerShell` более сложный и мощный, чем `CMD`. 

**Характеристики.** Кроме того, `PowerShell` имеет дополнительные функции и улучшения, чем `CMD`.

## **Какой командой в PowerShell можно просмотреть список доступных журналов событий?** 
```
Get-EventLog -List
```

## **Какой командой можно узнать текущую версию PowerShell?**
```
$PSVersionTable
```