# Сравнение переменных и вывод наибольшего значения.

```javascript
// Получаем значения переменных
var a = parseFloat(getContactVariable("а"));
var b = parseFloat(getContactVariable("б"));
var v = parseFloat(getContactVariable("в"));

// Вычисляем максимальное значение
var max = Math.max(a, b, v);

// Сохраняем результат в переменную
setContactVariable("максимум", max);

```

