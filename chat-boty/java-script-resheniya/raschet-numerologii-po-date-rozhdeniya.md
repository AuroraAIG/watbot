# Расчет нумерологии по дате рождения

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
