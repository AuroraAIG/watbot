# Интеграция Chat GPT c чат-ботом

Для интеграции мы использовали сервис [chadgpt.ru](https://chadgpt.ru/)

Стоимость и тарифы смотрите на сайте (для работы данного бота хватит минимального тарифа)&#x20;

<figure><img src="../../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Переменная "вопрос" записывается в блоке, где пользователь задает вопрос </p></figcaption></figure>

URL:&#x20;

```
https://ask.chadgpt.ru/api/public/gpt-3.5?
```

Method: POST

Body: json

```
{
"message": "{{$Вопрос}}",
"api_key": "ваш ключ"
}
```

Где найти Апи-ключ (api\_key):

1. Перейти на сайт [chadgpt.ru](https://chadgpt.ru/)
2. Нажать "использовать бесплатно"

<figure><img src="../../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Нажать на меню

<figure><img src="../../../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

4. Перейти в личный кабинет

<figure><img src="../../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

5. Перейти в раздел API для разработчиков

<figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

6. Зайти в раздел мой API ключ

&#x20;

<figure><img src="../../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

7. Скопировать API ключ и вставить его в json-массив (см.скриншот блока)
