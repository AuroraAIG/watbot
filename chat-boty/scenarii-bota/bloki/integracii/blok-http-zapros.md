---
description: Расширение возможностей конструктора через стороннее API
---

# HTTP-запрос

### Шаг №1 - Создание блока HTTP-запрос

![Меню создания блока HTTP-запрос](<../../../../.gitbook/assets/image (157).png>)

### Шаг №2 - Настройка

![Настройка HTTP-запроса](<../../../../.gitbook/assets/image (158).png>)

Укажите тип запроса и ваш URL для обработки запроса. На данный момент поддерживаются методы `GET` и `POST`.

## Запрос

В теле запроса приходят все пользовательские переменные полученные на предыдущих шагах, контакт пользователя и данные crm систем.

#### Пример запроса:

```javascript
{
    "variables": [
        {
            "name": "Город",
            "value": "Москва"
        }
    ],
    "contact": {
        "name": "Дмитрий",
        "messenger": "whatsapp",
        "phone": "79999999999"
    }
}
```

{% hint style="warning" %}
**Время ожидания соединения:** 3 секунды
{% endhint %}

#### Ответ

В случае успеха, сервер должен ответить кодом `200`, а тело должно содержать текст для пользователя.

Текст должен быть форматирован под стандарты WhatsApp. Форматирование под другие мессенджеры происходит автоматически на нашем сервере.

В случае ошибки (например валидации), вы можете сообщить пользователю об этом. Для этого сервер должен ответить кодом `422`, а тело должно содержать сообщение для пользователя.

В таком случае не забудьте указать переменную в конструкторе для данного шага, в которую запишется ответ пользователя и отправиться на ваш сервер еще раз.

![Переменная в блоке HTTP-запроса](<../../../../.gitbook/assets/image (121).png>)

{% hint style="warning" %}
**Время получения ответа:** 5 секунд
{% endhint %}

В ссылку для блоков HTTP-запрос и Webhook возможно подставлять пользовательские переменные и константы

![](../../../../.gitbook/assets/5г.png)
