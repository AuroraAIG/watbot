---
description: Прием платежей в ботах WhatsApp, Viber, Telegram, ICQ
---

# Платежи

## Какие платёжные системы доступны для интеграции?

* юkassa
* юmoney
* robokassa
* cloud payments
* liqpay
* JustClick
* bePaid
* flowell
* cryptopay

### Общая схема

Чтобы принимать платежи в ботах нужно в разделе **Настройки** -> **Интеграции** подключить платежную систему Яндекс.Касса.

![Интерфейс подключения Яндекс.Касса ](<../../.gitbook/assets/image (160).png>)

Заполните соответствующие поля во вкладке **Основное** и нажмите кнопку **Сохранить**, после чего система сгенерирует webhook (ссылку), который нужно скопировать и сохранить в личном кабинете сервиса Яндекс.Касса в настройках в поле URL для уведомлений.

![ Личный кабинет Яндекс.Касса](<../../.gitbook/assets/image (97).png>)

Во вкладке **Оповещения** вы можете указать URL для уведомлений (только https), на который будет приходить информация о платежах. Ответ должен содержать код состояния `200`. В случае ошибки, система будет пытаться доставить уведомление в течение суток, постепенно увеличивая интервал между запросами.

![Настройка оповещений](<../../.gitbook/assets/image (185).png>)

О каких статусах вы будете получать уведомления:

* `pending` - платеж создан, но не завершен.
* `waiting_for_capture` - платеж выполнен и ожидает подтверждения.
* `succeeded` - платеж успешно завершен.
* `canceled` - платеж отменен.

Подробнее о статусах сервиса Яндекс.Касса смотрите по ссылке:

{% embed url="https://kassa.yandex.ru/developers/payments/payment-process#payment-statuses" %}

**Пример оповещения для статуса `pending`. Платеж на 900 руб.**

```javascript
{
    "id": 1,
    "provider": "yandex_kassa",
    "provider_id": "12345678-1234-1234-1234-123456789ab",
    "currency": "RUB",
    "amount": 90000,
    "state": "pending",
    "created_at": 1554717083,
    "payload": null,
    "order": [
         {
             "name": "Название товара",
             "description": "Описание товара",
             "amount": 900
         }
    ],
    "contact": {
         "id": 1,
         "name": "Дмитрий",
         "messenger": "whatsapp",
         "phone": "79999999999"
    }
}
```

{% hint style="info" %}
Поле `amount` содержит сумму в минимальной единице измерения валюты.
{% endhint %}

**Пример оповещения для статуса `waiting_for_capture`**

```javascript
{
    "id": 1,
    "provider": "yandex_kassa",
    "provider_id": "12345678-1234-1234-1234-123456789ab",
    "currency": "RUB",
    "amount": 90000,
    "state": "waiting_for_capture",
    "created_at": 1554717099,
    "payload": {
        "type": "notification",
        "event": "payment.waiting_for_capture",
        "object": {
            "id": "12345678-1234-1234-1234-123456789ab",
            "status": "waiting_for_capture",
            "paid": true,
            "amount": {
                "value": "900.00",
                "currency": "RUB"
            },
            "authorization_details": {
                "rrn": "858585858585",
                "auth_code": "555444"
            },
            "created_at": "2019-04-08T09: 51: 35.762Z",
            "description": "[ID1] Дмитрий +79999999999",
            "expires_at": "2019-04-15T09: 51: 38.488Z",
            "metadata": [

            ],
            "payment_method": {
                "type": "bank_card",
                "id": "12345678-1234-1234-1234-123456789ab",
                "saved": false,
                "card": {
                    "first6": "555555",
                    "last4": "4444",
                    "expiry_month": "12",
                    "expiry_year": "2021",
                    "card_type": "MasterCard"
                },
                "title": "Bank card *4444"
            },
            "recipient": {
                "account_id": "123456",
                "gateway_id": "654321"
            }
        }
    },
    "order": [
        {
            "name": "Название товара",
            "description": "Описание товара",
            "amount": 900
        }
    ],
    "contact": {
        "id": 1,
        "name": "Дмитрий",
        "messenger": "whatsapp",
        "phone": "79999999999"
    }
}
```

##
