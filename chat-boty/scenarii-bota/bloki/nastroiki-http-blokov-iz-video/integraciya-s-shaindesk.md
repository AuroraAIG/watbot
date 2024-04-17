---
description: Способ интеграции с сервисом Сhaindesk
---

# Интеграция с Сhaindesk

> Документация интеграции с сервисом Chaindesk расположена по-адресу&#x20;
>
> [https://docs.chaindesk.ai/introduction](https://docs.chaindesk.ai/introduction)

## Блок HTTP запрос

{% hint style="info" %}
**Применяется метод POST-запрос**
{% endhint %}

> Http request: [https://api.chaindesk.ai/agents/clsaglahh004wo98i3fxh4738/query](https://api.chaindesk.ai/agents/clsaglahh004wo98i3fxh4738/query)

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2024-04-17 в 21.20.39.png" alt=""><figcaption><p>Запрос к сервису Сhaindesk</p></figcaption></figure>



<figure><img src="../../../../.gitbook/assets/Снимок экрана 2024-04-17 в 21.21.05.png" alt=""><figcaption><p>Вывод ответа в json переменные</p></figcaption></figure>

#### Json-запрос

```json
{
  "modelName": "gpt_3_5_turbo_16k",
  "maxTokens": 500,
  "presencePenalty": 0,
  "promptTemplate": "{{$вопрос}}",
  "promptType": "raw",
  "query": "{{$вопрос}}",
  "streaming":false 
}
```
