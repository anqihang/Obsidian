# 指令

```javascript
#内置
	v-bind#:&&单向绑定
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
```

# API

```javascript

Vue.set(target,key,value)[不能在实例对象和根属性上添加]
```

# 方法

```javascript
vm.$set()
```

# 生命周期

```javascript
beforeCreate
created
#
beforeMout
mouted
#
beforeUpdate
updated
#
beforeDestory
destoryed
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
	 }
})
//
const v = Vue.extend({
	template:'',
})
```