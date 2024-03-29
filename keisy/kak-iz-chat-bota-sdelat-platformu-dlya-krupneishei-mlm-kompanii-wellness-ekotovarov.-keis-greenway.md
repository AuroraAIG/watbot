# Как из чат-бота сделать платформу для крупнейшей МЛМ компании Wellness-экотоваров. Кейс Greenway

![](https://leonardo.osnova.io/4bda6118-0638-5224-8584-2cb3100450a7/-/preview/800/-/format/webp/)

В 2021 году наблюдается такой рост внедрения чат-ботов в бизнес различных ниш, что скоро они будут являться базовым техническим оснащением как и сайты.

Не исключением стала и компания Greenway, которой потребовался чат-бот, который бы выполнял функцию по обучению новых сотрудников и содержал всю необходимую информацию с удобной навигацией.

По данным на ноябрь 2021 года количество поисков в Яндекс достигло 500,000! При работе с такими масштабами требуется максимальная автоматизация с минимальным привлечением сотрудников. Бот компании был создан 1,5 года назад и на данный момент насчитывает почти 8,000 пользователей. В качестве канала для работы был выбран Телеграм, т.к. он является наиболее простым для подключения и наиболее удобным с точки зрения функционала (кликабельные кнопки, медиа-материалы, которые сохраняются в боте и т.д.)

**Зачем чат-бот компании Гринвей?**

Когда к компании хочет присоединиться новый партнёр, необходимо чтобы он

\- получил базовую презентацию компании

\- узнал о продукции

\- увидел отзывы других партнеров

\- имел под рукой все важные контакты

\- изучил видео инструкцию по личному кабинету

\- умел активировать свой личный кабинет

\- прошел обучение после активации

При этом, из-за большого количества пользователей, необходимо было исключить наличие технической поддержки. Т.е. структура чат-бота должна быть выстроена максимально логично, чтобы не возникало никаких вопросов и все задачи были выполнены только при помощи информации, добавленной в чат-бот. Также требовалось, чтобы в раздел "обучение" было возможно перейти только после активации личного кабинета. И даже если пользователь ранее не пользовался чат-ботами, он смог бы всё интуитивно понять. Давайте подробно разберём структуру этого чат-бота!

**1) Информационная составляющая**

![](https://leonardo.osnova.io/78f028e3-8146-5e7b-9960-216d24483a6e/-/preview/800/-/format/webp/)

На карте сценария можно увидеть блоки (в боте это те самые сообщения, по которым пользователь ищет информацию). В блоках содержатся кнопки (они отмечены зелёным цветом). Отметим, что в каждом блоке содержится всего по несколько кнопок, чтобы не путать пользователя. И в каждом блоке содержится только одна смысловая часть.

А именно,

\- о компании

\- история

\- отзывы

\- маркетинг-план

\- секрет млм

\- отработка сомнений

\- информация о личном кабинете

\- подробности активации личного кабинета

\- сайты

\- контакты

\- инструкция по использованию кнопок в боте

**2) Особенности наполнения блоков**

![](https://leonardo.osnova.io/361f201f-f4da-518d-9917-a66c51455a32/-/preview/500/-/format/webp/)![](https://leonardo.osnova.io/a794427d-3c92-5510-940c-ae3e00dda5be/-/preview/500/-/format/webp/)

На скринах выше можно увидеть принцип, по которому выстраивается структура сообщений. Минимальное количество текста и ссылка на видео. Т.к. информация достаточно объемная, не было смысла переводить её в текст и отправлять длинные сообщения. В итоге пользователь получает короткое сообщение, все детали он может узнать, посмотрев видео.

**3) Доступ к продукции после активации**

![](https://leonardo.osnova.io/59ea4a32-b477-5605-a4f4-985371ffbf65/-/preview/500/-/format/webp/)

Это возможно сделать с помощью блока "условие". Чтобы перейти к обучению, необходимо ввести кодовое слово/цифру. Оно же устанавливается в самом блоке и пускает к последующий информации, только если обнаружено совпадение

**4) Сценарий "Обучение"**

![](https://leonardo.osnova.io/4d1f7d08-e279-5e4a-8f75-5aca4ed4c92d/-/preview/600/-/format/webp/)

Все блоки с сообщениями можно добавлять как на одной карте, так и на нескольких. Это делается для удобства специалиста по сборке чат-бота. Если всё будет на одной карте, то из-за большого количества блоков в них будет тяжело ориентироваться.

В сообщениях сценария обучения содержится видео + домашнее задание. Его результат пользователь отправляет прямо в чат. И он записывается в пользовательскую переменную, которая сохраняется в карточке. Далее, при необходимости, их можно проверить.

Ещё один вариант проверки домашних заданий, уже автоматизированный, реализован с помощью блока "условие".Если ответ верный, то приходит сообщение со следующим заданием, если нет - соответствующее уведомление.

![](https://leonardo.osnova.io/0c82b79b-2492-5369-bae9-8687b0a4cead/-/preview/500/-/format/webp/)

Таким образом мы получили простой и функциональный чат-бот, отвечающий всем поставленным задачам.

**Данный чат-бот был собран на платформе-конструкторе Watbot. С его помощью вы сможете собрать чат-бота для реализации ваших целей. Регистрируйтесь и получайте бонусные баллы для тестирования вашего чат-бота!**
