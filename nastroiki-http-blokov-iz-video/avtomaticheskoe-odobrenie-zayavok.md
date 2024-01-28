---
description: >-
  Чат-бот для автоматического одобрения заявок в частную группу или
  телеграмм-канал
---

# Автоматическое одобрение заявок



<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

#### 1 блок HTTP запроса

```
https://api.telegram.org/bot{{token}}/getChatMember?chat_id={{chat_id}}&user_id={{telegram_id}}
```

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

#### 2 блок HTTP

```
https://api.telegram.org/bot{{token}}/ApproveChatJoinRequest?chat_id={{chat_id}}&user_id={{telegram_id}}&hide_requester=true

```

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

3 блок HTTP запрос

```
https://api.telegram.org/bot{{token}}/banChatMember?chat_id={{chat_id}}&user_id={{telegram_id}}
```

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
