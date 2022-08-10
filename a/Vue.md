
# 指令

```
v-bind#:&&单向绑定
v-model&&双向绑定
v-once
v-html
v-
```

```javascript
#html
<div id='root'>
	{{name}}//插值
	<a :href="url"></a>//v-bind:href="url"
</div>

const vm = new Vue({
	el:'#root' ----> vm.$mount("#root")
	data:{     ----> data:function(){return {name:""}}
		name:''
		url:''
	}
})
```