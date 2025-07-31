---
description: Как отправить несколько фотографий в одном сообщении?
---

# Отправка группы фото

{% embed url="https://youtu.be/FkudcnlTgJ0" %}

**1 блок HTTP-запрос с функцией чтения записи**&#x20;

URL - [https://watbot.ru/api/v1/getListItems](https://watbot.ru/api/v1/getListItems)

Method - POST

Body - x-www-form-urlencoded

api\_token - "ключ с платформы"

schema\_id - "адрес из ссылки"

_Записать ответ json в переменные_

data.\{{$N\}}.foto1.url → фото1

data.\{{$N\}}.foto2.url → фото2

data.\{{$N\}}.foto3.url → фото3

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

**2 блок HTTP-запрос с выводом фото**

URL - [https://api.telegram.org/bot\{{bot\_token\}}/sendMediaGroup?](https://api.telegram.org/bot%7B%7Bbot_token%7D%7D/sendMediaGroup?)

Method - POST

Body - json

```json
{
  "chat_id": "{{ telegram_id }}",
  "media": [
    {"type": "photo", "media": "ссылка на фото"},
{"type": "photo", "media": "{{ $фото1}}"},
{"type": "photo", "media": "{{ $фото2}}"},
{
      "type": "photo",
      "media": "{{ $фото3}}",
      "caption": "описание",
      "parse_mode": "HTML"
    }
  ]
}

```

<div><figure><img src="../../../../.gitbook/assets/Скриншот 31-07-2025 160917.jpg" alt=""><figcaption></figcaption></figure> <figure><img src="https://skr.sh/sWsWbLQpEps" alt=""><figcaption></figcaption></figure></div>

<figure><img src="../../../../.gitbook/assets/Скриншот 31-07-2025 161248.jpg" alt=""><figcaption></figcaption></figure>
