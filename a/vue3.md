# 创建

```
#组合式API
	- ref/reactive
	- h
	- computed
	- watch/watchEffect
	- on生命周期
	- shallowRef/shallowReactive&[浅层代理]
	- toRef          [将对象的属性设置别名]
	- toRefs         [将对象的所有属性设置别名]
	- readonly        [深层只读]
	- shallowReadonly [浅层只读]
	- toRaw           [响应式转换成普通式]
	- markRow         [给代理对象添加一个普通数据]
	- customRef       [自定义ref]
	- provide
	- inject
	- isRef
	- isProxy
	- isReactive
	- isReadonly
	- defineAsyncComponent
```

## 生命周期

```
- beaforeCreate [不是组合式API]
- created       [不是组合式API]
- beforeMount
- mounted
- beforeUpdate
- updated
- beforeUnmount
- unmounted
```


## setup

```js
import {h} from 'vue'
props:[],
setup(props,context){
	let name=''
	function a(){}
	return {
		name,
		a,
	}
	#
	return ()=>{return h('h1','anqihang')}
}
######
<script setup>
</script>
```

## ref/reactive函数

```js
import {ref,reactive} from 'vue'
	let name =ref('')
	修改用name.value#$ref则不需要.value[实验性的]
	复杂类型不需要第二个value[对象]
	reactive(obj)//不能设置简单类型包装成proxy类型
############################
toRef()/toRefs()#将 响应对象的属性进行别名设置
shadowRef()#只处理基本类型响应
shadowReactive()#只处理浅层的数据响应
```

## computed 计算属性

```js
import {computed} from 'vue'
setup(){
	let computed = computed(()=>{
		return a+b;
	})
}
```

## watch/watchEffect

```Markdown
#
	immediate&直接执行,deep&深层,flush&读取的是更新后的dom
	
watch(a,(newv,oldv)=>{},{immediate:true})
	#reactive参数的oldv==newv,是深度监视，对象不是深度
	[a,b]|()=>{a.c}#监视多个或某个属性&&ref对象需要.value
watchEffect不需要元数据，依赖于回调函数中所有数据的变化，立即执行
```

## hooks

```js
import {ref}from 'vue'
export default function(){
	let a=ref(0)
	let b =function(){}
	return {a,b}
}
```

## 自定义ref

```js
funcrion myref(value){
	return customRef((track,trigger)=>{
		return {
			get(){
				track()//追踪数据的更改
			}，
			set(newValue){
				value = newValue;
				trigger()//重新解析模板
			}
		}
	})
}
```

## 依赖注入

```js
provide('key',value)
inject('key')
```

`<fragment>`&类似vue2的最外部包含标签
`<teleport>`&控制标签内容在那个
`<Suspent>`&控制延迟显示的标签的暂时替代显示【实验性的】

# vite创建项目

安装脚手架工具（安装并执行create-vue)
`npm init vue@last`   

安装依赖并开启服务器
```
> cd <your-project-name>
> npm install
> npm run dev
```

# router

```js
app.use(router);
cosnt router = VueRouter.createRouter({
	history:VueRouter.createWebHistory(),
	routes:[]
})
```

```js
//模板中可以使用$router\$route，所以setup不需要返回
const router = useRouter();
const route = userRoute();

```

# mitt全局事件总线

```js
#install
	npm install mitt
#useg
	import 
```