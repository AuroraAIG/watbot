---
description: >-
  С помощью данного способа вы можете отправлять текст, данные из
  пользовательских переменных
---

# Пересылка информации из бота в канал или группу

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

Настройки блока HHTP-запрос:

**URL:**&#x20;

```
https://api.telegram.org/bot{{token}}/sendMessage?
```

**Metod** - POST

**Body:**

json

```
{
"chat_id":"чат айди из  специального бота",
"text":"Ваш текст" , 
"parse_mode": "html"
}
```

{% embed url="https://www.youtube.com/watch?v=bLLCAO2RIzU" %}
Видео-инструкция
{% endembed %}
