# Преобразовать время из Unix в формат d.m.Y

```javascript
var переменная = getContactVariable("watbot"); // Unix timestamp
var date = new Date(переменная * 1000); // Умножаем на 1000, чтобы преобразовать секунды в миллисекунды
var formattedDate = date.getFullYear() + '-' + ('0' + (date.getMonth()+1)).slice(-2) + '-' + ('0' + date.getDate()).slice(-2) + ' ' + ('0' + date.getHours()).slice(-2) + ':' + ('0' + date.getMinutes()).slice(-2) + ':' + ('0' + date.getSeconds()).slice(-2);
console.log(formattedDate); // Выводим дату и время в формате `YYYY-MM-DD HH:mm:ss`
sendMessage(formattedDate);
```
