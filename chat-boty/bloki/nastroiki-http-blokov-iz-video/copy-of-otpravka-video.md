# Отправка фото

Как отправить фото.

<figure><img src="../../../.gitbook/assets/Скриншот 31-07-2025 151530.jpg" alt=""><figcaption></figcaption></figure>

**Создайте блок** **HTTP-запрос с запросом https://api.telegram.org/botТОКЕНБОТА/sendPhoto**\
\
**Настройки для блока:**

Метод POST

1. Токен бота из @BotFather
2. chat\_id = \{{ telegram\_id \}}
3. photo = ссылка на фото из хостинга, телеграмм канала, либо переменная.
4. Проверенный и работающий вариант - загрузить видео в свой тг-канал и скопировать ссылку на сообщение.&#x20;



### Получение ссылки на фото, отправленное пользователем.&#x20;

Записываем ответ пользователя в переменную, к примеру **url\_photo**.

<figure><img src="../../../.gitbook/assets/Скриншот 31-07-2025 152233.jpg" alt=""><figcaption></figcaption></figure>

https://watbot.ru/api/v1/decodeShortLink?

api\_token=\{{ token\_WB\}}

\&url=\{{ $url\_photo\}}



Заголовок: X-Requested-With:XMLHttpRequest

\{{ token\_WB\}} - токен из личного кабинета [Watbot](https://watbot.ru/account/api).&#x20;



<figure><img src="../../../.gitbook/assets/Скриншот 31-07-2025 152339.jpg" alt=""><figcaption></figcaption></figure>

Записываем ответ json в переменные.

data.url = url\_photo
