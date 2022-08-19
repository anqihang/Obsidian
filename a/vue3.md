# 创建

```
import {h} from 'vue'
setup(){
	let name=''
	function a(){}
	return {
		name,
		a,
	}
	#
	return ()=>{return h('h1','anqihang')}
}
```
## ref函数
```
	let name =ref('')
	修改用name.value
```