node-list-cycler
================

Infinity cycle through list

Install:
--------

```npm install list-cycler```

Examples:
---------

Iterate from beginning of list:
```javascript
var cycler = require("list-cycler"),
    colors = cycler(['red', 'green', 'blue']),
    color,
    i=6;
while (--i) {
    color = colors.next();
    console.log(i + '. <span color="' + color + '">' + color + '</span>');
}
```

If should start from index other then 0 - here iterate
from index 1 (letter 's') - look at second argument to *cycler*:
```javascript
var cycler = require('list-cycler'),
    my_list = cycler(['a', 's', 'd'], 1),
    my_condition = true;

while (my_condition) {
    console.log(my_list.next());
    my_condition = Math.random() < 0.9;
}
```
