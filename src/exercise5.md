##### Задание №5. 

![PowerShell](https://img.icons8.com/color/480w/powershell.png)

# PowerShell



#### Что такое PowerShell?

***PowerShell*** — это кроссплатформенное решение для автоматизации задач, которое включает оболочку командной строки, скриптовый язык и платформу управления конфигурацией. PowerShell поддерживается в Windows, Linux и macOS.


#### Какие возможности имеет PowerShell?

1. Менять настройки операционной системы;

2. Управлять службами и процессами;

3. Настраивать роли и компоненты сервера;

4. Устанавливать программное обеспечение;

5. Управлять установленным ПО через специальные интерфейсы;

6. Встраивать исполняемые компоненты в сторонние программы;

7. Создавать сценарии для автоматизации задач администрирования;

8. Работать с файловой системой, реестром Windows, хранилищем сертификатов и т.д.



#### Как открыть журнал событий в PowerShell?

Журнал событий Windows PowerShell можно просмотреть в ***Просмотр событий*** или с помощью ***Get-EventLog*** командлетов и ***Get-WmiObject*** .


#### Чем cmd отличается от PowerShell?

Ключевым отличием от CMD, заметным на старте работы, являются командлеты — упрощенные команды, используемые в среде PowerShell. Назначение команды PowerShell довольно легко интерпретировать по названию: они следуют простой закономерности — за глаголом идет существительное.
В один ряд с терминалом Линукс по своей многозадачности PowerShell ставить нельзя: мелко плавает. Но по сравнению с cmd она может гораздо больше, и это на фоне того факта, что практически всё, что может cmd, прокатит и в PowerShell. Однако для работы с shell придётся использовать уже отдельный вид команд, которые, дабы на русском не звучало косноязычно, переводчики назвали «командлетами». В отличие от cmd, в shell команды исполняются по нескольким каналам. Это значит, что выход одной команды (в смысле, командлета) может быть одновременно входом в другую. И всё потому, что командлеты  PowerShell — это вполне себе определённые объекты, представители конкретной структуры данных. Даже те командлеты, которые встречают в ответе shell на запрос пользователя. Выражаясь языком программистов, PSH — объектно-ориентированный, а cmd обрабатывает только символы или последовательность символов. Проще говоря, PowerShell позволяет работать с некоторыми программами изнутри, в режиме реального времени, интерактивно. Cmd, в сущности, может только запускать утилиты, которые в Windows уже существуют (почти все они в папке C:\Windows).
Более того, PowerShell — это вполне себе законченная среда для написания и исполнения скрипта. Так что можно создавать очень сложные и объёмные скрипты для управления системой, чем те, на какие была способна консоль cmd.

Основная разница между PowerShell и cmd в том, что последняя — это обновлённая версия «отжившей» в своё время программной оболочки DOS, а в первую, как видно, Windows вдыхает новую жизнь. Очевидно демонстрируя, что от DOS команд разработчики отказываться вообще не собираются. Сравнение с DOS уже неверно, та очень ограничена в своих возможностях; cmd существовала в Windows как «наследие DOS для избранных» или ремонтный, прямой вариант самых необходимых команд. А ввод в работу PowerShell — это как своеобразное предложение, если не покопаться во внутренностях системы, то поучаствовать в изучении её возможностей и способ заняться её модификацией вполне официально: интеграция в среду .Net тому подтверждение.

|  PowerShell	                       |     Командная строка CMD            | 
|:------------------------------------:|:-----------------------------------:|
| Введен в 2006 г.                     |  Введен в 1981 г.                   |
| Работает как с пакетными командами, так и с командами PowerShell| Работает только с пакетными командами|
| Позволяет создавать псевдонимы для команд или сценариев| Не поддерживает создание псевдонимов команд|
| Позволяет передавать вывод команды другим командам.| не позволяет передавать вывод команды другим командам.|
| Вывод осуществляется в виде объекта| Вывод — просто текст|
| Можно выполнять последовательность команд в рамках сценария| Требуется, чтобы одна команда завершилась раньше другой|
| Имеет библиотеки для программирования, так как построен на .net framework.| Отсутствие библиотек программирования|
| Бесшовная интеграция с WMI |Требуется внешний плагин для взаимодействия с WMI|
|Поддерживает системы Linux | Не поддерживает системы Linux |
|Выполняет все типы программ | Запускает только программы консольного типа |




#### Какой командой в PowerShell можно просмотреть список доступных журналов событий? (Запустите эту команду в PowerShell и сделайте скрин, который назовите exercise5.1.png.)

Чтобы просмотреть все классические журналы событий, необходимо ввести: ***Get-EventLog -List***



#### Какой командой можно узнать текущую версию PowerShell? (Запустите эту команду в PowerShell и сделайте скрин, который назовите exercise5.2.png.)

Самый простой способ определить какая версия PowerShell у вас установлена с помощью команды: ***Get-host*** или ***$PSVersionTable***


#### Создайте файл ps.txt (файл должен быть именно в формате .txt) в C:\Users\<ваш логин в системе> с содержимым: This is PS file. Запустите команду из PowerShell для чтения содержимого этого файла. Сделайте скрин запуска команды, который назовите exercise5.3.png.

***Get-Content -Path .\ps.txt*** - команда для чтения содержимого из файла px.txt в директории C:\Users\edij 
