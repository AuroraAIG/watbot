# Системные функции

{% hint style="info" %}
**Функция** - подпрограмма, которую можно вызвать. Результат выполнения функции подставляется в сообщение от бота. В функцию можно передать аргументы (параметры), от которых зависит результат выполнения функции.
{% endhint %}

{% hint style="warning" %}
Пока платформа не поддерживает вложение функции в функцию
{% endhint %}

## Арифметические операции



**Сумма чисел:** `{{ sum(1, 2) }}`

**Сумма пользовательских переменных:** `{{ sum($переменная1, $переменная2) }}`

**Сумма нескольких значений:** `{{ sum($переменная1, 1, 2) }}`

**Псевдоним функции:** `{{ сумма(1, 2) }}`



**Разность чисел** `{{ diff(4, 2) }}`&#x20;

**Разность пользовательских переменных:** `{{ diff($переменная1, $переменная2) }}`

**Разность нескольких значений:** `{{ diff($переменная1, 1, 2) }}`

**Псевдоним функции:** `{{ разность(4, 2) }}`



**Произведение чисел:**`{{ multiplication(2, 2) }}`&#x20;

**Произведение пользовательских переменных:** `{{ multiplication($переменная1, $переменная2) }}`

**Произведение нескольких значений:** `{{ multiplication($переменная1, 1, 2) }}`

**Псевдоним функции:** `{{ произведение(2, 2) }}`



**Деление чисел:** `{{ div(4, 2) }}` -&#x20;

**Деление пользовательских переменных:** `{{ div($переменная1, $переменная2) }}`

**Деление нескольких значений:** `{{ div($переменная1, 4, 2) }}`

**Псевдоним функции:** `{{ деление(4, 2) }}`



**Записать сумму переменных/чисел в переменную**`{{ setSumVariablesIntoVariable("сумма", "а", "б") }}` -&#x20;

В переменную **`$cумма`** запишется сумма переменных **`$а`** и **`$б`**. В функцию передаются имена переменных в двойных кавычках или числа. Количество аргументов для передачи в функцию может быть до 100 шт.



**Записать произведение переменных/чисел в переменную**`{{ setMultiplicationVariablesIntoVariable("произведение", "а", "б") }}` -&#x20;

В переменную **`$произведение`** запишется произведение переменных **`$а`** и **`$б`**. В функцию передаются имена переменных в двойных кавычках или числа. Количество аргументов для передачи в функцию может быть до 100 шт.

## Работа с датой&#x20;



**Вчера** - \{{ date("d.m.Y", "yesterday") \}}

**Сегодня**- \{{ date("d.m.Y", "today") \}}

**Завтра** - \{{ date("d.m.Y", "tomorrow") \}}

**Послезавтра** - \{{ date("d.m.Y", "+ 2 days") \}}

**Следующая среда** - \{{ date("d.m.Y", "next wednesday") \}}

**Прошлая пятница** - \{{ date("d.m.Y", "last friday") \}}

**Этот четверг** - \{{ date("d.m.Y", "this thursday") \}}

**14 дней вперед** - \{{ date("d.m.Y", "+ 14 days") \}}

**7 дней назад** - \{{ date("d.m.Y", "- 7 days") \}}

**2 часа вперед** -  \{{ date("d.m.Y H:i:s", "+ 2 hours") \}} (Часовой пояс по умолчанию UTC-0)

Для того, чтобы к текущей дате прибавить месяц(или любую другую единицу времени) и вывести в формате даты вы можете воспользоваться функцией **modifyDateTime.**&#x20;

Для этого вам нужно:

1\. Изначально _записать текущую дату в переменную_, например в переменную "currentDate" с помощью блока "Операция над переменной" - \{{ date("d.m.Y") \}}&#x20;

2\. Прибавить к текущей дате месяц: \{{ modifyDateTime($currentDate, "d.m.Y", "d.m.Y", "+30 days +12 hours") \}}

Описание аргументов функции modifyDateTime:

* 1-ый аргумент функции должен содержать дату или переменную с датой
* 2-ой аргумент функции должен содержать формат даты, которая передается в первом аргументе
* 3-й аргумент функции должен содержать формат даты в который нужно преобразовать дату переданную в первом аргументе
* 4-й аргумент функции (необязательный) должен содержать модификатор даты (+30 days +12 hours ...)
* 5-й аргумент функции и дальше (необязательный) должны содержать переменные для замены знаков "?" в аргументах с 1-го по 4-ый последовательно

## Преобразование даты в UNIX формат

**Текущее время** - \{{date("U")\}}

**Пять минут вперёд** - \{{date("U", "+ 5 minutes")\}}

**Пять минут назад** - \{{date("U", "- 5 minutes")\}}

**Пять часов вперёд** - \{{date("U", "+ 5 hours")\}}

**Пять часов назад** - \{{date("U", "- 5 hours")\}}

**Пять дней вперёд** - \{{date("U", "+ 5 days")\}}

**Пять дней назад** - \{{date("U", "- 5 days")\}}

**Преобразование даты из переменной** - \{{date("U", $переменная)\}}

## Как обрезать часть строки:

\{{ substr($Переменная, 0, 3) \}}

где: 0 - номер символа с которого начать обрезание строки (важно! нумерация начинается с нуля, т.е. 0 - первый символ, 1 - второй символ, 2 - третий символ и т. д.); 3 - количество сиволов, которое нужно оставить в строке;

Например в переменной $Строка записано значение "abcdef"&#x20;

\{{ substr($Строка, 0, 3) \}} -> abc&#x20;

\{{ substr($Строка, 1, 2) \}} -> bc&#x20;

\{{ substr($Строка, 3) \}} -> def&#x20;

\{{ substr($Строка, -1, 1) \}} -> f&#x20;

\{{ substr($Строка, -2, 1) \}} -> e

С помощью этого решения можно, например, вырезать часть номера телефона, если он сохранён в переменной.

## Другое

#### abs - абсолютное значение (модуль числа)

* \{{ abs(-100) \}} – преобразует в положительное число 100
* \{{ abs($число) \}} – преобразует число содержащееся в переменной «число» в положительное число

#### ceil - округление дроби в большую сторону

* \{{ ceil(1.2) \}} – преобразует в целое число 2
* \{{ ceil($число) \}} – преобразует число содержащееся в переменной «число» в целое число

#### floor - округление дроби в меньшую сторону

* \{{ floor(1.9) \}} – преобразует в целое число 1
* \{{ floor($число) \}} – преобразует число содержащееся в переменной «число» в целое число c округлением в меньшую сторону

#### max – поиск набольшего числа

* \{{ max(1, 5) \}} – вернет число 5
* \{{ max(1, 5, 100, 4) \}} – вернет число 100
* \{{ max($число1, $число2, $число3) \}} – вернет наибольшее число содержащееся в переменных «число1», «число2», «число3»
* \{{ max($число1, $число2, 100, 200) \}} – микс параметров, можно передавать «неограниченное» количество чисел и переменных

#### min – поиск наименьшего числа

* \{{ min(1, 5) \}} – вернет число 1
* \{{ min(1, 5, 100, 4) \}} – вернет число 1
* \{{ min($число1, $число2, $число3) \}} – вернет наименьшее число содержащееся в переменных «число1», «число2», «число3»
* \{{ min($число1, $число2, 100, 200) \}} – микс параметров, можно передавать «неограниченное» количество чисел и переменных

#### pow – возведение в степень

* \{{ pow(2, 2) \}} – два в квадрате, вернет число 4
* \{{ pow(2, 3) \}} – два в кубе, вернет число 8
* \{{ pow(2) \}} – два в нулевой степени, вернет число 1
* \{{ pow(($число, $степень) \}} – возведет число содержащееся в переменной «число» в степерь содержащейся в переменной «степень»
* \{{ pow($число, 10) \}} – микс параметров

#### round – округление числа

* \{{ round(1.123456789, 1) \}} – округлит число до 1.1
* \{{ round(1.123456789, 2) \}} – округлит число до 1.12
* \{{ round(1.123456789, 5) \}} – округлит число до 1.12345
* \{{ round(1.49) \}} – округлит число до 1
* \{{ round(1.5) \}} – округлит число до 2
* \{{ round($число, $точность) \}} – округлит число содержащееся в переменной «число» с точностью содержащееся в переменной «точность»
* \{{ round(1.123456789, $точность) \}} – микс праметров

#### sqrt – квадратный корень

* \{{ sqrt(4) \}} – вернет 2
* \{{ sqrt(100) \}} – вернет 10
* \{{ sqrt(200) \}} – вернет 14.142135623731
* \{{ sqrt($число) \}} – вычислит квадратный корень из числа содержащегося в переменной «число»

### Генератор случайных чисел и строк

#### &#x20;Сгенерировать случайное число - `{{ rand() }}`&#x20;

#### Сгенерировать случайное число от 5 до 100: `{{ rand(5, 100) }}`

#### Сгенерировать случайную строку -`{{ strRandom() }}`&#x20;

#### Сгенерировать случайную строку длинной 20 символов: `{{ strRandom(20) }}`

#### &#x20;Сгенерировать случайную строку длинной 20 символов заглавными буквами: `{{ strRandom(20, true) }}`

#### **`Сгенерировать случайную фразу -` \{{ randomText("a", "b", "c") \}}**

### Сообщение для определенного мессенджера

#### `{{ messageToTelegram("Сообщение") }}` - Сообщение в Telegram

Пример: `{{ messageToTelegram("Это сообщение отобразится только в Telegram") }}`

#### `{{ messageToViber("Сообщение") }}` - Сообщение в Viber

Пример: `{{ messageToViber("Это сообщение отобразится только в Viber") }}`

#### `{{ messageToWhatsApp("Сообщение") }}` - Сообщение в WhatsApp

Пример: `{{ messageToWhatsApp("Это сообщение отобразится только в WhatsApp") }}`

#### [`{{ messageToFacebook("Сообщение") }}`](#user-content-fn-1)[^1] - Сообщение в Facebook

Пример: `{{ messageToFacebook("Это сообщение отобразится только в Facebook") }}`

#### `{{ messageToIcq("Сообщение") }}` - Сообщение в ICQ

Пример: `{{ messageToIcq("Это сообщение отобразится только в ICQ") }}`

### Счета

#### `{{ getBalance("`_`Код валюты`_`") }}` - Получить баланс контакта&#x20;

В рублях: `{{ getBalance("RUB") }}`

В долларах: `{{ getBalance("USD") }}`



#### `{{` getCartAmount() `}}` – выводит общую стоимость товаров в корзине





[^1]: 