
## Code乌托邦

### 1.工作制度
。。。<待续>。。。

### 2.代码制度  

1.`缩进一律2个空格。一行不超过120个字符`  
2.`变量全部用let和const ,尽量都在顶部声明，如果必须设置全局变量或者常量，书写规则全部大写，设置在独立的代码块中。`    

3.`结束必须以分号做结尾`  
4.`字符串一律用单引号，字符串拼接一律用模板`  

5.`构造函数名开头大写`  
6.`所定义的变量 尽量都要写在头部，就算后面才会赋值，也可以在头部先声明，除非作用域不一样`  
7.`避免隐式类型转换,使用===代替==，!==代替!=`  
8.`所有的操作符和操作对象前后都要有空格`  


9.`在函数中，通过 flag 的 true 或 false，来判断执行逻辑，违反了一个函数干一件事的原则。`

```
10.
**大驼峰与小驼峰  
css命名 参考(http://www.zhangxinxu.com/wordpress/2010/09/精简高效的css命名准则方法/)
```
11.`使用字面量语法创建引用对象,尽量使用函数表达式而不是函数声明，容易作用域提升
`  
12.`在同一个数组内不许放入不同类型的对象`  
13.`将通用的代码封装成Function`  
14.`避免使用delete关键字，这会对V8的性能有影响，可以用null代替。`  
15.`当某些对象具有相同的属性的时候，尽可能的为他们创建一个构造函数，这样V8的性能会有所提升`  
16.`尽量用forEach代替for，避免使用for-in,如果对数组中的值做操作的画，尽可能的使用map`  

```
17.
在async/await中，视情况使用Promise.all 例如：：
// bad
async function someAsyncFunc() {
    const user = await asyncGetUser();
    const categories = await asyncGetCategories();
    const mapping = await asyncMapUserWithCategory(user, categories);
}
 
// good
async function someAsyncFunc() {
    const [user, categories] = await Promise.all([
        asyncGetUser(),
        asyncGetCategories()
    ]);
    const mapping = await asyncMapUserWithCategory(user, categories);
}
没必要的串行变成并行
```
18.`函数使用默认参数语法，并且将默认参数放在最后边`  
19.`不要改变函数的参数`
20.`枚举变量，枚举的属性一律全部大写，单词之间使用下划线`  
21.`boolean 类型的变量使用 is 或 has 开头`  
22.`基本类型检测优先使用typeof,引用类型检测优先使用instanceof`  
23.`不允许修改和扩展任何原生对象和宿主对象的原型。`

<待续>


### 3.交流制度  
。。。<待续>。。。



#### PS：有些规则借鉴了Airbnb和Google的风格，这里放上资源，因人而异。后两个资源也不错，也可以参考！
https://github.com/airbnb/javascript  
https://google.github.io/styleguide/jsguide.html  
https://github.com/standard/standard/blob/master/docs/README-zhcn.md
https://github.com/rwaldron/idiomatic.js/tree/master/translations/zh_CN