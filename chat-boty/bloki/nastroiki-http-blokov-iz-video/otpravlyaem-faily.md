---
description: Способ отправки файлов с помощью http запроса при обращении к ИИ.
---

# Отправляем файлы

## Блок HTTP запрос

{% hint style="info" %}
**Применяется метод POST-запрос**
{% endhint %}

> Http request: [https://gigachat.devices.sberbank.ru/api/v1/files](https://gigachat.devices.sberbank.ru/api/v1/files)

{% hint style="success" %}
Добавлен метод **multipart/form-data** с возможностью прикрепить файл
{% endhint %}

<figure><img src="../../../.gitbook/assets/Скриншот 21-03-2025 203729 (1).jpg" alt="" width="563"><figcaption><p>В распоряжении два способа добавления файлов.</p></figcaption></figure>



Файл, который пользователь отправил в боте.&#x20;

В этом случае не забудьте преобразовать ссылку с помощью метода [decodeShortLink](https://docs.watbot.ru/rabota-s-api/ssylki-na-mediafaily)

<figure><img src="../../../.gitbook/assets/Скриншот 21-03-2025 203823.jpg" alt="" width="563"><figcaption></figcaption></figure>

Выбрать локальный файл с компьютера.

<figure><img src="../../../.gitbook/assets/Скриншот 21-03-2025 203928.jpg" alt="" width="563"><figcaption></figcaption></figure>

Частое и наиболее подходящее применение - это отправка файла (картинки или голосового сообщения) в ИИ, для обработки данного файла и выдачи результата.
