## Вкладка "Network" (Сеть) в DevTools в Firefox на сайте Сбермегамаркет.

1.***Какой запрос(-ы) отправляется на сервер для получения списка типов товаров в шторке "Каталог"?***

##### POST https://sbermegamarket.ru/api/mobile/v1/catalogService/catalog/menu

![Alt text](misc/images/image-3.png)

2. ***Какой запрос(-ы) отправляется на сервер при использовании поиска товаров в каталоге?***

##### POST https://sbermegamarket.ru/api/mobile/v1/catalogService/filters/search

![Alt text](misc/images/image.png)


##### POST https://sbermegamarket.ru/api/mobile/v3/catalogService/catalog/searchSuggest

![Alt text](misc/images/image-1.png)

##### POST https://sbermegamarket.ru/api/mobile/v1/catalogService/catalog/search


![Alt text](misc/images/image-2.png)

3. ***Какой запрос(-ы) отправляется на сервер при поиске региона или города в модалке выбора вашего региона?***

##### POST https://sbermegamarket.ru/api/mobile/v1/addressSuggestService/address/suggest

![Alt text](image-4.png)
