# node.js �ص�����
-----------
## ��������ʵ��(���ļ���ȡ����ִ�������)
- input.txt

```����̳̹�����ַ��www.runoob.com```

- main.js

```
var fs = require("fs");

var data = fs.readFileSync('input.txt');

console.log(data.toString());
console.log("����ִ�н���!");
```

## ����������ʵ��(����Ҫ��˳��)
- input.txt

```����̳̹�����ַ��www.runoob.com```

- main01.js

```
var fs = require("fs");

fs.readFile('input.txt', function (err, data) {
    if (err) return console.error(err);
    console.log(data.toString());
});

console.log("����ִ�н���!");
```