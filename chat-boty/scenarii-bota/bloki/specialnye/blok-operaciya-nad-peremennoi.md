# Операция над переменной

Способ записать произвольное значение в переменную с возможностью произвести вычисление перед записью. Это отлично подходит для создания тестов или викторин.

![](../../../../.gitbook/assets/AOsdBWvfla8.jpg)

При попадании в этот блок выполняется операция над переменной и сразу же происходит перенаправление пользователя в следующий блок по связи.

На данный момент можно выбрать два типа операции:

* Произвольное значение
* Математическое выражение

#### Произвольное значение

Простая операция, которая записывает указанное значение в указанную переменную.

#### Математическое выражение

Вы можете задать произвольное математическое выражение с простыми арифметическими операциями.

![](../../../../.gitbook/assets/ihGY3nNHZYA.jpg)

В выражении можно оперировать с текущей переменной, для этого ее имя всегда должно быть `x`, т.е. в данном примере `x` равен значению переменной «Балл».

Выражение `x + 1` означает, что к значению переменной «Балл» прибавится единица, а результат вычисления запишется в переменную «Балл».&#x20;

Это отлично подходит для тестов или викторин, просто ставьте этот блок между ответом и следующим вопросом, и за каждый вопрос начисляйте какой-то балл, а в конце теста вы можете вывести результат в блоке «Простое сообщение» или «Цепочка сообщений». Так же эта переменная будет присутствовать при выгрузке данных их бота в Excel.

Также с помощью этого блока возможно записывать локальную переменную в глобальную. В произвольном выражении можно использовать автоподстановку (переменные, функции и т.д.). В значение/выражение записывается пользовательская переменная и она записывается в глобальную если указать тип результирующей переменной "глобальная".&#x20;

![](../../../../.gitbook/assets/1й.png)



## Запись локальной переменной в глобальную с помощью блока «Операция над переменной»

Теперь с помощью этого блока возможно записывать локальную переменную в глобальную. В произвольном выражении можно использовать автоподстановку (переменные, функции и т.д.). В значение/выражение записывается пользовательская переменная и она записывается в глобальную если указать тип результирующей переменной "глобальная".

![](<../../../../.gitbook/assets/01 (1).png>)

{% embed url="https://www.youtube.com/watch?v=r7mlwupi4Y4" %}

\


{% embed url="https://www.youtube.com/watch?v=Qlz2gU--ROs" %}

{% embed url="https://www.youtube.com/watch?t=212s&v=B7Wf1Yy_W7M" %}

{% embed url="https://www.youtube.com/watch?v=Go2IjfpKApc" %}

{% embed url="https://www.youtube.com/watch?t=3s&v=W0AEEONZ-fo" %}
