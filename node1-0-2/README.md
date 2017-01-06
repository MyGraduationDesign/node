# node.js 回调函数

## 阻塞代码实例(在文件读取完后才执行完程序)
- main.js
```
    var fs = require("fs");

    var data = fs.readFileSync('input.txt');

    console.log(data.toString());
    console.log("程序执行结束!");
```
## 非阻塞代码实例(不需要按顺序)
- main01.js
```
    var fs = require("fs");

    fs.readFile('input.txt', function (err, data) {
        if (err) return console.error(err);
        console.log(data.toString());
    });

    console.log("程序执行结束!");
```
