---
description: >-
  Если вам нужно брать только короткие значения длинных текстов из
  Google-таблицы можно это сделать 3 строчками а блоке интерпретатор Javascript
---

# Обрезание строчки из гугл таблицы

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-29 в 00.11.48.png" alt=""><figcaption><p>Начальный текст в Google таблице</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-29 в 00.07.25.png" alt=""><figcaption><p>Блок чтения записей из Google таблицы который сохраняет текст в переменную long</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-29 в 00.07.32.png" alt=""><figcaption><p>Блок интерпретатор JavaScript который обрезает значение переменной long</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2024-06-29 в 00.07.43.png" alt=""><figcaption><p>Блок Цепочка сообщений для вывода новой переменной short</p></figcaption></figure>

А вот и сам текст

```
//Записываем переменную long во временную переменную
var long = getContactVariable("long");
//С помощью функции substr достаем первые 100 символов и сохраняем во временную переменную
var short = long.substr(0, 100);
//сохраняем значение временной переменной в локальную переменную пользователя
setContactVariable("short", short);
```

