vue+vite
```js
npm install bootstrap
main.js{
	// Import our custom CSS
	import "./assets/styles.scss";
	// Import all of Bootstrap's JS
	import * as bootstrap from "bootstrap";
}
新建
styles.scss{
	// Import all of Bootstrap's CSS
	@import "~bootstrap/scss/bootstrap";
	/
	@import 'node_modules/bootstrap/scss/bootstrap';
}
```
### breakpoint
| Breakpoint        | Class infix | Dimensions |
| ----------------- | ----------- | ---------- |
| small             | sm          | >=576px    |
| medium            | md          | >=768      |
| large             | lg          | >=992      |
| extra large       | xl          | >=1200     |
| extra extra large | xxl         | >=1400     |
| fluid             |             |            |
	

|                                              | 功能 |
| -------------------------------------------- | ---- |
| container[-breakpoint]                       |      |
| row[-cols-1]                                 | 列数 |
| col[-breakpoint][-1]                         |      |
| align-items-[start/end/center]               |      |
| align-self-[start/end/center]                |      |
| justify-content-[start/end/center/around...] |      |
| order-1                                      |      |
| offset[-breakpoint][-1]                      |      |
| g/gx/gy-1                                    |      |
| grid                                         |      |
| g-col-1                                      |      |
| --bs-rows                                    | 行数 |
| --bs-columns                                 | 列数 |
| --bs-gap                                     | 间隙 |
| offcanvas                                    |      |
