---
title: Vue.js条件与循环
date: 2019-08-08 16:43:37
tags:
---

#### 条件判断

```
v-if
	条件判断使用v-if
	
v-else
	可以使用v-else指令给v-if添加一个"else"块

v-else-if 
	v-else-if在2.1.0新增,顾名思义,用作v-if的else-if块.可以链式的多次使用

v-else 、v-else-if 必须跟在 v-if 或者 v-else-if之后。

v-show
	我们也可以使用 v-show 指令来根据条件展示元素：
	<h1 v-show="ok">Hello!</h1>
```

#### 循环语句

```
v-for
	v-for指令需要以site in sites 形式的特殊语法,sites是源数据数组并且site是数组元素迭代的别名
	
	v-for可以绑定数据到数组来渲染一个列表
	
	v-for迭代对象
		可以通过一个对象的属性来迭代数据
		提供第二个的参数为键名
		第三个参数为索引
			<li v-for="(value, key, index) in object">
     			{{ index }}. {{ key }} : {{ value }}
    		</li>
    		<script>
                new Vue({
                  el: '#app',
                  data: {
                    object: {
                      name: 'dsy',
                      url: 'http://www.111.com',
                    }
                  }
                })
             </script>
             
	v-for 迭代整数
		v-for 也可以循环整数
		<div id="app">
  			<ul>
    			<li v-for="n in 10">
     				{{ n }}
    			</li>
  			</ul>
		</div>
```

