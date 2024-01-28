---
description: Чат-бот со встроенной реферальной системой
---

# Реферальная система

HTTP-запрос (оба блока одинаковые)

<figure><img src="../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

**URL**

```
https://watbot.ru/api/v1/getReferrals?api_token=BSSbyrmnPAxjb6ivWmPSGorknl8QaPig8RjkjoFq3UE8uEXVcm4RQifLXetM&contact_id={{id}}
```

Method - POST

Body - x-www-form-urlencoded

Соотношение переменных:

data.0.name - usernames

data.0.telegram\_id - userid

data.0.telegram\_username - telegramusrname

data.meta.to - to
