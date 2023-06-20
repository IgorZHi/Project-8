#### Задание №2.  

## Поиск ошибок, проблем , багов интерфейса , багов в логике работы приложения - при помощи вкладки "Console" (Консоль) в DevTools браузера Firefox на официальном сайте веб-приложения СберМегаМаркета .

https://www.mozilla.org/ru/firefox/new/

https://sbermegamarket.ru/


# Баг-репорты

## Баг №1 Ошибка 400 * (Bad Request - Плохой запрос)POST https://sbermegamarket.ru/api/fl?u=6efd37c0-6ff6-11ed-a2cf-b37c7b2b7873&cfidsw-smm=qRNQZvVQSjyXNsxdUNaeRaG1R9VUM3r0CUDznB52UW6pz9mlFKA6CwPxO64Mam4E05wriPH6nFD84uY2FKYEFlK2BRwfYsuMYREq8xqENnwXgfwdX%2BZ38mN53RwpS5%2FhhC9xjg%2FcrNGLqlK6DpJMUVZTQNOPapDsXyIK

- #### Предшествующие условия:

1. Открыт браузер Firefox

2. Открыта страница https://sbermegamarket.ru/

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:

1. нажать F12
2. открыть вкладку "Console" (Консоль) в DevTools
3. нажать кнопку ошибки , если горит красный кружок с восклицательным знаком.

- ##### Ожидаемый результат.

- Веб-приложение работает без ошибок


- ##### Фактический результат:

- в консоли зафиксирована следующая ошибка:
POST Ответ сервера с кодом ошибки 400 * (Bad Request - Плохой запрос)

 - ##### Окружение:

ПК desktop/ Windows 11 Pro.Версия 21H2


## Баг №2 Код ошибки: SEC_ERROR_UNKNOWN_ISSUER  Вероятная угроза безопасности.

- ##### Предшествующие условия:

1. Открыт браузер Firefox

2. Открыта страница https://sbermegamarket.ru/

- ##### Серьёзность:

Minor

- ##### Шаги для воспроизведения:

1. нажать F12
2. открыть вкладку "Console" (Консоль) в DevTools
3. нажать кнопку ошибки , если горит красный кружок с восклицательным знаком.

- ##### Ожидаемый результат:

- Веб-приложение работает без ошибок

- ##### Фактический результат:

В консоле красными буквами надпись : Запрос из постороннего источника заблокирован: Политика одного источника запрещает чтение удаленного ресурса на https://cms-res.online.sberbank.ru/sberid/BlackList/Button/No_Button.json. (Причина: не удалось выполнить запрос CORS). Код состояния: (null).
Если нажать на ссылку то открывается вкладка :Предупреждение: Вероятная угроза безопасности : если нажать подробнее то открывается вкладка :Ошибка при установлении защищённого соединения или соединение не установлено. 
нажать кнопку дополнительно открывается окно : Кто-то может пытаться подменить настоящий сайт и вам лучше не продолжать.
 Веб-сайты подтверждают свою подлинность с помощью сертификатов. Firefox не доверяет cms-res.online.sberbank.ru, потому что издатель его сертификата неизвестен, сертификат является самоподписанным, или сервер не отправляет корректные промежуточные сертификаты.
 
Код ошибки: SEC_ERROR_UNKNOWN_ISSUER
 Просмотреть сертификат

- ##### Окружение:

ПК desktop/ Windows 11 Pro.Версия 21H2


## Баг №3. Код ответа 502 на запрос GET https://sbermegamarketru.webim.ru/button.php при обновлении главной страницы https://sbermegamarket.ru/
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать кнопку обновить в браузере

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок
- Коды ответов у всех запросов при обновлении страницы 200-е

- ##### Фактический результат:
в консоли зафиксирована следующая ошибка:
- код ответа 502 Bad Gateway (неверный ответ от сервера)
- метод GET
- URL: https://sbermegamarketru.webim.ru/button.php
- Заголовки ответа:
```   	
    Connection
    	keep-alive
    Content-Length
    	1943
    Content-Type
    	text/html
    Date
    	Tue, 20 Jun 2023 08:28:27 GMT
    ETag
    	"6488db85-797"
    Server
    	nginx
```
- Заголовки запроса: 
```   	
    Accept
    	image/avif,image/webp,*/*
    Accept-Encoding
    	gzip, deflate, br
    Accept-Language
    	ru-RU,ru;q=0.8,en-US;q=0.5,en;q=0.3
    Connection
    	keep-alive
    Host
    	sbermegamarketru.webim.ru
    Referer
    	https://sbermegamarket.ru/
    Sec-Fetch-Dest
    	image
    Sec-Fetch-Mode
    	no-cors
    Sec-Fetch-Site
    	cross-site
    User-Agent
    	Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/114.0
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)


## Баг №4. Ошибка t is null при выборе в каталоге "Сделано в Москве" 
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать кнопку  Каталог
2. В открывшемся боковом меню выбрать "Сделано в Москве" 

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок  
- Отобразился список товаров  

- ##### Фактический результат:
- Отобразился список товаров  
в консоли зафиксирована следующая ошибка: 
- TypeError: DDManager Custom Event "Viewed Campaign" Error
```
 t is null
    campaign https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    h https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    campaigns https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    h https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    ...
node_modules.89ca50aa.js:2:383012
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)


## Баг №5.  Код ответа 400 на запрос  GET https://online.sberbank.ru/CSAFront/api/oidc/sbidclient_id=52cd75e2-76e1-43ba-ade6-938b2c7d4e7a при нажатии на кнопку Войти
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать кнопку  Войти

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок
- Появится модальное окно для авторизации на сайте

- ##### Фактический результат:
- Появилось модальное окно для авторизации на сайте
в консоли зафиксирована следующая ошибка:
- код ответа  400 Bad Request (сервер не смог понять запрос из-за недействительного синтаксиса)
- метод GET
- URL: https://online.sberbank.ru/CSAFront/api/oidc/sbid?client_id=52cd75e2-76e1-43ba-ade6-938b2c7d4e7a
- Заголовки ответа:
```
    Access-Control-Allow-Credentials
    	true
    Access-Control-Allow-Methods
    	GET
    Access-Control-Allow-Origin
    	https://sbermegamarket.ru
    Access-Control-Max-Age
    	600
    Connection
    	keep-alive
    Content-Length
    	0
    Date
    	Tue, 20 Jun 2023 10:12:45 GMT
    Set-Cookie
    	f5avraaaaaaaaaaaaaaaa_session_=FDJMKPDLIAKFKDGGCOEIDEGCEHPNMNJHHLCPPLEDLLFPLHJEFJMLACACICLOBGFBGEDDGKMCCLONDEDBLKMALKIHFHNCFJACCPENEJIKNDPLOBNFALFCGFIPILAMFCFN; HttpOnly; secure;
    Set-Cookie
    	TS019e0e98=0156c5c86022ead629bc8bcd661fd5bee339b83b52d74a10590d70c7a1b9aba6cbdfce35b8c896af4bec7c30e1dc0661900338351f06940e27bb29c22a4f160dec6995bc9a3c31cae833bff3dd4687565f9ace3dce3815174aeb873a47459968bd2dfd62bf; Path=/
    Set-Cookie
    	TS3bb85bd7027=08bd9624b8ab20003e39e04b67322c2aa453bf4d58456c8ec6ac77a427122d3dfd0dd157686323f308baf64222113000bc80cab6872dadb04693c5c4edfbfce6c317f5425afd2f8757c809d00134a4cf0baca601d9f5c802871724a686a69782; Path=/
```
- Заголовки запроса: 
```	
    Accept
    	*/*
    Accept-Encoding
    	gzip, deflate, br
    Accept-Language
    	ru-RU,ru;q=0.8,en-US;q=0.5,en;q=0.3
    Connection
    	keep-alive
    Cookie
    	f5avraaaaaaaaaaaaaaaa_session_=MNJPCICNLHANBKGLAJBBKBBJOJKIMCCFGHGFFGHKEJCLNIEFDDLBOGMIICEPBIKIHLLDIAHEMJPKPHHMNFGALLLDAHDPMPIEENCLOPIBLKENFKHIEDIKCJNLMHNGELAM; ESAWEBJSESSIONID=PBC5YS:17406548; TS0135c014=0156c5c860807fe1e276ebc257344843f9b5c1f990d5f47de9179711906534a857766658046ceb541f4f15bfea4a8cb737d91235e1b064a438268966a3f18370dd58e729a1; _sv=SA1.0f2f167e-9cc0-4523-8514-8eb173448271.1687208960; _ym_isad=2; _ym_uid=1687237133916527265; _ym_d=1687237501; JSESSIONID=node0gclm1utl4tqes1bxsfg5s2204873056.node0; TS019e0e98=0156c5c8605ab025e41be776f7b9ead1788cefc4d835a349b04dc5b3155f368e975db8a4c15dbaf2508c3aad3a02a8ab768e96a5fcdf3057287520d23f754f989437bda2002682b87521cb5a2ce1516e89ff52fc0aa596813b8374d07cd4d9a6f79cdaa9f2; TS3bb85bd7027=08bd9624b8ab2000772863cb02c99ccc9e68d976a3ea53c7df34ba5c99b651d0251f92f86cc5928e089aa2a2c0113000cbbda1dce191b884bf352ad5c2f9e5db68991ac15676f047ff927f313e3f558c50256e1dfe8ce6a55cb045f587cd7f4e
    Host
    	online.sberbank.ru
    Origin
    	https://sbermegamarket.ru
    Referer
    	https://sbermegamarket.ru/
    Sec-Fetch-Dest
    	empty
    Sec-Fetch-Mode
    	cors
    Sec-Fetch-Site
    	cross-site
    User-Agent
    	Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/114.0
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)  


## Баг №6. Ошибка e.getAttribute(...) is null при нажатии на кнопку "Корзина" 
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Пользователь авторизован
4. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать кнопку Корзина

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок
- Открывается Страница https://sbermegamarket.ru/multicart/, "Корзина"  

- ##### Фактический результат:
- Открылась Страница https://sbermegamarket.ru/multicart/, "Корзина"  
в консоли зафиксирована следующая ошибка:
- TypeError: DDManager Custom Event "Clicked ToCart Button (Desktop + Mobile Main Icon)" Error
```
e.getAttribute(...) is null
    handler https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    run https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    resolveHandlerAndFireEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    trackClick https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    i https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    o https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    s https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    p https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    ... 
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)  


## Баг №7. Ошибка JSON.parse: unexpected character at line 1 column 1 of the JSON data при нажатии на текст в футере сайта "База знаний" 
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать на текст в футере сайта "База знаний"

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок
- Открывается Страница https://partner-wiki.sbermegamarket.ru/, "Помощь продавцам"

- ##### Фактический результат:
- Открылась Страница https://partner-wiki.sbermegamarket.ru/, "Помощь продавцам"
- в консоли зафиксирована следующая ошибка:
```
SyntaxError: JSON.parse: unexpected character at line 1 column 1 of the JSON data
    <anonymous> https://partner-wiki.sbermegamarket.ru/s/d41d8cd98f00b204e9800998ecf8427e-CDN/g8kpk6/8804/1log4hf/27c6b5f597b37f548187348a79616089/_/download/contextbatch/js/browser-metrics-plugin.contrib,-_super,-viewcontent/batch.js?highlightactions=true:20
    i https://partner-wiki.sbermegamarket.ru/s/336fb53f5b34039447faad612a426cfc-CDN/g8kpk6/8804/1log4hf/b3787a8320a4f130e416f5326ae48227/_/download/contextbatch/js/_super/batch.js?locale=ru-RU:127
    add https://partner-wiki.sbermegamarket.ru/s/336fb53f5b34039447faad612a426cfc-CDN/g8kpk6/8804/1log4hf/b3787a8320a4f130e416f5326ae48227/_/download/contextbatch/js/_super/batch.js?locale=ru-RU:127
   ... 
batch.js:20:249 
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)  


## Баг №8. Код ответа 404 на запрос GET https://sbermegamarket.ru/info/about-sbermegamarket-ru/desktop/css/desktop.css при нажатии на текст "Настоящий маркетплейс" в футере сайта
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать на текст "Настоящий маркетплейс" в футере сайта

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок
- Открывается страница https://sbermegamarket.ru/info/about-sbermegamarket-ru/, "Маркетплейс СберМегаМаркет"

- ##### Фактический результат:
- Открылась страница https://sbermegamarket.ru/info/about-sbermegamarket-ru/, "Маркетплейс СберМегаМаркет"  
в консоли зафиксирована следующая ошибка:
- код ответа 404 Not Found 
- метод GET
- URL: https://sbermegamarket.ru/info/about-sbermegamarket-ru/desktop/css/desktop.css  
- Заголовки ответа:
```   	
    content-encoding
    	gzip
    content-type
    	text/html
    date
    	Tue, 20 Jun 2023 12:04:11 GMT
    server
    	nginx
    strict-transport-security
    	max-age=31536000; includeSubDomains
    X-Firefox-Spdy
    	h2
    x-sp-crid
    	152018004:5
```
- Заголовки запроса: 
```   	    	
    Accept
    	text/css,*/*;q=0.1
    Accept-Encoding
    	gzip, deflate, br
    Accept-Language
    	ru-RU,ru;q=0.8,en-US;q=0.5,en;q=0.3
    Connection
    	keep-alive
    Cookie
    	spid=1687208879723_cf2ca146756d650cad1eda10b0b66f62_6gcq32kpn3r6l3tb; _ym_uid=168720892012870705; _ym_d=1687208920; KFP_DID=b4245789-2379-c4b1-a4fa-230e926d7101; ssaid=948b4980-0ee5-11ee-bd11-d94e5c0bb8b1; adspire_uid=AS.1563408899.1687208970; _ym_isad=2; device_id=9740ddf1-0ee5-11ee-b89b-0242ac110002; cfidsw-smm=hO7/DvuM7RfA7ojRaDZm0WsVHE+9Pp2JhS5kGXOagqJasvTD0PuD+PZ5mxdUjKT0WLy6Mv8mBBvWTJ84ch7mqNK4bOEIkwPcf1F4BH5ZpsE6pCrM2yBca+r3e01C4ZFnHyOJkd1vCDHmYgJPVvJCsUdI9Njz/DqY4MeaKv4=; cfidsw-smm=2x/ZxyizSN08D+d/…-d6c9-bb42-d3e437a272a9#0#1800000#5000#1800000; _ym_visorc=b; address_info=%7B%22addressId%22%3A%2201b58d7f-dd8b-425f-a5c6-a1c015b67b99%2311%23%22%2C%22full%22%3A%22%D0%A1%D0%B0%D1%80%D0%B0%D1%82%D0%BE%D0%B2%D1%81%D0%BA%D0%B0%D1%8F%20%D0%BE%D0%B1%D0%BB%2C%20%D0%B3%20%D0%AD%D0%BD%D0%B3%D0%B5%D0%BB%D1%8C%D1%81%2C%20%D1%83%D0%BB%20%D0%9A%D1%80%D0%B0%D1%81%D0%BD%D0%BE%D0%B4%D0%B0%D1%80%D1%81%D0%BA%D0%B0%D1%8F%2C%20%D0%B4%2011%22%2C%22geo%22%3A%7B%22lon%22%3A46.125553%2C%22lat%22%3A51.472527%7D%7D; __tld__=null
    Host
    	sbermegamarket.ru
    Referer
    	https://sbermegamarket.ru/info/about-sbermegamarket-ru/
    Sec-Fetch-Dest
    	style
    Sec-Fetch-Mode
    	no-cors
    Sec-Fetch-Site
    	same-origin
    TE
    	trailers
    User-Agent
    	Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/114.0  
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)  


## Баг №9. Ошибка t.digitalData(...) is undefined при нажатии на текст "Настоящий маркетплейс" в футере сайта 
- #### Предшествующие условия:
1. Открыт браузер Firefox
2. Открыта страница https://sbermegamarket.ru/
3. Открыт DevTools

- ##### Серьёзность:
Minor

- ##### Шаги для воспроизведения:
1. Нажать на текст в футере сайта "Настоящий маркетплейс"

- ##### Ожидаемый результат.
- Веб-приложение работает без ошибок
- - Открывается страница https://sbermegamarket.ru/info/about-sbermegamarket-ru/, "Маркетплейс СберМегаМаркет"

- ##### Фактический результат:
- Открылась страница https://sbermegamarket.ru/info/about-sbermegamarket-ru/, "Маркетплейс СберМегаМаркет"
- в консоли зафиксирована следующая ошибка:
```
TypeError: DDManager Custom Event "Viewed Product Listing" Error

 t.digitalData(...) is undefined
    handler https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    run https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    resolveHandlerAndFireEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    trackEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireUnfiredEvents https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    ...
```
- ##### Окружение:
Windows 10, Firefox, Версия 114.0.1 (64-bit)  



