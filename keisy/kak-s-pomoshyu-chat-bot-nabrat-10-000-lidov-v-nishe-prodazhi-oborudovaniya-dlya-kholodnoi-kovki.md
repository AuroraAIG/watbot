# Как с помощью чат-бот набрать 10,000 лидов в нише продажи оборудования для холодной ковки

![](https://leonardo.osnova.io/c9734515-4a91-5775-ab31-306d7cb134ee/-/preview/800/-/format/webp/)

Сегодня команда платформы-конструктора WatBot поделится с вами кейсом разработки чат-бота для необычной ниши: продажа станков для изготовления товаров методом холодной ковки.

Некоторые думают, что чат-ботами пользуются только самые распространенные ниши для решения очевидных задач:

* в недвижимости для бронирования объектов
* в сфере услуг для записи клиентов
* в инфобизнесе для создания автоворонок и повышения доходимости до вебинаров
* инстамагазины для мгновенного выбора товара, добавления в корзину и оплаты

Всё действительно так. Вышеуказанные примеры это кейсы, которые встречаются чаще всего. Даже не так, очень часто. И обратите внимание, насколько разным бизнесам чат-бот помогает в автоматизации процессов: от аренды вилл до записи в салон красоты!

**Почему все бизнесы внедряют чат-боты?**

Ответ прост: это универсальное и многофункциональное средство для решения большого круга задач. В 2021 году возможности чат-ботов настолько разнообразны, что некоторые даже не догадываются обо всех их способностях.

**Вот несколько примеров:**

* в чат-боте можно создать очень крутую автоворонку с сегментацией аудитории. И уже после сегментации пользователям будет выдаваться лид-магнит, соответствующий особенностям именной той группе ЦА, в которой они находятся. Чат-бот позволяет не вести всех вошедших в бот по одной воронке, а поделить их на несколько для более точечной работы с болями
* в чат-бот можно внедрить геймификацию. Например, проводить конкурсы и квизы. Или голосования среди предложенных участников с автоматическим выводом победителя. Да-да, чат-бот сам подсчитывает количества голосов, отданных разным конкурсантам
* на базе чат-бота можно создать полноценный лендинг. Для дизайна есть весь необходимый набор инструментов: добавление кнопок, ведущих в другой блок/сайт, цвета кнопок/фона, шрифты.

**Продажа оборудования для холодной ковки**

_Давайте подробнее рассмотрим структуры чат-бота для такой редкой ниши_

**1. Стартовое сообщение**

В нём содержится

\-приветствие

\- описание того, чем занимается компания

\- основные разделы с информацией (по аналогии с вкладками на сайтах. Только вместо перехода на другую вкладку мы нажимаем нужную кнопку, и к нам в чат приходит вся информация).

Также обратите внимание, что кнопки находятся под сообщением. А в тексте названия кнопок дублируются и нумеруются. Для чего это сделано: чат-бот был подключен и к WhatsApp, и к Telegram. В Telegram есть функция перехода к следующему сообщению нажатием кнопки. А в WhatsApp её нет, клиентам необходимо отправить цифру раздела, куда они хотят перейти.

![](https://leonardo.osnova.io/a649d1ea-2ec2-5982-b5fa-e0f769f44424/-/preview/600/-/format/webp/)

**2. Ассортимент продукции**

Нажав на первую кнопку мы можем перейти в блок, где находится список всего продаваемого оборудования. Можно также нажать на интересующий товар и получить более подробную информацию

![](https://leonardo.osnova.io/dc4bf6f0-3cc1-528f-96c9-fe94bfe6fcb1/-/preview/600/-/format/webp/)

**3. Заказ продукции**

Можно увидеть, что практически в каждом сообщении есть кнопка заказа товар. Если мы кликаем на неё, нам приходит прайс и фото акционного товара для более наглядной презентации. В ответ нас просят отправить цифру, которой соответствует интересующий нас товар. После того, как мы это сделаем, с нами связывается менеджер.

Как менеджер узнаёт об этом? В настройках бота есть возможность отправлять ответ на указанный канал, например, в телеграм менеджера или на почту. А также интегрировать бот с crm-системой. Таким образом ни один клиент не будет пропущен

![](https://leonardo.osnova.io/f7aec103-a02c-5783-99f3-eccd899f20ba/-/preview/600/-/format/webp/)

**4. Расчёт доставки**

Если мы хотим узнать данную информацию, нас просят указать название города и количество станков к покупке. Эти данные в настройках блока записываются в пользовательскую переменную и сохраняются в карточке клиента. Далее с нами связывается менеджер. Как заявка попадает к менеджеру было описано в предыдущем пункте.

![](https://leonardo.osnova.io/a3351012-b8bc-58ad-8ef3-2cdef407079d/-/preview/600/-/format/webp/)

**5. Подробная информация о товаре**

Далее следует кнопка, которая выведет нам ссылки на видео товаров на ютуб, каталоги и другую полезную информацию. Обратим внимание, что в каждом разделе есть кнопка возврата либо в предыдущее меню, либо в главное. Таким образом у клиента всегда есть возможность возвратиться на один или несколько шагов назад.

![](https://leonardo.osnova.io/7e5b6d51-e4d7-53c0-a443-9f6bfb22739e/-/preview/600/-/format/webp/)

**6. Отзывы о товаре**

Отзывы - важнейшая часть воронки продаж. Редко какой клиент согласиться сделать покупке не видя отзывов от предыдущих покупателей. Поэтому этот раздел обязательно должен присутствовать и в чат-боте.

![](https://leonardo.osnova.io/66ae0d58-4e27-5c20-9bd7-dbbfe27fd0a5/-/preview/600/-/format/webp/)

**7. Способы связи**

Как и на любой другой платформе обязательно должны быть способы связи: у данной компании их 5 (vk, instagram, email, whatsapp и телефон).

![](https://leonardo.osnova.io/3b9206cf-b114-5c67-8ddc-32b1bff901da/-/preview/600/-/format/webp/)

**Мы увидели, что каким бы бизнесом не владел человек, даже если у него очень редкая ниша, чат-бот всё равно облегчит работу.**

**Для создания чат-бот приглашаем вас на нашу платформу-конструктор WatBot! Регистрируйтесь, получайте баллы для тестового использования чат-бота и автоматизируйте ваш бизнес!**