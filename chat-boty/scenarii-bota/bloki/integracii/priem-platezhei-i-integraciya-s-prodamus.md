---
description: Интеграция Watbot c платежной системой Prodamus
---

# Прием платежей и интеграция с Prodamus

Особенности платежной системы:

* отправляет покупателям фискальные чеки (по 54-ФЗ) без необходимости покупать или брать в аренду электронную кассу
* работает с самозанятыми
* комиссия сервиса около 3.5%

Для того, что бы подключить прием платежей в боте через п/с Prodamus, перейдите в созданного бота на платформе

<figure><img src="../../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Далее, перейдите в настройки. Они располагаются слева в столбце, иконка "шестеренки"

<figure><img src="../../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Переходим в раздел "интеграции". Сверху видны активные интеграции, снизу возможные. Выбираем "Prodamus"

<figure><img src="../../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Для подключения Prodamus Вам понадобятся URL-платежной формы и секретный ключ. URL-платежной формы вы получаете после регистрации, он имеет вид: demo.payform.ru

<figure><img src="../../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

Секретный ключ можно получить в личном кабинете платежной формы Prodamus, там же нужно будет прописать URL адрес для уведомлений.

Подробная инструкция как это сделать: [https://help.prodamus.ru/payform.ru-onlain-oplaty/prochee/url-dlya-uvedomlenii-i-sekretnyi-klyuch](https://help.prodamus.ru/payform.ru-onlain-oplaty/prochee/url-dlya-uvedomlenii-i-sekretnyi-klyuch)

Далее переходим в интегрированный блок Prodamus и в разделе Webhook копируем ссылку

<figure><img src="../../../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Интеграция появилась в списке активных</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Далее переходим в личный кабинет платежной формы Prodamus и в разделе Настройка уведомлений вставляем скопированную ссылку

<figure><img src="../../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Далее настраиваем блок приема платежей Prodamus, в сценарии в разделе&#x20;

<figure><img src="../../../../.gitbook/assets/image (30).png" alt=""><figcaption><p>Платежный блок Prodamus</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (31).png" alt=""><figcaption><p>Назначаем назначение и описание платежа</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (32).png" alt=""><figcaption><p>Выбираем предмет расчета и сумму</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (33).png" alt=""><figcaption><p>После оплаты назначаем тэг</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (34).png" alt=""><figcaption><p>Настраиваем блок "условие", если оно выполняется - отправляем ссылку на ресурс</p></figcaption></figure>

После настройки блока, приходит ссылка на оплату

<figure><img src="../../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (36).png" alt=""><figcaption><p>Выбираете способ оплаты</p></figcaption></figure>

После успешной оплаты клиент получает, необходимые материалы
