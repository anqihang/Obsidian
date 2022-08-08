# [[MySql]]

```javascript
#安装包
	npm install mysql2
#设置配置
	const db = mysql.createpool({
		host:'127.0.0.1',
		user:'root',
		password:'123456789',
		database:'',
		connectionLimit:10,//最大链接数
		
	})
```