---
title: Node.js
localeTitle: Node.js
---
## Node.js

Node.js - это среда выполнения JavaScript, встроенная в движок JavaScript V8 от Chrome. Node.js использует управляемую событиями, неблокирующую модель ввода-вывода, которая делает ее легкой и эффективной. Пакетная экосистема Node.js, npm, является самой большой экосистемой библиотек с открытым исходным кодом в мире.

#### Давайте сломаем его.

*   Среда выполнения Javascript построена на движке JavaScript V8 от Chrome.  
    В каждом браузере встроен движок JavaSript для обработки файлов JavaScript, содержащихся на веб-сайтах. Google Chrome использует движок V8, который построен на C ++. Node.js также использует этот сверхбыстрый движок для интерпретации файлов JavaScript.
*   Node.js использует управляемую событиями модель.  
    Это означает, что Node.js ждет определенных событий. Затем он действует на эти события. События могут быть любыми: от клика до HTTP-запроса. Мы также можем объявить наши собственные события и заставить node.js прослушивать эти события.
*   Node.js использует неблокирующую модель ввода-вывода.  
    Мы знаем, что задачи ввода-вывода занимают гораздо больше времени, чем задачи обработки. Node.js использует функции обратного вызова для обработки таких запросов.

Предположим, что для выполнения конкретной задачи ввода-вывода требуется 5 секунд. И мы хотим выполнить этот ввод-вывод дважды в нашем коде.

**питон**

```python
import time 
 
 def my_io_task(): 
  time.sleep(5) 
  print("done") 
 
 my_io_task() 
 my_io_task() 
```

**Node.js**

```js
function my_io_task() { 
    setTimeout(function() { 
      console.log('done'); 
    }, 5000); 
 } 
 
 my_io_task(); 
 my_io_task(); 
```

Оба выглядят одинаково, но время, затраченное на выполнение, отличается. Код python занимает 10 секунд, пока код Node.js занимает всего 5 секунд.

Node.js занимает меньше времени из-за своей неблокирующей модели ввода-вывода. Первый вызов `my_io_task()` запускает таймер и оставляет его там. Он не ждет ответа от функции, вместо этого он переходит к вызову второй `my_io_task()` , запускает таймер и оставляет его там.

Когда таймер завершает выполнение, занимает 5 секунд, он вызывает функцию и `done` печать на консоли. Поскольку оба таймера запускаются вместе, они завершаются вместе и, следовательно, занимают одинаковое количество времени.

#### Дополнительная информация:

*   [Официальный сайт NodeJS](https://nodejs.org)
*   [Менеджер версий узлов](https://github.com/creationix/nvm/blob/master/README.md)
*   [n: Интерактивный менеджер версий NodeJS](https://github.com/tj/n)