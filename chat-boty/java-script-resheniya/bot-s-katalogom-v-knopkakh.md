# Бот с каталогом в кнопках

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
