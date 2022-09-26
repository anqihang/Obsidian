# [[MySql|mysql]]

```javascript
#安装包
	npm install mysql2
#设置配置
	const mysql = require('mysql2');
	const db = mysql.createpool({
		host:'127.0.0.1',
		user:'root',
		password:'123456789',
		database:'',
		connectionLimit:10,//最大链接数		
	})
```

# express

```javascript
#安装包
	npm install express
#设置
	const express = require('express')
	const app = express()
	app.get(url,(request,response)=>{
		response.setHeader('Access-Control-Allow-Origin','*')
		response.send();
	})
	app.listener(post,()=>{
		console.log("服务已启动，post端口监听中......")
	})
```

# fs

```javascript
const fs = require('fs');
fs.readFile(path[,options],callback)
fs.writeFile(path,data[,option],callback)
```

# http
```js

```