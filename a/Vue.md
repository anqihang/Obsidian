# 创建

```js
npm install @vue/cli
vue create <your project name>
cd <your project name>
npm run serve
```

# 指令

```javascript
#内置
	v-bind/:&&单向绑定
	v-model&&双向绑定
	v-once
	v-html
	v-on#@&&事件
	v-show
	v-if
	v-else-if
	v-else
	v-for
	v-text
	v-cloak
	v-solt/#&&插槽
	v-pre&&跳过
#自定义
	directives:{
	  big:{
	  }
	}
```

# 事件/按键修饰符

```
.stop     == stopPropagation
.prevent  == preventDefault()
.capture  ==
.self     ==
.once     ==
.passive  ==
---
.enter
.tab
.delete
.esc
.space
.up
.down
.left
.right
.ctrl
.alt
.shift
.meta
.middle
.exact
#自定义事件
	
vc.$emit(vc.parent.event)&&触发父组件的方法
vc.$off([vc.parent.evet,vc.parent.event])&&解绑多个事件，没有参数解绑所有事件,原生加.native
```

# API

```javascript

Vue.set(target,key,value)[不能在实例对象和根属性上添加]
Vue.mixin
```

# 方法

```javascript
vm.$set()
vm.$on
vm.$mouted
vm.$destory
vm.$nextTick
```

# 生命周期

```javascript
beforeCreate
created
#
beforeMount
mounted
#
beforeUpdate
updated
#
beforeDestory
destoryed
#路由钩子
activated
deactivated
```

# 属性

```javascript
$refs#ref=''&&绑定的dom
```

# 配置项

```Markdown
el#模板
data#数据
computed#计算数据
methods#方法
watch#监视
filters#过滤
directives#自定义指令
components#组件
props#标签属性
mixins#混合
```

# 动画

```
<transition appear>
	<div>a</div>
</transition>
```

# 插槽

```Markdown
<vc>
	<img/>
</vc>
-----[默认插槽]
vc#<template>
<slot>默认值</slot>##被img标签替代
</template>
-----[具名插槽]
<template v-slot:fir>
</template>
vc#
<slot name="fir"></slot>
-----[作用域插槽]
<template v-slot="new">
{{new.v}}
</template>
vc#
<slot :v='data.b'></slot>
```

# 全局事件总线

```
vue.property.$bus=this
```

# 实例

```javascript
#html
<div id='root'>
	{{name}}//插值
	<a :href="url"></a>//v-bind:href="url"
	<button v-on:'show(1,$event)'></div>
	<div>{{name | fil('str')}} | fli1</ div>

const vm = new Vue({
	el:'#root' ----> vm.$mount("#root")
	data:{     ----> data:function(){return {name:""}}
		name:''
		url:''
	}
	computed:{
	
	}，
	methods:{
		show(a,event){}
	},
	watch:{
		ishot:{             ---->ishot(newv,oldv){}
			hander(newv,oldv){}
		}
	}，
	filters:{     ----------->Vue.filter('',function(){})(全局)
	 fil(base,str){
		 return
	 }
	 },
	 directives:{
		 big:{         --------->big(element,binding){}
		 bind(){},
		 insert(){},
		 update(){}
		 }
	 },
	 components:{
		 a:v;
	 },
	 props:[],
})
//
const v = Vue.extend({---》{}
	template:'',
})
```

# vuex #2中只能用@3

```javascript
import vue from 'vue'
import vuex from 'vuex'
vue.use(vuex)
const actions={}
const mutations={}
const state={}
const getters={}#结果会被缓存
export default new vuex.Store{
	actions,
	mutations,
	state,
	getters,
}
```

## mapState

```javascript
import {mapState,mapGetters,mapMutations,mapActions} from 'vuex'
mapState({'name':'state.value'})[object]
mapState([state.value])
mapGetters()
//
mapMutations({name:'mutations.value'})
//
this.$store.state.namepace.key
this.$store.getter[namespace/key]
this.$store.commit('namespace.method',value)
this.$store.dispatch('namespace.method',value)
```

# vue-router #2中用@3

```javascript
import router from 'vue-router';
import a from './components/a'
const router = new router({
	routers:[
	{
		path:'/a',
		component:a,
		children:[
		{
			path:'new',
			compontent:New,
		}]
	}
	]
});
```

```html
<router-link to='/a' active-class=''></router-link>
<router-view></router-view>
#属性
active-class=''#路由激活时应用css
replace#开启网页历史替代
```

## 路由传参

```
query
	#:to="`/a?id=${}&title=${}`"
	#:to="{path:'/a',query:{id=,title=}}"
	$this.$route.query.id
```

## 路由守卫

```
router.beforeEach((to,from,next)=>{
	next()
})
```