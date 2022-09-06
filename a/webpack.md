# webpack
- 初始化npm，下载包
```
	npm init -y	
	npm install webpack webpack-cli --save-dev
#
	npm install --save-dev[-D]  webpack-dev-server
	npx webpack serve
```

###### 概念
- 入口ntry
```js
entry: './src/main.js'
entry:{                       //多入口
	app:'./src/app.js',
	main:'./src/main.js'
}
```

- 出口otput
```js
output:{
	path:path.resolve(__dirname,'dist'),
	filename:'amin.js',
	chunkFilename:''
	clean:true,
}
```

- loader #loader自下向上执行
```js
module:{ 
	rules:[
		{
		enforce:pre|normal|inline|post
			test://,
			use:[],
			generator:{
				filename:'static/images/[hash][ext][query]',//图片模块打包的路径
			}
		}
	]
}
```

- 插件plugins
```js
plugins:[
	new ESLintPlugin(options),new HtmlWebpackPlugin()
]
```

- 模式 
```js
mode:'development'|'production'
```

- devtool
```js
devtool:''//错误位置检测

```

- devserver
```js
devsserve:{
	hot:true,//热模块
	host:'localhost'
}
```

###### 模块
| 名字         | 功能 |
| ------------ | ---- |
| ts.loader    |      |
| less.loader  |      |
| css.loader   |      |
| style.loader |      |
| asset        |      |

