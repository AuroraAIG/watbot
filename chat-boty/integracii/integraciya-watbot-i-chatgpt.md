# Интеграция Watbot и ChatGPT

Для того чтобы "подружить" Watbot и ChatGPT для начала нужно завести аккаунт на сайте [https://platform.openai.com](https://platform.openai.com)

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-25 в 21.49.49.png" alt=""><figcaption><p>Кнопка регистрации на сайте openai.com</p></figcaption></figure>

<div data-full-width="true">

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-25 в 21.51.26.png" alt="" width="375"><figcaption><p>Окно регистрации на сайте openai.com</p></figcaption></figure>

</div>

Далее вам на почту придет подтверждающее письмо, и вы можете заходить в личный кабинет

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-25 в 21.52.31.png" alt=""><figcaption><p>Личный кабинет в платформе openai</p></figcaption></figure>

Чтобы завести ключ API переходим в раздел API Keys  и нажимаем Create&#x20;

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-25 в 21.56.08.png" alt=""><figcaption><p>Создание ключа апи в openai</p></figcaption></figure>

После создания ключа его можно использовать в http-блоке в сценарии бота

ссылка запроса:

[https://api.openai.com/v1/chat/completions](https://api.openai.com/v1/chat/completions)

в тело запроса добавляем следующий код:

```
{
    "model": "gpt-4o",
    "messages": [
      {
        "role": "system",
        "content": "You are a helpful assistant."
      },
      {
        "role": "user",
        "content": "{{$prompt}}"
      }
    ]
}
```

<div data-full-width="true">

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-25 в 23.30.52.png" alt="" width="375"><figcaption><p>Настроенный http-блок </p></figcaption></figure>

</div>

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-25 в 23.33.14.png" alt="" width="375"><figcaption><p>Включенный прокси в http-блоке</p></figcaption></figure>

