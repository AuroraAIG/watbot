---
description: >-
  В этом разделе будут размещаться Javascript решения для блока HTTP-запрос,
  которые помогут справится с нестандартными задачам
---

# Javascript решения

## Пример кода передачи файла на сторонний сервер:

```javascript
var fileUrl = "https://example.com/path/to/file.jpeg";
var xhr = new XMLHttpRequest();
xhr.open("POST", "/upload", true);
var formData = new FormData();
formData.append("file", fileUrl);

xhr.setRequestHeader("Content-Type", "multipart/form-data");
xhr.onload = function() {
  if (xhr.status === 200) {
    console.log("Файл успешно отправлен");
  } else {
    console.log("Ошибка отправки файла");
  }
};
xhr.send(formData);
```

## Пример кода для расчётов по дате рождения&#x20;

URL для блока HTTP-запрос: [https://watbot.ru/api/v1/getMe?api\_token=\{{Ключ\}}](https://watbot.ru/api/v1/getMe?api\_token=\{\{%D0%9A%D0%BB%D1%8E%D1%87\}})

```javascript
var yearBirth = getContactVariable("Дата");
var year = yearBirth.substring(yearBirth.length - 4);
function digit (number) {
  var figures = "" + number
  var sum = 0

  for (var i = 0; i < figures.length; i++) 
    sum += +figures[i]

  return sum
}
year = digit(year);
if(year > 22){
  year = digit(year);
}
setContactVariable("Энергия", year) 
```

## Пример кода для бота с каталогом в кнопках

Для первого блока HTTP

```javascript
for (i = 1; i <= 100; i++) {
 deleteContactVariable("Кнопка "+i);
};
```

Для второго блока HTTP

```javascript
var total = response.data.meta.total;

for (i = 1; i <= total; i++) {
 var tovar = response.data.data[i-1].nazvanie;
 var cena = response.data.data[i-1].cena;
 setContactVariable("Кнопка "+i,
 tovar+" | "+cena+" ₽");
};
```

Для третьего блока HTTP

```javascript
var vibor = getContactVariable("выбор");
vibor = vibor.split(" |")[0];
setContactVariable("выбор", vibor);
```
