安装
	`npm install -g typescript`

转换成js
	`tsc [name.ts] [name.ts]`
	tsc --init  
| 指令 | 功能 |
| ---- | ---- |
| -w   | 监听 | 

类型
`boolean\number\string\number[]|Array<number>\object|{}\元组[number,string]\枚举enum、任意值any\void没返回值\never\ReadonlyArray<T>`  
类型断言#`<number>name//name as string`  
type a=[] #别名 //let i=a;

声明
	`var [变量名]:[类型]=[值]`
	`function(a:[类型，b?:[类型]= 值):[返回值类型]{return }`##问号是可选`...c:number[]`
	构造函数 `new function(a,b,'return ')`  
	
重载
```ts
重载签名
	function name(a:number,b:string):string;
	function name(a:string,b:number):string[];
实现签名
	function name(a:any,b:any):void{console.log(a,b)}
```

联合类型
```ts
let a:number|string =0
```

接口(规定必须有接口的属性)
```ts
interface name {
	readonly key:string,
	[key:number:string],
	(source:string):number,//函数，函数参数可以不匹配
}

类使用接口
	class cla implements name{}
```

继承
`interface person extends name[,name1]{age:number}` 

任意属性
`var oo: { num: number; [propName: string]: unknown };`

元组
`let aa: [string, number];`

命名空间  #可嵌套
```ts
namespaced SpaceName{
	export interface ID {id:number}
	export class person{name:string}
}
引用
	SpaceName.ID#同一文件
	///《reference path= '文件名称' />#另一个文件
```

泛类-类型不明确时使用-在执行的时候确定
```ts
function fn2<T>(a: T): T {
  return a;
}
```

枚举
```ts
enum Gender {
  male,
  female,
} //{male=1}默认从0
let i: { name: string; gender: Gender };
i = { name: "an", gender: Gender.male };
```

抽象类，做继承父类的，不可实例
```ts
abstract class person {
  //抽象方法，没有方法体,子类必须重写
  abstract show(): void;
}
```

declare


stype