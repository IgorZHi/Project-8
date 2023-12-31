
![doker](https://blog.skillfactory.ru/wp-content/uploads/2023/02/vertical-logo-monochromatic-2822952.png.webp)


# Задание №7. Docker и Kubernetes

## Что такое Docker? Для чего он используется?

***Docker*** — это программная платформа для разработки, доставки и запуска контейнерных приложений. Он позволяет создавать контейнеры, автоматизировать их запуск и развертывание, управляет жизненным циклом. С помощью Docker можно запускать множество контейнеров на одной хост-машине.

***Docker*** — клиент-серверное приложение. Это означает, что оно состоит из двух частей: сервера и клиента.

Сервер еще называют Docker-движком или демоном (daemon). Это фоновый процесс, который непосредственно управляет контейнерами. Именно демон создает, разворачивает и запускает контейнеры. Его можно сравнить с двигателем машины.

Клиент — это программа-интерфейс для командной строки, с которой взаимодействует пользователь. Он отдает команды через терминал. Клиент сообщает нужные сведения демону и отдает ему указания. Если продолжать аналогию с машиной, клиент — это руль и педали.

Клиент и сервер могут находиться на одном устройстве, а могут — на разных. Во втором случае клиент подключают к удаленному серверу через сокеты или API. 


## Чем Docker отличается от виртуальной машины?

| Виртуальная машина                                   | Docker контейнер                                          |
|------------------------------------------------------|-----------------------------------------------------------|
| Изоляция процесса на аппаратном уровне               | Изоляция процесса на уровне ОС                            |
| Каждая виртуальная машина имеет отдельную ОС         | Каждый контейнер может совместно использовать ОС          |
| Загружается в считанные минуты                       | Загружается в считанные секунды                           |
| Виртуальные машины занимают несколько ГБ             | Контейнеры легкие (КБ / МБ)                               |
| Готовые виртуальные машины трудно найти              | Готовые док-контейнеры легко доступны                     |
| Виртуальные машины могут легко перейти на новый хост | Контейнеры уничтожаются и воссоздаются, а не перемещаются |
| Создание ВМ занимает относительно больше времени     | Контейнеры могут быть созданы в считанные секунды         |
| Больше использования ресурса                         | Меньшее использование ресурсов                            |


## Что такое Docker Compose?

***Docker Compose*** — это инструментальное средство, входящее в состав Docker. Оно предназначено для решения задач, связанных с развёртыванием проектов.

***Docker Compose*** позволяет управлять набором контейнеров, каждый из которых представляет собой один сервис проекта. Управление включает в себя сборку, запуск с учетом зависимостей и конфигурацию. Конфигурация Docker Compose описывается в файле docker-compose.yml, лежащем в корне проекта.

## Что такое Kubernetes? Для чего он используется?

***Kubernetes*** — это платформа с открытым исходным кодом, которая автоматизирует операции с контейнерами. Она упрощает многие ручные процессы, связанные с развертыванием и масштабированием упакованных в контейнеры приложений. Таким образом, можно объединять группы хостов, работающих под управлением контейнеров Linux, и Kubernetes поможет эффективно управлять этими кластерами, которые могут охватывать узлы в общедоступных, частных или гибридных облаках. Поэтому Kubernetes является идеальной платформой для размещения облачных приложений, требующих быстрого масштабирования.

***Kubernetes*** планирует и автоматизирует эти и другие задачи, связанные с контейнерами:

Развертывание: разверните указанное количество контейнеров на указанном хосте и поддерживайте их работу в желаемом состоянии.

Внедрение: внедрение — это изменение развертывания. Kubernetes позволяет запускать, приостанавливать, возобновлять или откатывать развертывание.

Обнаружение службы: ***Kubernetes*** может автоматически открывать контейнер для Интернета или других контейнеров, используя DNS-имя или IP-адрес.

Предоставление хранилища: настройте ***Kubernetes*** для подключения постоянного локального или облачного хранилища для ваших контейнеров по мере необходимости.

Балансировка и масштабирование нагрузки: когда трафик к контейнеру резко возрастает, Kubernetes может использовать балансировку и масштабирование нагрузки, чтобы распределить его по сети для поддержания стабильности.

Самовосстановление для обеспечения высокой доступности: при сбое контейнера Kubernetes может перезапустить или заменить его автоматически; он также может разбирать контейнеры, которые не соответствуют вашим требованиям к проверке здоровья.

