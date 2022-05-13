##  JavaScript 面试知识点总结

本部分主要是笔者在复习 JavaScript 相关知识和一些相关面试题时所做的笔记，如果出现错误，希望大家指出！

### 目录

- [1. 介绍 js 的基本数据类型。](#1-介绍-js-的基本数据类型)
- [2. JavaScript 有几种类型的值？你能画一下他们的内存图吗？](#2-javascript-有几种类型的值你能画一下他们的内存图吗)
- [3. 什么是堆？什么是栈？它们之间有什么区别和联系？](#3-什么是堆什么是栈它们之间有什么区别和联系)
- [4. 内部属性 Class 是什么？](#4-内部属性-class-是什么)
- [5. 介绍 js 有哪些内置对象？](#5-介绍-js-有哪些内置对象)
- [6. undefined 与 undeclared 的区别？](#6-undefined-与-undeclared-的区别)
- [7. null 和 undefined 的区别？](#7-null-和-undefined-的区别)
- [8. 如何获取安全的 undefined 值？](#8-如何获取安全的-undefined-值)
- [9. 说几条写 JavaScript 的基本规范？](#9-说几条写-javascript-的基本规范)
- [10. JavaScript 原型，原型链？ 有什么特点？](#10-javascript-原型原型链-有什么特点)
- [11. js 获取原型的方法？](#11-js-获取原型的方法)
- [12. 在 js 中不同进制数字的表示方式](#12-在-js-中不同进制数字的表示方式)
- [13. js 中整数的安全范围是多少？](#13-js-中整数的安全范围是多少)
- [14. typeof NaN 的结果是什么？](#14-typeof-nan-的结果是什么)
- [15. isNaN 和 Number.isNaN 函数的区别？](#15-isnan-和-numberisnan-函数的区别)
- [16. Array 构造函数只有一个参数值时的表现？](#16-array-构造函数只有一个参数值时的表现)
- [17. 其他值到字符串的转换规则？](#17-其他值到字符串的转换规则)
- [18. 其他值到数字值的转换规则？](#18-其他值到数字值的转换规则)
- [19. 其他值到布尔类型的值的转换规则？](#19-其他值到布尔类型的值的转换规则)
- [20. {} 和 [] 的 valueOf 和 toString 的结果是什么？](#20--和--的-valueof-和-tostring-的结果是什么)
- [21. 什么是假值对象？](#21-什么是假值对象)
- [22. ~ 操作符的作用？](#22--操作符的作用)
- [23. 解析字符串中的数字和将字符串强制类型转换为数字的返回结果都是数字，它们之间的区别是什么？](#23-解析字符串中的数字和将字符串强制类型转换为数字的返回结果都是数字它们之间的区别是什么)
- [24. 操作符什么时候用于字符串的拼接？](#24--操作符什么时候用于字符串的拼接)
- [25. 什么情况下会发生布尔值的隐式强制类型转换？](#25-什么情况下会发生布尔值的隐式强制类型转换)
- [26. || 和 &amp;&amp; 操作符的返回值？](#26--和--操作符的返回值)
- [27. Symbol 值的强制类型转换？](#27-symbol-值的强制类型转换)
- [28. == 操作符的强制类型转换规则？](#28--操作符的强制类型转换规则)
- [29. 如何将字符串转化为数字，例如 '12.3b'?](#29-如何将字符串转化为数字例如-123b)
- [30. 如何将浮点数点左边的数每三位添加一个逗号，如 12000000.11 转化为『12,000,000.11』?](#30-如何将浮点数点左边的数每三位添加一个逗号如1200000011转化为1200000011)
- [31. 常用正则表达式](#31-常用正则表达式)
- [32. 生成随机数的各种方法？](#32-生成随机数的各种方法)
- [33. 如何实现数组的随机排序？](#33-如何实现数组的随机排序)
- [34. javascript 创建对象的几种方式？](#34-javascript-创建对象的几种方式)
- [35. JavaScript 继承的几种实现方式？](#35-javascript-继承的几种实现方式)
- [36. 寄生式组合继承的实现？](#36-寄生式组合继承的实现)
- [37. Javascript 的作用域链？](#37-javascript-的作用域链)
- [38. 谈谈 This 对象的理解。](#38-谈谈-this-对象的理解)
- [39. eval 是做什么的？](#39-eval-是做什么的)
- [40. 什么是 DOM 和 BOM？](#40-什么是-dom-和-bom)
- [41. 写一个通用的事件侦听器函数。](#41-写一个通用的事件侦听器函数)
- [42. 事件是什么？IE 与火狐的事件机制有什么区别？ 如何阻止冒泡？](#42-事件是什么ie-与火狐的事件机制有什么区别-如何阻止冒泡)
- [43. 三种事件模型是什么？](#43-三种事件模型是什么)
- [44. 事件委托是什么？](#44-事件委托是什么)
- [45. ["1", "2", "3"].map(parseInt) 答案是多少？](#45-1-2-3mapparseint-答案是多少)
- [46. 什么是闭包，为什么要用它？](#46-什么是闭包为什么要用它)
- [47. javascript 代码中的 "use strict"; 是什么意思 ? 使用它区别是什么？](#47-javascript-代码中的-use-strict-是什么意思--使用它区别是什么)
- [48. 如何判断一个对象是否属于某个类？](#48-如何判断一个对象是否属于某个类)
- [49. instanceof 的作用？](#49-instanceof-的作用)
- [50. new 操作符具体干了什么呢？如何实现？](#50-new-操作符具体干了什么呢如何实现)
- [51. Javascript 中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？](#51-javascript中有一个函数执行时对象查找时永远不会去查找原型这个函数是)
- [52. 对于 JSON 的了解？](#52-对于-json-的了解)
- [53. `[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})` 能解释一下这段代码的意思吗？](#53-foreachcallfunctionaastyleoutline1px-solid-mathrandom124tostring16-能解释一下这段代码的意思吗)
- [54. js 延迟加载的方式有哪些？](#54-js-延迟加载的方式有哪些)
- [55. Ajax 是什么? 如何创建一个 Ajax？](#55-ajax-是什么-如何创建一个ajax)
- [56. 谈一谈浏览器的缓存机制？](#56-谈一谈浏览器的缓存机制)
- [57. Ajax 解决浏览器缓存问题？](#57-ajax-解决浏览器缓存问题)
- [58. 同步和异步的区别？](#58-同步和异步的区别)
- [59. 什么是浏览器的同源政策？](#59-什么是浏览器的同源政策)
- [60. 如何解决跨域问题？](#60-如何解决跨域问题)
- [61. 服务器代理转发时，该如何处理 cookie？](#61-服务器代理转发时该如何处理-cookie)
- [62. 简单谈一下 cookie ？](#62-简单谈一下-cookie-)
- [63. 模块化开发怎么做？](#63-模块化开发怎么做)
- [64. js 的几种模块规范？](#64-js-的几种模块规范)
- [65. AMD 和 CMD 规范的区别？](#65-amd-和-cmd-规范的区别)
- [66. ES6 模块与 CommonJS 模块、AMD、CMD 的差异。](#66-es6-模块与-commonjs-模块amdcmd-的差异)
- [67. requireJS 的核心原理是什么？（如何动态加载的？如何避免多次加载的？如何 缓存的？）](#67-requirejs-的核心原理是什么如何动态加载的如何避免多次加载的如何-缓存的)
- [68. JS 模块加载器的轮子怎么造，也就是如何实现一个模块加载器？](#68-js-模块加载器的轮子怎么造也就是如何实现一个模块加载器)
- [69. ECMAScript6 怎么写 class，为什么会出现 class 这种东西?](#69-ecmascript6-怎么写-class为什么会出现-class-这种东西)
- [70. documen.write 和 innerHTML 的区别？](#70-documenwrite-和-innerhtml-的区别)
- [71. DOM 操作——怎样添加、移除、移动、复制、创建和查找节点？](#71-dom-操作怎样添加移除移动复制创建和查找节点)
- [72. innerHTML 与 outerHTML 的区别？](#72-innerhtml-与-outerhtml-的区别)
- [73. .call() 和 .apply() 的区别？](#73-call-和-apply-的区别)
- [74. JavaScript 类数组对象的定义？](#74-javascript-类数组对象的定义)
- [75. 数组和对象有哪些原生方法，列举一下？](#75-数组和对象有哪些原生方法列举一下)
- [76. 数组的 fill 方法？](#76-数组的-fill-方法)
- [77. [,,,] 的长度？](#77--的长度)
- [78. JavaScript 中的作用域与变量声明提升？](#78-javascript-中的作用域与变量声明提升)
- [79. 如何编写高性能的 Javascript ？](#79-如何编写高性能的-javascript-)
- [80. 简单介绍一下 V8 引擎的垃圾回收机制](#80-简单介绍一下-v8-引擎的垃圾回收机制)
- [81. 哪些操作会造成内存泄漏？](#81-哪些操作会造成内存泄漏)
- [82. 需求：实现一个页面操作不会整页刷新的网站，并且能在浏览器前进、后退时正确响应。给出你的技术实现方案？](#82-需求实现一个页面操作不会整页刷新的网站并且能在浏览器前进后退时正确响应给出你的技术实现方案)
- [83. 如何判断当前脚本运行在浏览器还是 node 环境中？（阿里）](#83-如何判断当前脚本运行在浏览器还是-node-环境中阿里)
- [84. 把 script 标签放在页面的最底部的 body 封闭之前和封闭之后有什么区别？浏览器会如何解析它们？](#84-把-script-标签放在页面的最底部的-body-封闭之前和封闭之后有什么区别浏览器会如何解析它们)
- [85. 移动端的点击事件的有延迟，时间是多久，为什么会有？ 怎么解决这个延时？](#85-移动端的点击事件的有延迟时间是多久为什么会有-怎么解决这个延时)
- [86. 什么是“前端路由”？什么时候适合使用“前端路由”？“前端路由”有哪些优点和缺点？](#86-什么是前端路由什么时候适合使用前端路由前端路由有哪些优点和缺点)
- [87. 如何测试前端代码么？ 知道 BDD, TDD, Unit Test 么？ 知道怎么测试你的前端工程么(mocha, sinon, jasmin, qUnit..)？](#87-如何测试前端代码么-知道-bdd-tdd-unit-test-么-知道怎么测试你的前端工程么mocha-sinon-jasmin-qunit)
- [88. 检测浏览器版本版本有哪些方式？](#88-检测浏览器版本版本有哪些方式)
- [89. 什么是 Polyfill ？](#89-什么是-polyfill-)
- [90. 使用 JS 实现获取文件扩展名？](#90-使用-js-实现获取文件扩展名)
- [91. 介绍一下 js 的节流与防抖？](#91-介绍一下-js-的节流与防抖)
- [92. Object.is() 与原来的比较操作符 三等于和两等于的区别？](#92-objectis-与原来的比较操作符--的区别)
- [93. escape,encodeURI,encodeURIComponent 有什么区别？](#93-escapeencodeuriencodeuricomponent-有什么区别)
- [94. Unicode 和 UTF-8 之间的关系？](#94-unicode-和-utf-8-之间的关系)
- [95. js 的事件循环是什么？](#95-js-的事件循环是什么)
- [96. js 中的深浅拷贝实现？](#96-js-中的深浅拷贝实现)
- [97. 手写 call、apply 及 bind 函数](#97-手写-callapply-及-bind-函数)
- [98. 函数柯里化的实现](#98-函数柯里化的实现)
- [99. 为什么 0.1 0.2 != 0.3？如何解决这个问题？](#99-为什么-01--02--03如何解决这个问题)
- [100. 原码、反码和补码的介绍](#100-原码反码和补码的介绍)
- [101. toPrecision 和 toFixed 和 Math.round 的区别？](#101-toprecision-和-tofixed-和-mathround-的区别)
- [102. 什么是 XSS 攻击？如何防范 XSS 攻击？](#102-什么是-xss-攻击如何防范-xss-攻击)
- [103. 什么是 CSP？](#103-什么是-csp)
- [104. 什么是 CSRF 攻击？如何防范 CSRF 攻击？](#104-什么是-csrf-攻击如何防范-csrf-攻击)
- [105. 什么是 Samesite Cookie 属性？](#105-什么是-samesite-cookie-属性)
- [106. 什么是点击劫持？如何防范点击劫持？](#106-什么是点击劫持如何防范点击劫持)
- [107. SQL 注入攻击？](#107-sql-注入攻击)
- [108. 什么是 MVVM？比之 MVC 有什么区别？什么又是 MVP ？](#108-什么是-mvvm比之-mvc-有什么区别什么又是-mvp-)
- [109. vue 双向数据绑定原理？](#109-vue-双向数据绑定原理)
- [110. Object.defineProperty 介绍？](#110-objectdefineproperty-介绍)
- [111. 使用 Object.defineProperty() 来进行数据劫持有什么缺点？](#111-使用-objectdefineproperty-来进行数据劫持有什么缺点)
- [112. 什么是 Virtual DOM？为什么 Virtual DOM 比原生 DOM 快？](#112-什么是-virtual-dom为什么-virtual-dom-比原生-dom-快)
- [113. 如何比较两个 DOM 树的差异？](#113-如何比较两个-dom-树的差异)
- [114. 什么是 requestAnimationFrame ？](#114-什么是-requestanimationframe-)
- [115. 谈谈你对 webpack 的看法](#115-谈谈你对-webpack-的看法)
- [116. offsetWidth/offsetHeight,clientWidth/clientHeight 与 scrollWidth/scrollHeight 的区别？](#116-offsetwidthoffsetheightclientwidthclientheight-与-scrollwidthscrollheight-的区别)
- [117. 谈一谈你理解的函数式编程？](#117-谈一谈你理解的函数式编程)
- [118. 异步编程的实现方式？](#118-异步编程的实现方式)
- [119. Js 动画与 CSS 动画区别及相应实现](#119-js-动画与-css-动画区别及相应实现)
- [120. get 请求传参长度的误区](#120-get-请求传参长度的误区)
- [121. URL 和 URI 的区别？](#121-url-和-uri-的区别)
- [122. get 和 post 请求在缓存方面的区别](#122-get-和-post-请求在缓存方面的区别)
- [123. 图片的懒加载和预加载](#123-图片的懒加载和预加载)
- [124. mouseover 和 mouseenter 的区别？](#124-mouseover-和-mouseenter-的区别)
- [125. js 拖拽功能的实现](#125-js-拖拽功能的实现)
- [126. 为什么使用 setTimeout 实现 setInterval？怎么模拟？](#126-为什么使用-settimeout-实现-setinterval怎么模拟)
- [127. let 和 const 的注意点？](#127-let-和-const-的注意点)
- [128. 什么是 rest 参数？](#128-什么是-rest-参数)
- [129. 什么是尾调用，使用尾调用有什么好处？](#129-什么是尾调用使用尾调用有什么好处)
- [130. Symbol 类型的注意点？](#130-symbol-类型的注意点)
- [131. Set 和 WeakSet 结构？](#131-set-和-weakset-结构)
- [132. Map 和 WeakMap 结构？](#132-map-和-weakmap-结构)
- [133. 什么是 Proxy ？](#133-什么是-proxy-)
- [134. Reflect 对象创建目的？](#134-reflect-对象创建目的)
- [135. require 模块引入的查找方式？](#135-require-模块引入的查找方式)
- [136. 什么是 Promise 对象，什么是 Promises/A 规范？](#136-什么是-promise-对象什么是-promisesa-规范)
- [137. 手写一个 Promise](#137-手写一个-promise)
- [138. 如何检测浏览器所支持的最小字体大小？](#138-如何检测浏览器所支持的最小字体大小)
- [139. 怎么做 JS 代码 Error 统计？](#139-怎么做-js-代码-error-统计)
- [140. 单例模式模式是什么？](#140-单例模式模式是什么)
- [141. 策略模式是什么？](#141-策略模式是什么)
- [142. 代理模式是什么？](#142-代理模式是什么)
- [143. 中介者模式是什么？](#143-中介者模式是什么)
- [144. 适配器模式是什么？](#144-适配器模式是什么)
- [145. 观察者模式和发布订阅模式有什么不同？](#145-观察者模式和发布订阅模式有什么不同)
- [146. Vue 的生命周期是什么？](#146-vue-的生命周期是什么)
- [147. Vue 的各个生命阶段是什么？](#147-vue-的各个生命阶段是什么)
- [148. Vue 组件间的参数传递方式？](#148-vue-组件间的参数传递方式)
- [149. computed 和 watch 的差异？](#149-computed-和-watch-的差异)
- [150. vue-router 中的导航钩子函数](#150-vue-router-中的导航钩子函数)
- [151. $route 和 $router 的区别？](#151-route-和-router-的区别)
- [152. vue 常用的修饰符？](#152-vue-常用的修饰符)
- [153. vue 中 key 值的作用？](#153-vue中-key-值的作用)
- [154. computed 和 watch 区别？](#154-computed-和-watch-区别)
- [155. keep-alive 组件有什么作用？](#155-keep-alive-组件有什么作用)
- [156. vue 中 mixin 和 mixins 区别？](#156-vue-中-mixin-和-mixins-区别)
- [157. 开发中常用的几种 Content-Type ？](#157-开发中常用的几种-content-type-)
- [158. 如何封装一个 javascript 的类型判断函数？](#158-如何封装一个-javascript-的类型判断函数)
- [159. 如何判断一个对象是否为空对象？](#159-如何判断一个对象是否为空对象)
- [160. 使用闭包实现每隔一秒打印 1,2,3,4](#160-使用闭包实现每隔一秒打印-1234)
- [161. 手写一个 jsonp](#161-手写一个-jsonp)
- [162. 手写一个观察者模式？](#162-手写一个观察者模式)
- [163. EventEmitter 实现](#163-eventemitter-实现)
- [164. 一道常被人轻视的前端 JS 面试题](#164-一道常被人轻视的前端js面试题)
- [165. 如何确定页面的可用性时间，什么是 Performance API？](#165-如何确定页面的可用性时间什么是-performance-api)
- [166. js 中的命名规则](#166-js-中的命名规则)
- [167. js 语句末尾分号是否可以省略？](#167-js-语句末尾分号是否可以省略)
- [168. Object.assign()](#168-objectassign)
- [169. Math.ceil 和 Math.floor](#169-mathceil-和-mathfloor)
- [170. js for 循环注意点](#170-js-for-循环注意点)
- [171. 一个列表，假设有 100000 个数据，这个该怎么办？](#171-一个列表假设有100000个数据这个该怎么办)
- [172. js 中倒计时的纠偏实现？](#172-js-中倒计时的纠偏实现)
- [173. 进程间通信的方式？](#173-进程间通信的方式)
- [174. 如何查找一篇英文文章中出现频率最高的单词？](#174-如何查找一篇英文文章中出现频率最高的单词)

#### 1. 介绍 js 的基本数据类型

```
js 一共有六种基本数据类型，分别是 Undefined、Null、Boolean、Number、String，还有在 ES6 中新增的 Symbol 和 ES10 中新增的 BigInt 类型。
Symbol 值代表独一无二的值，它的出现我认为主要是为了解决可能出现的全局变量冲突的问题。
BigInt 用于表示超过精度范围的大整数，1n ！= 1
```

#### 补充：JS语言特点：

```
动态语言(弱类型的)：其动态性就主要体现在是事件驱动的脚本语言，不需要经过web服务器就可以对用户的输入做出响应；解释性语言，是在程序运行过程中逐行进行解释的；跨平台性好，不依赖于操作系统，只需要浏览器的支持就可以了。主要是因为解释性原因并不是直接到机器语言，而是先翻译成中间代码（还是文本形式的代码），然后由解释器将其解释成相应的机器语言并加以执行，所以有解释器就可以了。相较于编译型语言，直接将源代码编译成相应的机器代码，然后直接执行，但是不同操作系统识别二进制的方式不同，编译后的机器码不一定能够在所有平台上运行，所以跨平台性不好。

解释型语言的源代码不是直接翻译成机器语言**，而是首先翻译成中间代码，然后再由解释器对中间代码进行解释运行。

解释型语言每次在运行时都需要实时的去翻译中间代码然后执行翻译出的机器代码，所以执行效率低下．解释型语言严重依赖于解释器的类型，解释器速度快，那么执行速度就会快一点．因为不需要进行预先编译，所以是以文本的方式存储程序代码，跨平台能力好

编译型语言是直接经过编译处理，把源代码直接翻译成机器代码，再由机器运行机器码．

跨平台能力: 因操作系统识别二进制的方式不同，所以经过编译后得到的机器码不一定能够在所有平台上运行，而解释型语言不同，只需要在系统配置一个解释器，程序即可兼容各个平台．

```



#### 2. JavaScript 有几种类型的值？你能画一下他们的内存图吗？

涉及知识点：

- 栈：基本数据类型（原始值）（Undefined、Null、Boolean、Number、String）
- 堆：引用数据类型 （对象）Object、Array、Function、Date、Error、RegExp

```
两种类型间的主要区别是它们的存储位置不同：

基本数据类型的值直接保存在栈中，由于基本数据类型占据空间小、大小固定，属于被频繁使用数据，所以放入栈中存。

而引用数据类型的值保存在堆中，通过使用在栈中保存对应的指针来获取堆中的值（指针指向堆中该对象实体的起始地址）。
由于引用数据类型占据空间大、大小不固定，放入栈中将会影响程序运行的性能，所以存储在堆内存中。
```



详细资料可以参考：
[《JavaScript 有几种类型的值？》](https://blog.csdn.net/lxcao/article/details/52749421)
[《JavaScript 有几种类型的值？能否画一下它们的内存图；》](https://blog.csdn.net/jiangjuanjaun/article/details/80327342)

#### 3. 什么是堆？什么是栈？它们之间有什么区别和联系？

```
堆和栈的概念存在于数据结构中和操作系统内存中。

在数据结构中，栈中数据的存取方式为先进后出。而堆是一个优先队列，是按优先级来进行排序的，优先级可以按照大小来规定。完全
二叉树是堆的一种实现方式。

在操作系统中，内存被分为栈区和堆区。

栈区内存由编译器自动分配释放，存放函数的参数值，局部变量的值等。其操作方式类似于数据结构中的栈。

堆区内存一般由程序员分配释放，若程序员不释放，程序结束时可能由垃圾回收机制回收。
```

详细资料可以参考：
[《什么是堆？什么是栈？他们之间有什么区别和联系？》](https://www.zhihu.com/question/19729973)

#### 4. 内部属性 [[Class]] 是什么？

对象的三个属性：原型；类型；可扩展性。

```
对象的内部属性 [[Class]] 表示这个对象的类型，可以用Object.prototype.toString(..) 来间接查看（因为除了object之外其他对象的toString方法基本都重写了）例如：

Object.prototype.toString.call( [1,2,3] );
// "[object Array]"

Object.prototype.toString.call( /regex-literal/i );
// "[object RegExp]"

// 我们自己创建的类就不会有这份特殊待遇，因为 toString()方法找不到 toStringTag 属性时只好返回默认的[[Class]]即[object Object]
class Class1 {}
Object.prototype.toString.call(new Class1()); // "[object Object]"
//ES6来创建类
// 需要定制[[Class]]
class Class2 {
  //指定symbol值的toStringTag 存取器属性的取回来的值，就是访问 toStringTag 属性时获取到的值
  get [Symbol.toStringTag]() {
    return "Class2";
  }
}
Object.prototype.toString.call(new Class2()); // "[object Class2]"
```

```
一般来设置存取器属性的时候：
get、set就相当于和function声明一样
obj = {
	get name(){...};
	set name(val){...}
}

借助Object.defineProperty

Object.defineProperty(obj,name,{
	get(){...}
	set(val){....}
})
```

#### 5. 介绍 js 有哪些内置对象？

JS对象可以分为内置对象、宿主对象、自定义对象

内置对象：由ECMAScript规范定义的对象或类比如：数组、函数、日期、正则表达式等..

宿主对象：由JS解释器所嵌入的宿主环境定义的。

自定义对象：运行的JS代码创建的对象。

涉及知识点：

```
标准内置对象的分类

（1）值属性，这些全局属性返回一个简单值，这些值没有自己的属性和方法。

例如 Infinity、NaN、undefined、null 字面量

（2）函数属性，全局函数可以直接调用，不需要在调用时指定所属对象，执行结束后会将结果直接返回给调用者。

例如 eval()、uneval()、isFinite()、isNaN()、parseFloat()、parseInt()、decodeURI()、decodeURIComponent()、encodeURI()、encodeURIComponent()、escape()、unescape() 等后两个已废弃

（3）基本对象，基本对象是定义或使用其他对象的基础。基本对象包括一般对象、函数对象和错误对象。

例如 Object、Function、Boolean、Symbol、Error 等

（4）数字和日期对象，用来表示数字、日期和执行数学计算的对象。

例如 Number、Math、Date

（5）字符串，用来表示和操作字符串的对象。

例如 String、RegExp

（6）可索引的集合对象，这些对象表示按照索引值来排序的数据集合，包括数组和类型数组，以及类数组结构的对象。例如 Array

（7）使用键的集合对象，这些集合对象在存储数据时会使用到键，支持按照插入顺序来迭代元素。

例如 Map、Set、WeakMap、WeakSet

（8）矢量集合，SIMD 矢量集合中的数据会被组织为一个数据序列。

例如 SIMD 等

（9）结构化数据，这些对象用来表示和操作结构化的缓冲区数据，或使用 JSON 编码的数据。

例如 JSON 等

（10）控制抽象对象

例如 Promise、Generator 等

（11）反射

例如 Reflect、Proxy

（12）国际化，为了支持多语言处理而加入 ECMAScript 的对象。

例如 Intl、Intl.Collator 等

（13）WebAssembly

（14）其他

例如 arguments

```

 回答：

```
js 中的内置对象主要指的是在程序执行前存在全局作用域里的由 ECMAScript规范定义的一些全局值属性、函数和用来实例化其他对象的构造函数对象。
```

详细资料可以参考：
[《标准内置对象的分类》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects)
[《JS 所有内置对象属性和方法汇总》](https://segmentfault.com/a/1190000011467723#articleHeader24)

#### 6. undefined 与 undeclared 的区别？

```
已在作用域中声明但还没有赋值的变量，是 undefined 的。相反，还没有在作用域中声明过的变量，是 undeclared 的。

对于 undeclared 变量的引用，浏览器会报引用错误，如 ReferenceError: b is not defined 。
但是我们可以使用 typeof 的安全防范机制来避免报错，因为对于 undeclared（或者 not defined ）变量，typeof 会返回 "undefined"。
```

#### 7. null 和 undefined 的区别？

```
undefined 代表的含义是未定义，一般变量声明了但还没有赋值定义的时候会返回 undefined。
null 代表的含义是空对象，主要用于初始化可能会返回对象的变量。

当我们对两种类型使用 typeof 进行判断的时候，Null 类型化会返回 “object”，这是一个历史遗留的问题。
当我们使用双等号对两种类型的值进行比较时会返回 true，使用三个等号时会返回 false。
```

详细资料可以参考：
[《JavaScript 深入理解之 undefined 与 null》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8Bundefined%E4%B8%8Enull.html)

#### 8. 如何获取安全的 undefined 值？

```
void运算符接操作数构成void表达式，操作数会照常计算但忽略计算结果并返回undefined。

常用 void 0 来获得 undefined。
```

#### 9. 说几条写 JavaScript 的基本规范？（X）

```
在平常项目开发中，我们遵守一些这样的基本规范，比如说：

（1）一个函数作用域中所有的变量声明应该尽量提到函数首部，用一个 var 声明，不允许出现两个连续的 var 声明，声明时
    如果变量没有值，应该给该变量赋值对应类型的初始值，便于他人阅读代码时，能够一目了然的知道变量对应的类型值。

（2）代码中出现地址、时间等字符串时需要使用常量代替。

（3）在进行比较的时候吧，尽量使用'===', '!=='代替'==', '!='。

（4）不要在内置对象的原型上添加方法，如 Array, Date。

（5）switch 语句必须带有 default 分支。

（6）for 循环必须使用大括号。

（7）if 语句必须使用大括号。
```

#### 10. JavaScript 原型，原型链？ 有什么特点？

```
一般情况下、每一个对象都有一个原型对象，而原型对象也有自己的原型对象，这样就形成了原型链，原型链的尽头一般来说都是 Object.prototype  
(这就是我们新建的对象为什么能够使用 toString() 等方法的原因)。
Object.create(null) 创建一个没有原型的对象
Object.create(Object.prototype) 创建一个空对象{}
Object.Prototype 没有原型对象
```

详细资料可以参考：
[《JavaScript 深入理解之原型与原型链》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8B%E5%8E%9F%E5%9E%8B%E4%B8%8E%E5%8E%9F%E5%9E%8B%E9%93%BE.html)

#### 11. js 对象获取原型的方法？

- p.\_\_proto\_\_

- p.constructor.prototype

- Object.getPrototypeOf(p)

  <img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-29_08-36-52.png" style="zoom: 80%;" />

#### 12. 在 js 中不同进制数字的表示方式

- 以 0X、0x 开头的表示为十六进制。

- 以 0O、0o 开头的表示为八进制。

- 以 0B、0b 开头的表示为二进制格式。

#### 13. js 中整数的安全范围是多少？

```
JS中数值是以64位双精度浮点数的形式存储的，有效位只是53位2进制数，超过53位的部分会被截取掉，造成精度丢失。安全整数为(2^53 - 1)、-(2^53 - 1)，
分别对应ES6中的 Number.MAX_SAFE_INTEGER和Number.MIN_SAFE_INTEGER

如果某次计算的结果得到了一个超过 JavaScript 数值范围的值，那么这个值会被自动转换为特殊的 Infinity 值。如果某次
计算返回了正或负的 Infinity 值，那么该值将无法参与下一次的计算。判断一个数是不是有穷的，可以使用 isFinite 函数
来判断。
```

#### 14. typeof NaN 的结果是什么？

```
NaN 意指“不是一个数字”（not a number）

typeof NaN; // "number"

NaN 和自身不相等
```

#### 15. isNaN 和 Number.isNaN 函数的区别？

```
函数 isNaN 接收参数后，会尝试将这个参数转换为数值，任何不能被转换为数值的的值都会返回 true，因此非数字值传入也会返回 true ，会影响 NaN 的判断。

函数 Number.isNaN 会首先判断传入参数是否为数字，如果是数字再继续判断是否为 NaN ，这种方法对于 NaN 的判断更为准确。

isNaN看的是参数能不能转换为数值，Number.isNaN看的是参数是不是就是数值。
```

#### 16. Array 构造函数只有一个参数值时的表现？

```
Array 构造函数只带一个数字参数的时候，创建一个指定长度的空数组

构造函数 Array(..) 不要求必须带 new 关键字。不带时，它会被自动补上。

new Array(5).fill(1)
```

#### 17. 其他值到字符串的转换规则？

```
规范的 9.8 节中定义了抽象操作 ToString ，它负责处理非字符串到字符串的强制类型转换。

（1）Null 和 Undefined 类型 ，null 转换为 "null"，undefined 转换为 "undefined"，

（2）Boolean 类型，true 转换为 "true"，false 转换为 "false"。

（3）Number 类型的值直接转换，不过那些极小和极大的数字会使用指数形式。

（4）Symbol 类型的值直接转换，但是只允许显式强制类型转换，使用隐式强制类型转换会产生错误。

（5）对普通对象来说，除非自行定义 toString() 方法，否则会调用 toString()（Object.prototype.toString()）
    来返回内部属性 [[Class]] 的值，如"[object Object]"。如果对象有自己的 toString() 方法，字符串化时就会
    调用该方法并使用其返回值。
```

#### 18. 其他值到数字值的转换规则？

```
有时我们需要将非数字值当作数字来使用，比如数学运算。为此 ES5 规范在 9.3 节定义了抽象操作 ToNumber。

null、false、空字符串‘’、空数组[]转换为0

（1）Undefined 类型的值转换为 NaN。

（2）Null 类型的值转换为 0。

（3）Boolean 类型的值，true 转换为 1，false 转换为 0。

（4）String 类型的值转换如同使用 Number() 函数进行转换，如果包含非数字值则转换为 NaN，空字符串为 0。

（5）Symbol 类型的值不能转换为数字，会报错。

（6）对象（包括数组）会首先被转换为相应的基本类型值，如果返回的是非数字的基本类型值，则再遵循以上规则将其强制转换为数字。
为了将值转换为相应的基本类型值，抽象操作 ToPrimitive 会首先（通过内部操作 DefaultValue）检查该值是否有valueOf() 方法。如果有并且返回基本类型值，就使用该值进行强制类型转换。如果没有就使用 toString() 的返回值（如果存在）来进行强制类型转换。
如果 valueOf() 和 toString() 均不返回基本类型值，会产生 TypeError 错误。
```

#### 19. 其他值到布尔类型的值的转换规则？

```
ES5 规范 9.2 节中定义了抽象操作 ToBoolean，列举了布尔强制类型转换所有可能出现的结果。

以下这些是假值：
• undefined
• null
• false
• +0、-0 和 NaN
• ""
假值的布尔强制类型转换结果为 false。从逻辑上说，假值列表以外的都应该是真值。
```

#### 20. {} 和 [] 的 valueOf 和 toString 的结果是什么？

```
{} 的 valueOf 结果为 {} ，toString 的结果为 "[object Object]"

[] 的 valueOf 结果为 [] ，toString 的结果为 ""
```

原始值没有属性和方法，但为什么字符串.length可以返回字符串的长度？

因为原始值会调用new String()自动装箱,创建一个临时的包装类对象，属性和方法的调用都来自这个包装类对象，访问完长度属性之后，随即销毁这个临时对象。

比如：

s = 'test';   //创建一个字符串

s.len = 4;  //字符串原始值自动装箱，创建一个临时对象，给其指定len属性值为4，随即消毁

console.log(s.len); //又创建了一个新的临时对象，但是这个对象上没有len属性，所以返回undefined

因此，对于原始值的一些操作都是只能读不能改的，同样的布尔值、数值、在使用时也会调用相应的new Boolen()、 new Number()进行装箱，

对于原始值undefined和null而言，其没有包装类对象，所以也就不能使用方法（没有toString、valueOf 等别人都能用的方法）

包装对象：区分字符串值和字符串对象、布尔值和布尔对象、数值和数值对象

new Number（）、new String（）、new Boolen（）创建包装对象，获取的是对象

Number（）、 String（）、 Boolen（）进行显示的类型转换，获取的是值

#### 21. 什么是假值对象？

```
浏览器在某些特定情况下，在常规 JavaScript 语法基础上自己创建了一些外来值，这些就是“假值对象”。假值对象看起来和
普通对象并无二致（都有属性，等等），但将它们强制类型转换为布尔值时结果为 false 最常见的例子是 document.all，它
是一个类数组对象，包含了页面上的所有元素，由 DOM（而不是 JavaScript 引擎）提供给 JavaScript 程序使用。
```

#### 22. ~ 操作符的作用？

（一字节八位）

``` 
 ~ 会将数字转换为 32 位整数，相当于求整数部分的补码。

~x 大致等同于 -(x+1)。 ~2 ==》 -3
~~2.9 ==》 2  ~~2.2 ==> 2

~~x 对x进行取整，亦可实现从字符串到数值的转换 ~~2 ==》 2 ~~‘2’ ==》 2 
和用Number()来进行字符串到数值转换的不同点就是 Number(undefined) ==》 NaN  ~~undefined == 0，此外遇到非数值的字符最终转换结果也是0

~ 按位取反  ！逻辑取反
```

#### 23. 解析字符串中的数字和将字符串强制类型转换为数字的返回结果都是数字，它们之间的区别是什么？

```
解析允许字符串（如 parseInt() ）中含有非数字字符，解析按从左到右的顺序，如果遇到非数字字符就停止。
而转换（如 Number ()）不允许出现非数字字符，否则会失败并返回 NaN。
```

#### 24. `+` 操作符什么时候用于字符串的拼接？

```
简单来说就是，如果 + 的其中一个操作数是字符串（或者通过以上步骤最终得到字符串），则执行字符串拼接，否则执行数字加法。

那么对于除了加法的运算符来说，只要其中一方是数字，那么另一方就会被转为数字。

‘1’ + 2 = ‘12’

+‘1’ + 2 = 3

‘2’ -1 = 1
```

#### 25. 什么情况下会发生布尔值的隐式强制类型转换？

```
（1） if (..) 语句中的条件判断表达式。
（2） for ( .. ; .. ; .. ) 语句中的条件判断表达式（第二个）。
（3） while (..) 和 do..while(..) 循环中的条件判断表达式。
（4） ? : 中的条件判断表达式。
（5） 逻辑运算符 ||（逻辑或）和 &&（逻辑与）左边的操作数（作为条件判断表达式）。
```

#### 26. || 和 && 操作符的返回值？

```
短路&&：第一个操作数为真则返回第二个操作数的值，第一个操作数为假则返回第一个操作数的值

短路||：第一个操作数为假则返回第二个操作数的值，第一个操作数为真则返回第一个操作数的值

|| 和 && 返回它们其中一个操作数的值，而非条件判断的结果
```

#### 27. Symbol 值的强制类型转换？

```
ES6 允许从Symbol到字符串的显式强制类型转换，然而隐式强制类型转换会产生错误。
String(Symbol('My symbol'))   Symbol('My symbol').toString()

Symbol 值不能够被强制类型转换为数字（显式和隐式都会产生错误），但可以被强制类型转换为布尔值（显式和隐式结果都是 true ）。
```

#### 28. == 操作符的强制类型转换规则？

```
1.对象和字符串的比较，调用对象的toString方法将对象转为字符串而后比较
2.null 和 undefined相等，其他都不相等，即null == undefined 为true
3.NaN 不等于 NaN，即 NaN == NaN 为false
4.其他是将左右操作数转换为数值加以判断
```

详细资料可以参考：
[《JavaScript 字符串间的比较》](https://www.jeffjade.com/2015/08/28/2015-09-02-js-string-compare/)

数字转换为字符串

toString无法对undefined 和 null进行转换(因为undefined没有包装类，不能一对象的形式使用方法)，String可以；

toString可以将数字转换为指定基数的字符串，String无法设置基数

toFixed()

toPrecision()

#### 29. 如何将字符串转化为数字，例如 '12.3b'?

```
（1）Number() 方法将字符串转化为数值，前提是所包含的字符串不能有非数值的字符。

（2）parseInt() 方法将字符串解析为整数，第一个参数是要解析的字符串，第二个参数可以设置基数，即以什么基底去看这个数，基底2-36，为0时按照10进制解析。

（3）parseFloat() 方法将字符串解析为浮点数，第一个参数是要解析的字符串，第二个参数可以设置基数，即以什么基底去看这个数，基底2-36，为0时按照10进制解析。
```

详细资料可以参考：
[《详解 JS 中 Number()、parseInt() 和 parseFloat() 的区别》](https://blog.csdn.net/m0_38099607/article/details/72638678)

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-15_09-07-42.png" style="zoom:67%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-15_09-20-54.png" style="zoom:67%;" />

```
replace的第二个参数如果是一个函数，则函数的第一个参数是匹配的字符，第二个则是匹配字符所出现的位置。
```

何将浮点数点左边的数每三位添加一个逗号，如 12000000.11 转化为『12,000,000.11』?

```js
// 方法一
function format(number) {
  //小数点后面每三位不加逗号
  return number && number.replace(/(?!^)(?=(\d{3})+\.)/g, ",");
}
零宽正向先行断言(？=p) 接下来的字符与p匹配
零宽负向先行断言(？！p) 接下来的字符不与p匹配
（...）把单独的项组合成子表达式；在完整的模式中定义子模式，即可以从匹配的目标中抽取和圆括号中子模式相匹配的部分
\n 对应第n个分组的匹配，
#n 对应第n个分组的值，
(?:...) 只组合，不记忆与该组相匹配的字符
// 方法二
function format2(number) {
  return number.toLocaleString('en')
}
```

#### 31. 常用正则表达式

```js
// （1）匹配 16 进制颜色值
var regex = /#([0-9a-fA-F]{6}|[0-9a-fA-F]{3})/g;

// （2）匹配日期，如 yyyy-mm-dd 格式
var regex = /^[0-9]{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])$/;

// （3）匹配 qq 号
var regex = /^[1-9][0-9]{4,10}$/g;

// （4）手机号码正则
var regex = /^1[34578]\d{9}$/g;

// （5）用户名正则
var regex = /^[a-zA-Z0-9_-]{4,16}$/;

// （6）邮箱正则
var regex = /^([A-Za-z0-9_-.])+@([A-Za-z0-9_-.])+.([A-Za-z]{2,4})$/

```

详细资料可以参考：
[《前端表单验证常用的 15 个 JS 正则表达式》](http://caibaojian.com/form-regexp.html)
[《JS 常用正则汇总》](https://www.jianshu.com/p/1cb5229325a7)

#### 32. 生成随机数的各种方法？

```
Math.random()
Math.random()*(m-n)+n  大于等于n，小于m，得到的不是整数一般还需要取个整
```

[《JS - 生成随机数的方法汇总（不同范围、类型的随机数）》](http://www.hangge.com/blog/cache/detail_1872.html)

#### 33. 如何实现数组的随机排序？

```js
// （2）随机从原数组抽取一个元素，加入到新数组

function randomSort(arr) {
  var result = [];

  while (arr.length > 0) {
    var randomIndex = Math.floor(Math.random() * arr.length);
    result.push(arr[randomIndex]);
    arr.splice(randomIndex, 1);
  }

  return result;
}

// （3）随机交换数组内的元素（洗牌算法类似）

function randomSort(arr) {
  var index,
    randomIndex,
    temp,
    len = arr.length;

  for (index = 0; index < len; index++) {
    randomIndex = Math.floor(Math.random() * (len - index)) + index;

    temp = arr[index];
    arr[index] = arr[randomIndex];
    arr[randomIndex] = temp;
  }

  return arr;
}

// es6
function randomSort(array) {
  let length = array.length;

  if (!Array.isArray(array) || length <= 1) return;

  for (let index = 0; index < length - 1; index++) {
    // [1,2,3] length为3，索引0时剩下长度为3，索引1时剩下长度为2
    let randomIndex = Math.floor(Math.random() * (length - index)) + index;

    // es6交换变量(解构赋值的常见用途)
    [array[index], array[randomIndex]] = [array[randomIndex], array[index]];
  }

  return array;
}
```

详细资料可以参考：
[《Fisher and Yates 的原始版》](https://gaohaoyang.github.io/2016/10/16/shuffle-algorithm/#top)
[《javascript 实现数组随机排序?》](https://www.zhihu.com/question/32303195)
[《JavaScript 学习笔记：数组随机排序》](https://www.w3cplus.com/javascript/how-to-randomize-shuffle-a-javascript-array.html)

#### 34. javascript 创建对象的几种方式？

ES5：

```
一般使用字面量的形式直接创建对象，但是这种创建方式对于创建大量相似对象的时候，会产生大量的重复代码。而且js
和一般的面向对象的语言不同，在 ES6 之前它没有类的概念。一般就是使用函数来进行模拟，从而获取可复用的对象创建方式，我了解到的方式有这么几种：

（1）第一种是工厂模式，工厂模式将创建对象的过程封装起来，通过调用函数来达到复用的目的。但是它有一个很大的问题就是创建出来的对象无法和某个类型联系起来。

（2）第二种是构造函数模式。js 中每一个函数都可以作为构造函数，并通过 new 来调用的。new构造函数首先会创建一个对象，然后将对象的原型指向构造函数的 prototype 属性，然后将执行上下文中的 this 指向这个对象，最后再执行整个函数，如果函数执行返回的是原始值，则最终返回新建的对象。因为 this 的值指向了新建的对象，因此我们可以使用 this 给对象赋值。构造函数模式相对于工厂模式的优点是，所创建的对象和构造函数建立起了联系，因此我们可以通过原型来识别对象的类型。但是构造函数存在一个缺点，就是造成了很多不必要的浪费，因为对象中有很多公有的方法，而利用构造函数创建的对象，其中的方法都是每个对象所独有的。

（3）第三种模式是原型模式，每一个函数都有一个 prototype 属性，这个属性是一个对象，它包含了通过构造函数创建的所有实例都能共享的属性和方法。因此可以使用原型对象来添加公用属性和方法，从而实现代码的复用。这种方式相对于构造函数模式来说，解决了对象中公有方法的复用问题。但是这种模式也存在一些问题，一个是没有办法通过传入参数来初始化实例，另一个是如果其属性值是一个引用类型的值，那么所有实例将会共享，也就是说一个实例对引用类型值的改变会影响所有的实例。

（4）第四种模式是组合使用构造函数模式和原型模式，构造函数中放实例对象所独有的属性，原型对象上放实例对象所公有的方法。这种方法很好的解决了两种模式单独使用时的缺点，但是有一点不足的就是，因为使用了两种不同的模式，所以对于代码的封装性不够好。

（5）第五种模式是动态原型模式，这一模式将原型方法赋值的过程移动到了构造函数的内部，通过对属性是否存在的判断，可以实现仅在第一次调用函数时对原型对象赋值一次的效果。这一种方式很好地对组合模式进行了封装。

（6）第六种模式是寄生构造函数模式，这一种模式和工厂模式的实现基本相同，我对这个模式的理解是，主要是基于一个已有的类型，在实例化时对实例化的对象进行扩展。这样既不用修改原来的构造函数，也达到了扩展对象的目的。它的一个缺点和工厂模式一样，无法实现对象的识别。

```

ES6类：

是构造函数的语法糖，相当于是对构造函数做了一层包装，类中包括constructor方法在内的其他非静态方法都定义在原型上，所有实例共享同一个原型对象。constructor方法是类的默认方法，作用是实例化一个对象(this)。实例调用的方法都是调用的原型对象上的方法，对于静态方法而言他不会被实例继承，直接通过类就可以调用。construct属性、prototype属性相关都和构造函数一样。此外，类中所有方法都是不可枚举的，而且只能通过new来使用类，这和构造函数有所不同。再者，类当前不支持静态属性、私有方法、私有属性、虽然目前有相关提案，但仍未实现。

```javascript
class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }

  toString() {
    return '(' + this.x + ', ' + this.y + ')';
  }
}
```

```javascript
//竟然可以这样在ES6中声明方法！！！！！
//写成表达式的形式和直接函数声明，不要function关键字的都可以
class Test {
    constructor() {}
    test1 = function() {
        console.log(1);
    }
    test2 = () => {
        console.log(2);
    }
    test3() {
        console.log(3);
    }

}

const test5 = new Test();
test5.test1();
test5.test2();
test5.test3();
```

详细资料可以参考：
[《JavaScript 深入理解之对象创建》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8B%E5%AF%B9%E8%B1%A1%E5%88%9B%E5%BB%BA.html)

#### 35. JavaScript 继承的几种实现方式？

```
我了解的 js 中实现继承的几种方式有：

（1）第一种是以原型链的方式来实现继承，但是这种实现方式存在的缺点是，在包含有引用类型的数据时，会被所有的实例对象所共享，一个实例改变这个数据，其他实例都会受到影响。还有就是在创建子类型的时候不能向超类型传递参数。

（2）第二种方式是使用借用构造函数的方式，这种方式是通过在子类型的函数中调用超类型的构造函数来实现的，这一种方法解决了不能向超类型传递参数的缺点，但是它存在的一个问题父类原型上的属性和方法也不能被继承。

（3）第三种方式是组合继承，组合继承是将原型链和借用构造函数组合起来使用。构造函数实现实例独有属性的继承，原型链式继承实现原型对象上实例公有方法的继承。
这种方式解决了两种模式单独使用时的问题，但是由于我们是以超类型的实例来作为子类型的原型，所以调用了两次超类的构造函数，造成了子类型的原型中多了很多不必要的属性。

（6）第六种方式是寄生式组合继承，组合继承的缺点就是使用超类型的实例做为子类型的原型，导致添加了不必要的原型属性。寄生式组合继承的方式是使用超类型的原型的副本来作为子类型的原型，这样就避免了创建不必要的属性。

（4）第四种方式是原型式继承，原型式继承的主要思路就是基于已有的对象来创建新的对象，实现的原理是，向函数中传入一个对象，然后返回一个以这个对象为原型的对象。ES5 中定义的 Object.create() 方法就是原型式继承的实现。缺点与原型链方式相同。

（5）第五种方式是寄生式继承，寄生式继承的思路是创建一个用于封装继承过程的函数，通过传入一个对象，然后复制一个对象的副本，然后对象进行扩展，最后返回这个对象。这个扩展的过程就可以理解是一种继承。这种继承的优点就是对一个简单对象实现继承，如果这个对象不是我们的自定义类型时。缺点是没有办法实现函数的复用。

```

ES6的继承:

通过`extends`关键字实现继承

```javascript
class ColorPoint extends Point {
  constructor(x, y, color) {
    super(x, y); // 调用父类的constructor(x, y)
    this.color = color;
  }

  toString() {
    return this.color + ' ' + super.toString(); // 调用父类的toString()
  }
}

//=====================================================================================================================
super有两种使用方式，一种是直接作为函数方法使用（代表父类的构造函数），一种是直接作为对象使用（在普通方法 中指向父类的原型对象，在静态方法中指向父类）：

作为函数使用：在子类的constructor方法中必须调用super方法，因为子类的this是在父类this的基础上处理得来的(没有调用super方法之前不能使用子类this)。
即先调用父类构造函数super()，得到父类的实例属性和方法，之后加工处理为子类的实例属性和方法。此外，虽然super()函数代表了父类的构造函数，但是其内部this指向的是子类的实例。

作为对象使用:super作为对象时，在普通方法中，指向父类的原型对象；在静态方法中，指向父类。在子类普通方法中,super调用父类的方法时，方法内部的this指向当前的子类实例;在子类的静态方法中通过super调用父类的方法时，方法内部的this指向当前的子类，而不是子类的实例。

//==========================================================================================
ES6继承的两条继承链：
静态方法的继承：子类的__proto__属性，表示构造函数的继承，总是指向父类。
原型对象上方法的继承：子类prototype属性的__proto__属性，表示方法的继承，总是指向父类的prototype属性。
子类实例的__proto__属性的__proto__属性，指向父类实例的__proto__属性

//===================================================================================================================
ES5的继承与ES6的继承：
ES5的继承实质上是先新建子类的实例对象this，再将父类的属性添加到子类上，由于父类的内部属性无法获取，导致无法继承原生的构造函数。而ES6则是在constructor方法中调用super()方法，获取父类的实例对象this，之后再将其处理为子类的实例对象this,从而使得父类的所有行为都可以继承。
```

详细资料可以参考：
[《JavaScript 深入理解之继承》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8B%E7%BB%A7%E6%89%BF.html)

#### 36. 寄生式组合继承的实现？

```js
function Person(name) {
  this.name = name;
}

Person.prototype.sayName = function() {
  console.log("My name is " + this.name + ".");
};

function Student(name, grade) {
  Person.call(this, name);
  this.grade = grade;
}

Student.prototype = Object.create(Person.prototype);
Student.prototype.constructor = Student;

Student.prototype.sayMyGrade = function() {
  console.log("My grade is " + this.grade + ".");
};
```

**原型链式继承：**

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/14_0%E7%BB%A7%E6%89%BF%E4%B9%8B%E5%8E%9F%E5%9E%8B%E9%93%BE%E7%BB%A7%E6%89%BF%E7%9A%84%E5%8E%9F%E7%90%86.png" style="zoom:67%;" />

**构造函数式继承：**

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/14_1%E7%BB%A7%E6%89%BF%E4%B9%8B%E6%9E%84%E9%80%A0%E5%87%BD%E6%95%B0%E7%BB%A7%E6%89%BF.png" style="zoom: 50%;" />

**组合式继承：**

<img src="https://gitee.com/kszycyp/blog/raw/master/img/14_2%E7%BB%A7%E6%89%BF%E4%B9%8B%E7%BB%84%E5%90%88%E5%BC%8F%E7%BB%A7%E6%89%BF3.png" style="zoom:67%;" />

**寄生组合是继承：**

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/14_3%E7%BB%A7%E6%89%BF%E4%B9%8B%E5%AF%84%E7%94%9F%E7%BB%84%E5%90%88%E5%BC%8F%E7%BB%A7%E6%89%BF.png" style="zoom: 80%;" />

#### 37. Javascript 的作用域链？

```
当前执行上下文的作用域链是在其父级执行上下文的作用域链顶端插入当前执行上下文的变量对象，作用域链的本质上是一个指向变量对象的指针列表。作用域链的前端始终都是当前执行上下文的变量对象。全局执行上下文的变量对象（也就是全局对象）始终是作用域链的最后一个对象。当我们查找一个变量时，如果当前执行环境中没有找到，我们可以沿着作用域链向后查找。
```

详细资料可以参考：
[《JavaScript 深入理解之作用域链》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8B%E4%BD%9C%E7%94%A8%E5%9F%9F%E9%93%BE.html)

#### 38. 谈谈 This 对象的理解。

```
this 是执行上下文中的一个属性，其指向和函数的使用方式有关
```

- 1.第一种是函数调用模式，当一个函数不是一个对象的属性时，直接作为函数来调用时，this 指向全局对象。

- 2.第二种是方法调用模式，如果一个函数作为一个对象的方法来调用时，this 指向这个对象。

- 3.第三种是构造器调用模式，如果一个函数用 new 调用时，函数执行前会新创建一个对象，this 指向这个新创建的对象。

- 4.第四种是 apply 、 call 和 bind 调用模式，这三个方法都可以显示的指定调用函数的 this 指向。其中 apply 方法接收两个参数：一个是 this 绑定的对象，一个是参数数组。call 方法接收的参数，第一个是 this 绑定的对象，后面的其余参数是传入函数执行的参数。也就是说，在使用 call() 方法时，传递给函数的参数必须逐个列举出来。bind 方法通过传入一个对象，返回一个 this 绑定了传入对象的新函数。这个函数的 this 指向除了使用 new 时会被改变，其他情况下都不会改变。

- 补充箭头函数没有自己的this，其内部this指向定义时所在作用域外层作用域相关联的执行上下文中的this。

  箭头函数除了没有自己的this之外，还没有arguments(如果一定要用可以使用rest参数代替)、super（指向当前对象的原型对象）、

  new.target(一般用在构造函数中，返回new命令作用于的那个构造函数)

```
这四种方式，使用构造器调用模式的优先级最高，然后是 apply 、 call 和 bind 调用模式，然后是方法调用模式，然后是函数调用模式。
```

[《JavaScript 深入理解之 this 详解》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8Bthis%E8%AF%A6%E8%A7%A3.html)

**补充：箭头函数的使用**：

```
let sum = (a,b) => a+b;
let sum = (a,b) => (a+b);
let sum = (a,b) => {return a+b};
function sum(a,b){return a+b};

这四种是等价的：
要么箭头直接a+b或者(a+b)，要么{return a+b}，应为花括号会被解析我代码块，那你代码块能不就必须要有return语句
一般只有在代码块部分有多条语句的时候，才使用花括号，且花括号内部一定要有return
let sum = (a,b) => (a+b,a+1);这里return出来的是a+1
```

#### 39. eval 是做什么的？

```
它的功能是把对应的字符串解析成 JS 代码并运行。

应该避免使用 eval，不安全，非常耗性能（2次，一次解析成 js 语句，一次执行）。
```

编译性语言：**只须编译一次**就可以把源代码编译成机器语言

解释性语言：源代码不能直接翻译成机器语言，而是先翻译成中间代码，再由解释器对中间代码进行解释运行

源代码—>中间代码—>机器语言

详细资料可以参考：
[《eval()》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/eval)

#### 40. 什么是 DOM 和 BOM？

```
DOM 指的是文档对象模型，它指的是把文档当做一个对象来对待，这个对象主要定义了处理网页内容的方法和接口。

BOM 指的是浏览器对象模型，它指的是把浏览器当做一个对象来对待，这个对象主要定义了与浏览器进行交互的法和接口。BOM
的核心是 window，而 window 对象具有双重角色，它既是通过 js 访问浏览器窗口的一个接口，又是一个 Global（全局）
对象。这意味着在网页中定义的任何对象，变量和函数，都作为全局对象的一个属性或者方法存在。window 对象含有 locati
on 对象、navigator 对象、screen 对象等子对象，并且 DOM 的最根本的对象 document 对象也是 BOM 的 window 对
象的子对象。
```

详细资料可以参考：
[《DOM, DOCUMENT, BOM, WINDOW 有什么区别?》](https://www.zhihu.com/question/33453164)
[《Window 对象》](http://www.w3school.com.cn/jsref/dom_obj_window.asp)
[《DOM 与 BOM 分别是什么，有何关联？》](https://www.zhihu.com/question/20724662)
[《JavaScript 学习总结（三）BOM 和 DOM 详解》](https://segmentfault.com/a/1190000000654274#articleHeader21)

#### 41. 写一个通用的事件侦听器函数。

```js
const EventUtils = {
  // 使其可以分别使用dom0||dom2||IE方式 来绑定事件...
  // 添加事件
  addEvent: function(element, type, handler) {
    if (element.addEventListener) {
      element.addEventListener(type, handler, false);
    } else if (element.attachEvent) {
      element.attachEvent("on" + type, handler);
    } else {
      element["on" + type] = handler;
    }
  },

  // 移除事件
  removeEvent: function(element, type, handler) {
    if (element.removeEventListener) {
      element.removeEventListener(type, handler, false);
    } else if (element.detachEvent) {
      element.detachEvent("on" + type, handler);
    } else {
      element["on" + type] = null;
    }
  },

  // 获取事件目标
  getTarget: function(event) {
    return event.target || event.srcElement;
  },

  // 获取 event 对象的引用，取到事件的所有信息，确保随时能使用 event
  getEvent: function(event) {
    return event || window.event;
  },

  // 阻止事件（主要是事件冒泡，因为 IE 不支持事件捕获）
  stopPropagation: function(event) {
    if (event.stopPropagation) {
      event.stopPropagation();
    } else {
      event.cancelBubble = true;
    }
  },

  // 取消事件的默认行为
  preventDefault: function(event) {
    if (event.preventDefault) {
      event.preventDefault();
    } else {
      event.returnValue = false;
    }
  }
};
```

详细资料可以参考：
[《JS 事件模型》](https://segmentfault.com/a/1190000006934031#articleHeader6)

#### 43. 事件是什么？IE 与火狐的事件机制有什么区别？ 如何阻止冒泡？

- 1.事件是用户操作网页时发生的交互动作，比如 click/move， 事件除了用户触发的动作外，还可以是文档加载，窗口滚动和大小调整。事件被封装成一个 event 对象，包含了该事件发生时的所有相关信息（ event 的属性）以及可以对事件进行的操作（ event 的方法）。
- 2.事件处理机制：IE 支持事件冒泡、Firefox 同时支持两种事件模型，也就是：事件冒泡和事件捕获。
- 3.阻止事件冒泡event.stopPropagation() 或者 ie 下的属性 event.cancelBubble = true;
- 4.阻止事件默认行为event.preventDefault() 或者ie下的属性 event.returnValue = false；

详细资料可以参考：
[《Javascript 事件模型系列（一）事件及事件的三种模型》](https://www.cnblogs.com/lvdabao/p/3265870.html)
[《Javascript 事件模型：事件捕获和事件冒泡》](https://blog.csdn.net/wuseyukui/article/details/13771493)

#### 42. 三种事件模型是什么？

```
事件是用户操作网页时发生的交互动作或者网页本身的一些操作，现代浏览器一共有三种事件模型。

第一种事件模型是最早的 DOM0 级模型，这种模型不会传播，所以没有事件流的概念，但是现在有的浏览器支持以冒泡的方式实
现，它可以在网页中直接定义监听函数，也可以通过 js 对象属性来指定监听函数。这种方式是所有浏览器都兼容的。

第二种事件模型是 IE 事件模型，在该事件模型中，一次事件共有两个过程，事件处理阶段，和事件冒泡阶段。事件处理阶段会首先执行目标元素绑定的监听事件。然后是事件冒泡阶段，冒泡指的是事件从目标元素冒泡到 document，依次检查经过的节点是否绑定了事件监听函数(事件处理程序)，如果有则执行。这种模型通过 attachEvent 来添加监听函数，可以添加多个监听函数，会按顺序依次执行。

第三种是 DOM2 级事件模型，在该事件模型中，一次事件共有三个过程，第一个过程是事件捕获阶段。捕获指的是事件从 document 一直向下传播到目标元素，依次检查经过的节点是否绑定了事件监听函数，如果有则执行。后面两个阶段和 IE 事件模型的两个阶段相同。这种事件模型，事件绑定的函数是 addEventListener，其中第三个参数可以指定事件是否在捕获阶段执行。
```

详细资料可以参考：
[《一个 DOM 元素绑定多个事件时，先执行冒泡还是捕获》](https://blog.csdn.net/u013217071/article/details/77613706)

#### 44. 事件委托是什么？

```
事件委托本质上是利用了事件冒泡的机制。因为事件在冒泡过程中会上传到父节点，并且父节点可以通过事件对象获取到目标节点，因此可以把子节点的监听函数定义在父节点上，由父节点的监听函数统一处理多个子元素的事件，这种方式称为事件代理。这种方式不必要为每一个子元素都绑定一个监听事件，这样减少了内存上的消耗。并且还可以实现事件的动态绑定，比如说新增了一个子节点，我们并不需要单独地为它添加一个监听事件，直接将其交由父节点的事件处理函数即可。
```

详细资料可以参考：
[《JavaScript 事件委托详解》](https://zhuanlan.zhihu.com/p/26536815)

#### 45. ["1", "2", "3"].map(parseInt) 答案是多少？

```
parseInt() 将字符串解析为整数，有两个参数 (val, radix)，其中 radix 表示要解析的数字的基数
（该值介于 2 ~ 36 之间，如果是0的话就按十进制解析，且指定基数后字符串中不能出现比基数大的数值）。

此处 map 传了 3 个参数 (element, index, array)，默认第三个参数被忽略掉，因此三次传入的参数分别为 "1-0", "2-1", "3-2"

"1-0"  基数radix为0 按照十进制去解析字符串 解析为1
"2-1"  基数radix不能为1 解析为NaN
"3-2"  基数radix为2 按照2进制解析字符串‘3’，但是字符串3不是2进制的形式，二进制形式只能出现0、1，所以解析为非数值 NaN
```

详细资料可以参考：
[《为什么 ["1", "2", "3"].map(parseInt) 返回 [1,NaN,NaN]？》](https://blog.csdn.net/justjavac/article/details/19473199)

#### 46. 什么是闭包，为什么要用它？

```
闭包是指有权访问另一个函数作用域中变量的函数，创建闭包的最常见的方式就是在一个函数内创建另一个函数，创建的函数可以
访问到其定义时所处函数作用域的局部变量。

闭包有两个常用的用途。

闭包的第一个用途是使我们在函数外部能够访问到函数内部的变量。

保留对父级执行上下文变量对象的引用，也正因为闭包函数保留了这个变量对象的引用，所以这个变量对象不会被回收。
```

详细资料可以参考：
[《JavaScript 深入理解之闭包》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8B%E9%97%AD%E5%8C%85.html)

#### 47. javascript 代码中的 "use strict"; 是什么意思 ? 使用它区别是什么？

相关知识点：

```
use strict 指定JS在严格模式下运行，设立"严格模式"的目的，主要有以下几个：
```

- 消除 Javascript 语法的一些不合理、不严谨之处，减少一些怪异行为;
- 消除代码运行的一些不安全之处，保证代码运行的安全；
- 提高编译器效率，增加运行速度；
- 为未来新版本的 Javascript 做好铺垫。

区别：

- 1.禁止使用 with 语句。
- 2.禁止 this 关键字指向全局对象。
- 3.对象不能有重名的属性。

我认为严格模式代表了 js 一种更合理、更安全、更严谨的发展方向。

详细资料可以参考：
[《Javascript 严格模式详解》](http://www.ruanyifeng.com/blog/2013/01/javascript_strict_mode.html)

#### 48. 如何判断一个对象是否属于某个类？

```
第一种方式是使用 instanceof 运算符来判断构造函数的 prototype 属性是否出现在对象的原型链中的任何位置。

第二种方式通过对象的 constructor 属性来判断，对象的 constructor 属性指向该对象的构造函数，但是该方式不是很安全，因为 constructor 属性可以被改写。

第三种方式，如果需要判断的是某个内置的引用类型的话，可以使用 Object.prototype.toString() 方法来打印对象的[[Class]] 属性来进行判断。
```

详细资料可以参考：
[《js 判断一个对象是否属于某一类》](https://blog.csdn.net/haitunmin/article/details/78418522)

#### 49. instanceof 的作用？

```js
// instanceof 运算符用于判断构造函数的 prototype 属性是否出现在对象的原型链上。
// 实现：

function myInstanceof(left, right) {
  let proto = Object.getPrototypeOf(left), // 获取对象的原型
    prototype = right.prototype; // 获取构造函数的 prototype 对象

  // 判断构造函数的 prototype 对象是否在对象的原型链上
  while (true) {
    if (!proto) return false;
    if (proto === prototype) return true;

    proto = Object.getPrototypeOf(proto);
  }
}
```

详细资料可以参考：
[《instanceof》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/instanceof)

#### 50. new 操作符具体干了什么呢？如何实现？

```js
// （1）首先创建了一个新的空对象
// （2）设置原型，将对象的原型设置为函数的 prototype 对象。
// （3）让函数的 this 指向这个对象，执行构造函数的代码（为这个新对象添加属性）
// （4）判断函数的返回值类型，如果是值类型，返回创建的对象。如果是引用类型，就返回这个引用类型的对象。

// 实现:
// objectFactory(构造函数, 初始化参数);
function objectFactory() {
  //创建一个空对象
  let newObject = null,
    //类数组对象arguments间接调用数组shift方法获取第一个参数(构造函数)
    constructor = Array.prototype.shift.call(arguments),
    //构造函数执行的结果初始为null
    result = null;

  // 判断传入的第一个参数是否为函数类型
  if (typeof constructor !== "function") {
    console.error("type error");
    return;
  }

  // 将新建空对象的原型指向构造函数的 prototype 对象
  newObject = Object.create(constructor.prototype);

  // 将函数执行上下文的this 指向新建对象，并执行函数
  result = constructor.apply(newObject, arguments);

  // 判断函数执行的返回值，如果是原始值则返回新创建的对象，如果是引用类型的对象则返回该引用类型的对象
  let flag =
    //result不管是一般(null\undefined除外)的原始值还是引用类型，短路&&前面的操作数都是true，则直接取第二个操作数
    result && (typeof result === "object" || typeof result === "function");

  // 这里判断第二个操作数，如果result为原始值，则flag为假则返回创建的对象
  // 如果result为引用类型的对象，则flag为真则返回该引用类型的对象
  return flag ? result : newObject;
}
```

```js
// 构造函数：
// new调用时，this指向新创建出来的对象
// 作为普通函数调用时，this指向window，这就造成了全局环境的污染
// 可以在构造函数内部判断this的指向，来避免全局环境的污染
function Person(name, age, job){
    if (this instanceof Person){
        this.name = name;
        this.age = age;
        this.job = job;
		console.log('this 指向： ',this)
    } else {
    	return new Person(name, age, job);
    }
}
```

详细资料可以参考：
[《new 操作符具体干了什么？》](https://segmentfault.com/a/1190000008576048)
[《JavaScript 深入之 new 的模拟实现》](https://github.com/mqyqingfeng/Blog/issues/13)

#### 51. Javascript 中，有一个函数，执行对象查找时，永远不会去查找原型，这个函数是？

```
hasOwnProperty 方法可以用来检测一个对象是否含有特定的自身属性，和in 运算符不同，该方法会忽略掉那些从原型链上继承到的属性。
```

详细资料可以参考：
[《Object.prototype.hasOwnProperty()》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty)

#### 52. 对于 JSON 的了解？

Html用于数据内容的展示、XML用于内容数据的传递。

JSON更轻量更简洁，XML更规范，个人觉得JSON用于数据的传递比较好，因为JSON的结构更容易**映射**至一般语言的数据结构

```
JSON 是一种数据交换格式(所谓格式就是规范你的数据要怎么表示，数据是同一个但是格式却可以有各种各样的)，基于文本(基于文本的数据格式常称为JSON字符串)，优于轻量，用于交换数据(独立与语言基于文本广泛应用于数据交互)。

在项目开发中，我们使用 JSON 作为前后端数据交换的方式。在前端我们通过将一个符合 JSON 格式的数据结构序列化为 JSON 字符串，然后将它传递到后端，后端通过 JSON 格式的字符串解析后生成对应的数据结构，以此来实现前后端数据的一个传递。
(前端JS对象用于包装要传递的数据，然后将JS对象转化为JSON字符串，再发送请求到后端，后端解析JSON字符串为后端的数据结构对象
前端JS对象===》传输JSON字符串====》后端数据结构对象)

因为 JSON 的语法(格式)是基于 js 的，因此很容易将 JSON 和 js 中的对象弄混，但是我们应该注意的是 JSON 和 js 中的对象不是一回事，是两个本质不同的东西。JSON是可以传输的，因为它是文本格式，但是JS对象是没办法传输的，在语法上，JSON也会更加严格，但是JS对象就很松了，比如说在 JSON 中属性值不能为函数，不能出现 NaN 这样的属性值等，因此大多数的 js 对象是不符合 JSON 对象的格式的。

在 js 中提供了两个函数来实现 js 数据结构和 JSON 格式的转换处理，一个是 JSON.stringify 函数，将JS对象转换为一个 JSON 字符串。

JSON.parse() 函数，这个函数用来将 JSON 格式的字符串转换为一个 js 数据结构，如果传入的字符串不是标准的 JSON 格式的字符串的话，将会抛出错误。
```

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/Snipaste_2021-06-14_13-59-49.png" style="zoom:80%;" />

JSON.Stringify()将JS转换为JSON字符串的相关规则：

- 键名不是双引号的（包括没有引号或者是单引号），会自动变成双引号；字符串是单引号的，会自动变成双引号

- 最后一个属性后面有逗号的，会被自动去掉

- 非数组对象的属性不能保证以特定的顺序出现在序列化后的字符串中 
  这个好理解，也就是对非数组对象在最终字符串中不保证属性顺序和原来一致

- 布尔值、数字、字符串的包装对象在序列化过程中会自动转换成对应的原始值 
  也就是你的什么new String(“bala”)会变成”bala”，new Number(2017)会变成2017

- undefined、任意的函数（其实有个函数会发生神奇的事，后面会说）以及 symbol 值（symbol详见ES6对symbol的介绍）

  - 出现在非数组对象的属性值中：在序列化过程中会被忽略

  - 出现在数组中时：被转换成 null

    JSON.stringify({x: undefined, y: function(){return 1;}, z: Symbol("")});  

    //出现在非数组对象的属性值中被忽略："{}"

    JSON.stringify([undefined, Object, Symbol("")]);  

    //出现在数组对象的属性值中，变成null："[null,null,null]"

- NaN、Infinity和-Infinity，不论在数组还是非数组的对象中，都被转化为null

- 所有以 symbol 为属性键的属性都会被完全忽略掉，即便 replacer 参数中强制指定包含了它们

- 不可枚举的属性会被忽略

详细资料可以参考：
[《深入了解 JavaScript 中的 JSON 》](https://my.oschina.net/u/3284240/blog/874368)

#### 53. `[].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})` 能解释一下这段代码的意思吗？

```
（1）选取页面所有 DOM 元素。在浏览器的控制台中可以使用$$()方法来获取页面中相应的元素，这是现代浏览器提供的一个命令行 API 相当于 document.querySelectorAll 方法。

（2）循环遍历 DOM 元素

（3）给元素添加 outline 。由于渲染的 outline 是不在 CSS 盒模型中的，所以为元素添加 outline 并不会影响元素的大小和页面的布局。

（4）生成随机颜色函数。Math.random()*(1<<24) 可以得到 0~2^24 - 1 之间的随机数，因为得到的是一个浮点数，但我们只需要整数部分，使用取反操作符 ~ 连续两次取反获得整数部分，然后再用 toString(16) 的方式，转换为一个十六进制的字符串。
```

outline是轮廓线，和border不同，他不占据空间 并不会影响元素的大小和页面的布局，它就沿着border环绕一圈，它谁都不影响。
详细资料可以参考：
[《通过一行代码学 JavaScript》](https://2008winstar.iteye.com/blog/2128290)

#### 54. js 延迟加载的方式有哪些？

```
js 延迟加载，最直观的解释也就是等页面加载完成之后再加载javaScript 文件。由于js 的加载、解析和执行会阻塞页面的渲染过程，因此我们希望 js 脚本能够尽可能的延迟加载，从而提高首屏加载速度。

我了解到的几种方式是：

第一种方式是我们一般采用的是将 js 脚本放在文档的底部，来使 js 脚本尽可能的在最后来加载执行。

第二种方式是给 js 脚本添加 defer 属性，这个属性会让脚本的加载与文档的解析同步解析，然后在文档解析完成后再执行这个脚本文件，这样的话就能使页面的渲染不被阻塞。多个设置了 defer 属性的脚本按规范来说最后是顺序执行的，但是在一些浏览器中可能不是这样。

第三种方式是给 js 脚本添加 async 属性，这个属性会使脚本异步加载，不会阻塞页面的解析过程，但是当脚本加载完成后立即执行 js 脚本，这个时候如果文档没有解析完成的话同样会阻塞。多个 async 属性的脚本的执行顺序是不可预测的，一般不会按照代码的顺序依次执行。

第四种方式是动态创建 DOM 标签的方式，我们可以对文档的加载事件进行监听，当文档加载完成后再动态的创建 script 标签来引入 js 脚本。
```

详细资料可以参考：
[《JS 延迟加载的几种方式》](https://blog.csdn.net/meijory/article/details/76389762)
[《HTML 5 `<script>` `async` 属性》](http://www.w3school.com.cn/html5/att_script_async.asp)

#### 55. Ajax 是什么? 如何创建一个 Ajax？

相关知识点：

AJax是一种脚本化Http的Web应用架构，它是 Asynchronous JavaScript and XML 的缩写，指的是通过 JavaScript 的异步通信，从服务器获取 XML 文档从中提取数据，再更新当前网页的对应部分，而不用刷新整个网页。

具体来说，AJAX 包括以下几个步骤。

- 1.创建 XMLHttpRequest 对象，也就是创建一个异步调用对象

- 2.创建一个新的 HTTP 请求，并指定该 HTTP 请求的方法、URL 及验证信息 xhr.open()

  post请求方式时还需要通过xhr.setRequestHeader()来告知服务器端请求参数的格式

  application/x-www-form-urlencoded 属性名=属性值 多对之间用&连接的 一般请求参数格式

  application/json  json字符串的请求参数格式

- 3.设置响应 HTTP 请求的onload事件监听函数

  (也可以是onreadystatechange 监听状态变化的监听函数，但是已经过时了，其状态码为4时就表示拿到服务器端返回的数据)

- 4.发送 HTTP 请求 xhr.send

- 5.获取异步调用返回的数据 xhr.responseText

- 6.根据拿到的数据使用 JavaScript 和 DOM 实现局部页面内容的无刷新更新

一般实现：

```js
// 1.创建ajax对象
var xhr = new XMLHttpRequest();
// 2.告诉Ajax对象要向哪发送请求，以什么方式发送请求
// 1)请求方式 2)请求地址
// open的第三个参数改为false，让他强行同步，就是拿不到结果就一直阻断着
xhr.open('get', 'http://localhost:3000/first');
// 3.获取服务器端响应到客户端的数据
xhr.onload = function (){
	console.log(xhr.responseText)
}
// 4.发送请求
xhr.send();

//=====================readyStateChange事件==============
const SERVER_URL = "/server";
let xhr = new XMLHttpRequest();
// 创建 Http 请求
xhr.open("GET", SERVER_URL, true);
// 设置状态监听函数
xhr.onreadystatechange = function() {
  if (this.readyState !== 4) return;
  // 当请求成功时
  if (this.status === 200) {
    handle(this.response);
  } else {
    console.error(this.statusText);
  }
};
// 设置请求失败时的监听函数
xhr.onerror = function() {
  console.error(this.statusText);
};
// 设置请求头信息
xhr.responseType = "json";
xhr.setRequestHeader("Accept", "application/json");
// 发送 Http 请求
xhr.send(null);
```

详细资料可以参考：
[《XMLHttpRequest 对象》](https://wangdoc.com/javascript/bom/xmlhttprequest.html)
[《从 ajax 到 fetch、axios》](https://juejin.im/post/5acde23c5188255cb32e7e76)
[《Fetch 入门》](https://juejin.im/post/5c160937f265da61180199b2)
[《传统 Ajax 已死，Fetch 永生》](https://segmentfault.com/a/1190000003810652)

fetch是浏览器提供的一个底层api，实际上就相当于底层的XmlHttpRequest

fetch('路径'，{method：，...其他配置规则的键值对}).then(data=>{data.text}).then(res=>console.log(res))

axios是一个封装库，是其底层是对XmlHttpRequest封装

axios.get('路径'，{params：{get请求参数的键值对}}).then(ret=>console.log(ret.data))

axios.post('路径'，{post请求参数的键值对}).then(ret=>console.log(ret.data))

且传递的参数默认是json字符串的格式

```
关于axios、ajax和fetch的总结

首先fetch和ajax是属于同一层次的，都是浏览器提供的api，然后fetch是promise实现支持promise相关api所以操作相比ajax而言，简单一点。

axios是第三方封装库，是基于promise对ajax的封装，操作简单，功能强大，且更为安全。

来看fetch存在哪些问题：

相比axios而言功能不够强大、
只有网络请求本身出问题才reject、像状态码为400、500这样的不会触发
然后就是没有办法原生监测请求的进度，而XHR可以
fetch默认不会带cookie，需要添加配置项： fetch(url, {credentials: 'include'})

axios相比fetch来说
安全，可有效对抗CSRF攻击；
功能强大支持拦截器，包括请求拦截器，响应拦截器。还能取消请求
对服务器端返回的JSON字符串会自动解析为js对象
axios既可以作为函数使用也可以作为对象使用，操作更为方便

补充请求拦截器添加token对抗CSRF攻击 config.head.Authorization = localstorage.token

补充axios可以作为对象和函数使用：
Axios作为构造函数，axios实例并不是由它直接new出来的，Axios new 出来的实例绑定上request方法返回的一个方法才是我们的axios。为了让axios上拥有Axios原型对象上的方法，还要将方法啥的一个个添加，最后返回。
所以得到的axios可以作为函数使用，也可以作为对象直接调用上面的属性和方法。

补充axios发送请求：
axios发送请求，实际上用到了其所被绑定的request函数，进一步的request函数里面的dispatch函数(dispatch函数是放到request里chain数组中的，只有拿到了它才会执行)才会去找xhr适配器或者http适配器去供客户端或服务器端使用，xhr适配器就是利用promise封装的xhr，利用它客户端就可以发送ajax请求了。

补充请求拦截器和响应拦截器：
请求拦截器1、请求拦截器2、响应拦截器1、响应拦截器2
问执行顺序？
请求拦截器2的回调执行
请求拦截器1的回调执行
响应拦截器1的回调执行
响应拦截器2的回调执行
首先请求拦截器对象.use会将一组成功、失败的回调函数放入该拦截器对象对应的handler数组中
同理相应拦截器也一样
接下来重点就是和axios同样功能的request函数！
他会将拦截器对象handler数组中放入的回调一组组的拿出来放入自己的chain数组中，
只不过不同拦截器对象其放入的方式不一样：
请求拦截器会将每组回调unshift从头部压入数组
响应拦截器会将每组回调push从尾部压入数组
所以chain中关于拦截器回调的顺序就变成了 请2 请1 响1 响2
之后遍历这个数组从头部逐个拿出来加以执行，这就是为啥会有上面这样执行顺序的原因了。
```

```
axios是一个基于Promise 用于浏览器和 nodejs 的 HTTP 客户端，本质上也是对原生XHR的封装，只不过它是Promise的实现版本，符合最新的ES规范，它本身具有以下特征：

1. 从浏览器中创建 XMLHttpRequest
2. 支持 Promise API
3. 客户端支持防止CSRF
4. 提供了一些并发请求的接口（重要，方便了很多的操作）
5. 从 node.js 创建 http 请求
6. 拦截请求和响应
7. 转换请求和响应数据
8. 取消请求
9. 自动转换JSON数据(将服务器端返回的JSON数据自动解析为直接可以使用的JS对象)

二、fetch存在问题
fetch是一个低层次的API，你可以把它考虑成原生的XHR，所以使用起来并不是那么舒服，需要进行封装。

1. fetch只对网络请求报错，对400，500都当做成功的请求，服务器返回 400，500 错误码时并不会 reject，只有网络错误这些导致请求不能完成时，fetch 才会被 reject。
2. fetch默认不会带cookie，需要添加配置项： fetch(url, {credentials: 'include'})
3. fetch不支持abort，不支持超时控制，使用setTimeout及Promise.reject的实现的超时控制并不能阻止请求过程继续在后台运行，造成了流量的浪费
4. fetch没有办法原生监测请求的进度，而XHR可以
```

**axios底层对xhr对象的封装**

![](C:\Users\88520\Desktop\前端\3.面试\blog-master\img/56llll.png)

![](https://gitee.com/chenyipeng9/blog/raw/master/img/345d3saf.png)

![](https://gitee.com/chenyipeng9/blog/raw/master/img/kjasfgk55.png)

#### 56. 谈一谈浏览器的缓存机制？

http报文：

请求报文：请求行+请求首部+请求主体

响应报文：状态行+响应首部+响应主体

常见的请求首部(11个)(请求头)：

请求方式 + 请求的目标资源、Accept、Accept-Encoding、Accept-language、Host、Connection、Reffer、Date、Cookie、user-Agent、if-modify-since

常见的响应首部(18个)(响应头)：

协议 版本号 状态码 描述信息、 server、location、content-encoding、content-length、content-language、content-type、content-disposation

set-ccokie、refersh、transfer-encoding、last-modify、

catch-control、expires、no-programe

Date、connectioin、user-agent

```
浏览器的缓存机制指的是通过在一段时间内保留已接收到的 web 资源的一个副本，如果在资源的有效时间内，发起了对这个资源的再一次请求，那么浏览器会直接使用缓存的副本，而不是向服务器发起请求。使用 web 缓存可以有效地提高页面的打开速度，减少不必要的网络带宽的消耗。

web 资源的缓存策略一般由服务器来指定，可以分为两种，分别是强缓存策略和协商缓存策略。

使用强缓存策略时，如果缓存资源有效，则直接使用缓存资源，不必再向服务器发起请求。强缓存策略可以通过两种方式来设置，分别是 http 头信息中的 Expires 属性和 Cache-Control 属性。

服务器通过在响应头中添加 Expires 属性，来指定资源的过期时间。在过期时间以内，该资源可以被缓存使用，不必再向服务器发送请求。这个时间是一个绝对时间，它是服务器的时间，因此可能存在这样的问题，就是客户端的时间和服务器端的时间不一致，或者用户可以对客户端时间进行修改的情况，这样就可能会影响缓存命中的结果。

Expires 是 http1.0 中的方式，因为它的一些缺点，在 http 1.1 中提出了一个新的头部属性就是 Cache-Control 属性，
它提供了对资源的缓存的更精确的控制。它有很多不同的值，常用的比如我们可以通过设置 max-age 来指定资源能够被缓存的时间
的大小，这是一个相对的时间，它会根据这个时间的大小和资源第一次请求时的时间来计算出资源过期的时间，因此相对于 Expires
来说，这种方式更加有效一些。常用的还有比如 private ，用来规定资源只能被客户端缓存，不能够代理服务器所缓存。还有如 n
o-store ，用来指定资源不能够被缓存，no-cache 代表该资源能够被缓存，但是立即失效，每次都需要向服务器发起请求。

一般来说只需要设置其中一种方式就可以实现强缓存策略，当两种方式一起使用时，Cache-Control 的优先级要高于 Expires 。

使用协商缓存策略时，会先向服务器发送一个请求，如果资源没有发生修改，则返回一个 304 状态，让浏览器使用本地的缓存副本。
如果资源发生了修改，则返回修改后的资源。协商缓存也可以通过两种方式来设置，分别是 http 头信息中的 Etag 和 Last-Modified 属性。

服务器通过在响应头中添加 Last-Modified 属性来指出资源最后一次修改的时间，当浏览器下一次发起请求时，会在请求头中添加一个 If-Modified-Since 的属性，属性值为上一次资源返回时的 Last-Modified 的值。当请求发送到服务器后服务器会通过这个属性来和资源的最后一次的修改时间来进行比较，以此来判断资源是否做了修改。如果资源没有修改，那么返回 304 状态，让客户端使用本地的缓存。如果资源已经被修改了，则返回修改后的资源。使用这种方法有一个缺点，就是 Last-Modified 标注的最后修改时间只能精确到秒级，如果某些文件在1秒钟以内，被修改多次的话，那么文件已将改变了但是 Last-Modified 却没有改变，
这样会造成缓存命中的不准确。

因为 Last-Modified 的这种可能发生的不准确性，http 中提供了另外一种方式，那就是 Etag 属性。服务器在返回资源的时候，在头信息中添加了 Etag 属性，这个属性是资源生成的唯一标识符，当资源发生改变的时候，这个值也会发生改变。在下一次资源请求时，浏览器会在请求头中添加一个 If-None-Match 属性，这个属性的值就是上次返回的资源的 Etag 的值。服务接收到请求后会根据这个值来和资源当前的 Etag 的值来进行比较，以此来判断资源是否发生改变，是否需要返回资源。通过这种方式，比 Last-Modified 的方式更加精确。

当 Last-Modified 和 Etag 属性同时出现的时候，Etag 的优先级更高。使用协商缓存的时候，服务器需要考虑负载平衡的问题，因此多个服务器上资源的 Last-Modified 应该保持一致，因为每个服务器上 Etag 的值都不一样，因此在考虑负载平衡时，最好不要设置 Etag 属性。

强缓存策略和协商缓存策略在缓存命中时都会直接使用本地的缓存副本，区别只在于协商缓存会向服务器发送一次请求。它们缓存不命中时，都会向服务器发送请求来获取资源。在实际的缓存机制中，强缓存策略和协商缓存策略是一起合作使用的。浏览器首先会根据请求的信息判断，强缓存是否命中，如果命中则直接使用资源。如果不命中则根据头信息向服务器发起请求，使用协商缓存，如果协商缓存命中的话，则服务器不返回资源，浏览器直接使用本地资源的副本，如果协商缓存不命中，则浏览器返回最新的资源给浏览器。
```

详细资料可以参考：
[《浅谈浏览器缓存》](https://segmentfault.com/a/1190000012573337)
[《前端优化：浏览器缓存技术介绍》](https://juejin.im/post/5b9346dcf265da0aac6fbe57#heading-3)
[《请求头中的 Cache-Control》](https://www.web-tinker.com/article/21221.html)
[《Cache-Control 字段值详解》](https://juejin.im/post/5c2d6c9ae51d450cf4195a08)

#### 57. Ajax 解决浏览器缓存问题？(X)

- 1.在 ajax 发送请求前加上 anyAjaxObj.setRequestHeader("If-Modified-Since","0")。

- 2.在 ajax 发送请求前加上 anyAjaxObj.setRequestHeader("Cache-Control","no-cache")。

- 3.在 URL 后面加上一个随机数： "fresh=" + Math.random();。

- 4.在 URL 后面加上时间戳："nowtime=" + new Date().getTime();。

- 5.如果是使用 jQuery，直接这样就可以了\$.ajaxSetup({cache:false})。这样页面的所有 ajax 都会执行这条语句就是不需要保存缓存记录。

详细资料可以参考：
[《Ajax 中浏览器的缓存问题解决方法》](https://www.cnblogs.com/cwzqianduan/p/8632009.html)
[《浅谈浏览器缓存》](https://segmentfault.com/a/1190000012573337)

#### 58. 同步和异步的区别？

相关知识点：

```
同步：任务是连续执行的，不能插入其他任务，即处于阻塞状态，只有连续的任务执行完了，才会接着执行其他任务。

异步：任务是不连续执行的，比如将一个任务分成两段，先执行任务的第一段，然后转而执行其他任务，这样就不会阻塞其他任务的执行，等满足了一定的条件在执行任务的第二段
```

详细资料可以参考：
[《同步和异步的区别》](https://blog.csdn.net/tennysonsky/article/details/45111623)

#### 59. 什么是浏览器的同源政策？

```
我对浏览器的同源政策的理解是，JS脚本只能读取和所属文档来源相同域下的资源内容。这里的同源的指的是两个域的协议、域名、端口号必须相同，否则则不属于同一个域。

脚本本身的来源和同源策略并不相关，相关的是脚本所嵌入的文档的来源。同源政策主要限制了三个方面

第一个是当前域下的 js 脚本不能够访问其他域下的 cookie、localStorage 和 indexDB。

第二个是当前域下的 js 脚本不能够操作访问操作其他域下的 DOM。

第三个是当前域下 ajax 无法发送跨域请求。

同源政策的目的主要是为了保证用户的信息安全，它是对 js 脚本所属文档来源的一种限制，并不是对浏览器的限制，对于一般的 img、或者
script 脚本请求都不会有跨域的限制，这是因为这些操都不太可能会出现安全问题。
```

#### 60. 如何解决跨域问题？

相关知识点：

- 1. 通过 jsonp 跨域
- 2. document.domain + iframe 跨域
- 3. location.hash + iframe
- 4. window.name + iframe 跨域
- 5. postMessage 跨域
- 6. 跨域资源共享（CORS)
- 7. nginx 代理跨域
- 8. nodejs 中间件代理跨域
- 9. WebSocket 协议跨域

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-06-27_09-25-41.png" style="zoom: 67%;" />

回答：

```
解决跨域的方法我们可以根据我们想要实现的目的来划分。

实现主域名下的不同子域名的跨域操作，我们可以使用设置 document.domain 来解决。

（1）document.domain可以放宽同源政策的限制，在不同子域中可以将document.domain值都设置为主域名(example.com)，
来实现不同子域名与主域名之间的跨域操作.
包含多个子域的大站，例如：
home.example.com
developer.example.com
orders.example.com

不同窗口间的跨域通信问题，比如说一个窗口想要和其中不同源的 iframe窗体 进行通信，我们可以使用 location.hash、window.name、postMessage 来解决。

（2）使用 location.hash 的方法，我们可以在窗口页面中动态的修改 iframe 窗体的 hash 值，然后在 iframe 窗体里利用window.hashchange来监听hash值的变化，这就实现了一个单向的通信。由于iframe窗体不能直接修改不同源父级窗口的hash值，所以反过来操作不行。我们可以在 iframe窗体中再加入一个与父级窗口同源的 iframe窗体，以此来实现双向通信。

（3）使用 window.name 的方法，主要是基于同一个窗口中设置了 window.name 后不同源的页面也可以相互访问，这种方式的好处是可以传输的数据量大。

（4）使用 h5 中新增的一个 api 即 postMessage（跨域消息传递）。主要是在一个窗口中调用 postMessage 来发送跨域信息，在另一个窗口中监听message事件 以此来实现不同源窗口间的消息出传递。

如果是像解决 ajax 无法提交跨域请求的问题，我们可以使用 jsonp、cors、websocket 协议、服务器代理来解决问题。

（5）jsonp 利用script标签发起请求没有同源限制的特性来实现的。通过在请求的 url 后指定一个回调函数名称，服务器将数据作为回调函数的实参返回给前端，前端接收到数据后，因为请求的是脚本文件，所以会直接执行，这样我们先前定义好的回调函数就可以被调用，从而实现了跨域请求的处理。这种方式只适用于get 请求。

（6）CORS 全称"跨域资源共享"。CORS 需要浏览器和服务器同时支持。目前，所有浏览器都支持该功能，因此我们只需要在服务器端配置就行。浏览器将 CORS 请求分成两类：简单请求和非简单请求。对于简单请求，浏览器直接发出 CORS 请求。具体来说，就是会在头信息之中，增加一个 Origin 字段。Origin 字段用来说明本次请求来自哪个源。服务器根据这个值，决定是否同意这次请求。对于如果 Origin 指定的源，不在许可范围内，服务器会返回一个正常的 HTTP 回应。浏览器发现，这个回应的头信息没有包含 Access-Control-Allow-Origin 字段，就知道出错了，从而抛出一个错误，ajax 不会收到响应信息。如果成功的话会包含一些以 Access-Control- 开头的字段。

非简单请求，浏览器会先发出一次预检请求，来判断该域名是否在服务器的白名单中，如果收到肯定回复后才会发起请求。

（7）使用 websocket 协议，这个协议没有同源限制。

（8）使用服务器来代理跨域的访问请求，就是有跨域的请求操作时发送请求给后端，让后端代为请求，然后最后将获取的结果发返回。
```

详细资料可以参考：
[《前端常见跨域解决方案（全）》](https://segmentfault.com/a/1190000011145364)
[《浏览器同源政策及其规避方法》](http://www.ruanyifeng.com/blog/2016/04/same-origin-policy.html)
[《跨域，你需要知道的全在这里》](https://juejin.im/entry/59feae9df265da43094488f6)
[《为什么 form 表单提交没有跨域问题，但 ajax 提交有跨域问题？》](https://www.zhihu.com/question/31592553)

#### 61. 服务器代理转发时，该如何处理 cookie？(X)

详细资料可以参考：
[《深入浅出 Nginx》](https://www.jianshu.com/p/5eab0f83e3b4)

#### 62. 简单谈一下 cookie ？

```
我的理解是 cookie在客户端存储服务器端数据，设计之初就是供服务器端使用的因此服务器端可以读写存储于本地的cookie值，常用于验证用户身份，因此每次会随着http请求一同发往服务器端。cookie 一般可以存储 4k 大小的数据属于会话级存储，并且只能够被同源的网页所共享访问。

服务器端可以使用 Set-Cookie 的响应头部来配置 cookie 信息。一条cookie 包括了多个属性其中ame 和 value 分别是 cookie 的名字和值。expires 指定了 cookie 失效的时间，domain 是域名、path是路径，domain 和 path 一起限制了 cookie 能够被哪些 url 访问。

而且这些相关信息并不是原来设置的样子，是经过编码之后的样子，所以获取cookie对应的属性还需要进行相应的解码。

（在发生 Ajax 跨域请求的时候，即使是同源下的 cookie，也不会被自动添加到请求头部，除非显示地规定。）
```

详细资料可以参考：
[《HTTP cookies》 ](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Cookies)
[《聊一聊 cookie》 ](https://segmentfault.com/a/1190000004556040)

#### 63. 模块化开发怎么做？(怎么定义模块)

```
我对模块的理解是，一个模块是实现一个特定功能的一组方法。在最开始的时候，js 只实现一些简单的功能，所以并没有模块的概念
，但随着程序越来越复杂，代码的模块化开发变得越来越重要。我所了解到的定义一个模块的常见写法：

由于函数具有独立作用域的特点，最原始的写法是使用函数来作为模块，几个函数作为一个模块，但是这种方式容易造成全局变量的污
染，并且模块间没有联系。

function m1(){
　　　//...
   }
function m2(){
　　　//...
}

把模块写成一个对象，通过将函数作为一个对象的方法来实现，这样解决了直接使用函数作为模块的一些缺点，但是这种办法会暴露所
有的所有的模块成员(ES6类内部的所有方法也是对外可见，暂不支持私有方法即属性，有个提案是加#。)，外部代码可以修改内部属性的值。

var module1 = new Object({
　　　　_count : 0,
　　　　m1 : function (){
　　　　　　//...
　　　　},
　　　　m2 : function (){
　　　　　　//...
　　　　}
　　});

现在最常用的是立即执行函数的写法，通过利用闭包来实现模块私有作用域的建立，同时不会对全局作用域造成污染。

var module1 = (function(){
　　　　var _count = 0;
　　　　var m1 = function(){
　　　　　　//...
　　　　};
　　　　var m2 = function(){
　　　　　　//...
　　　　};
　　　　return {
　　　　　　m1 : m1,
　　　　　　m2 : m2
　　　　};
　　})();
```

详细资料可以参考：
[《浅谈模块化开发》](https://juejin.im/post/5ab378c46fb9a028ce7b824f)
[《Javascript 模块化编程（一）：模块的写法》](http://www.ruanyifeng.com/blog/2012/10/javascript_module.html)
[《前端模块化：CommonJS，AMD，CMD，ES6》](https://juejin.im/post/5aaa37c8f265da23945f365c)
[《Module 的语法》](http://es6.ruanyifeng.com/#docs/module)

#### 64. js 的几种模块规范？（怎么用模块）

```
js 中现在比较成熟的有四种模块加载方案。

浏览器端的模块化规范：

第一种是 AMD 方案，这种方案采用异步加载的方式来加载模块，模块的加载不影响后面语句的执行，所有依赖这个模块的语句都定
义在一个回调函数里，等到加载完成后再执行回调函数。require.js 实现了 AMD 规范。

第二种是 CMD 方案，这种方案和 AMD 方案都是为了解决异步模块加载的问题，sea.js 实现了 CMD 规范。它和 require.js
的区别在于模块定义时对依赖的处理不同和对依赖模块的执行时机的处理不同。参考60

服务器端的模块化规范：NodeJS
第三种是 CommonJS 方案，针对于服务器端NodeJS而言，通过module.exports和require来输入输出模块，其采用同步的方式来引入模块，因为在服务端文件都存储在本地磁盘，所以读取非常快，所以以同步的方式加载没有问题。

前后端通用的模块化规范：
第四种方案是 ES6 提出的方案，使用 import 和 export 的形式来导入导出模块。参考 61。
```

#### 65. AMD 和 CMD 规范的区别？

它们之间的主要区别有两个方面。

（1）第一个方面是在模块定义时对依赖的处理不同。AMD 推崇依赖前置，在定义模块的时候就要声明其依赖的模块。而 CMD 推崇
就近依赖，只有在用到某个模块的时候再去 require。

（2）第二个方面是对依赖模块的执行时机处理不同。AMD 在依赖模块加载完成后就直接执行依赖模块，依赖模块的执行顺序和我们书写的顺序不一定一致。而 CMD在依赖模块加载完成后并不执行，等到所有的依赖模块都加载好后，进入回调函数逻辑，遇到 require 语句的时候才执行对应的模块，这样模块的执行顺序就和我们书写的顺序保持一致了。

```js
// CMD
define(function(require, exports, module) {
  var a = require("./a");
  a.doSomething();
  // 此处略去 100 行
  var b = require("./b"); // 依赖可以就近书写
  b.doSomething();
  // ...
});

// AMD 默认推荐
define(["./a", "./b"], function(a, b) {
  // 依赖必须一开始就写好
  a.doSomething();
  // 此处略去 100 行
  b.doSomething();
  // ...
});
```

详细资料可以参考：
[《前端模块化，AMD 与 CMD 的区别》](https://juejin.im/post/5a422b036fb9a045211ef789)

#### 66. ES6 模块与 CommonJS 模块、AMD、CMD 的差异。

- CommonJS 模块就是对象，即在输入时是先加载整个模块，生成一个对象，然后再从这个对象上面读取方法。一旦获取到了这个对象，不管你模块内部如何变化，都影响不到他了。
- ES6模块遇到模块加载命令 import，就会生成一个只读引用，等到脚本真正执行时，再根据这个只读引用，到被加载的那个模块里面去取值或方法。

#### 67. requireJS 的核心原理是什么？（如何动态加载的？如何避免多次加载的？如何缓存的？）

```
require.js 的核心原理是通过动态创建 script 脚本来异步引入模块，然后对每个脚本的 load 事件进行监听，如果每个脚本都加载完成了，再调用回调函数。
```

详细资料可以参考：
[《requireJS 的用法和原理分析》](https://github.com/HRFE/blog/issues/10)
[《requireJS 的核心原理是什么？》](https://zhuanlan.zhihu.com/p/55039478)
[《从 RequireJs 源码剖析脚本加载原理》](https://www.cnblogs.com/dong-xu/p/7160919.html)
[《requireJS 原理分析》](https://www.jianshu.com/p/5a39535909e4)

#### 68. JS 模块加载器的轮子怎么造，也就是如何实现一个模块加载器？(X)

详细资料可以参考：
[《JS 模块加载器加载原理是怎么样的？》](https://www.zhihu.com/question/21157540)

#### 69. ECMAScript6 怎么写 class，为什么会出现 class 这种东西?

```
在我看来 ES6 新添加的 class 只是为了补充 js 中缺少的一些面向对象语言的特性，但本质上来说它只是构造函数的语法糖，不是一个新的东西，其背后还是原型继承的思想。通过加入 class 可以有利于我们更好的组织代码。

在 class 中添加的方法，其实是添加在类的原型上的,包括constructor方法
```

详细资料可以参考：
[《ECMAScript 6 实现了 class，对 JavaScript 前端开发有什么意义？》](https://www.zhihu.com/question/29789315)
[《Class 的基本语法》](http://es6.ruanyifeng.com/#docs/class)

#### 70. documen.write 和 innerHTML 的区别？

```
document.write 的内容会代替整个文档内容，会重写整个页面。

innerHTML 的内容只是替代指定元素的内容，只会重写页面中的部分内容。
```

详细资料可以参考：
[《简述 document.write 和 innerHTML 的区别。》](https://www.nowcoder.com/questionTerminal/2c5d8105b2694d85b06eff85e871cf50)

#### 71. DOM 操作——怎样添加、移除、移动、复制、创建和查找节点？

（1）创建新节点

在添加节点之前，要先获取索要天价的节点，可以创建，也可以是复制

```js
createDocumentFragment(node);  
相当于其他节点的一个临时的容器，其特殊之处就在于将一组节点当做一个节点看待，将这个节点添加到文档上，其是是将该文档片段的所有子节点插入到文档
createElement(node);
createTextNode(text);
cloneNode()
```

（2）添加、移除、替换、插入

在父节点上调用这些方法对子节点进行操作

```js
appendChild(node)
removeChild(node)
replaceChild(new,old)
insertBefore(new,old)
```

（3）查找元素

```js
getElementById();
getElementsByName();
getElementsByTagName();   
getElementsByClassName();
querySelector();
querySelectorAll();
```

（4）属性操作

标准属性：dom元素在JS中作为对象的property属性和在html文档中作为标签的attribute属性是同步的。可以直接获取JS对象然后.属性名进行操作

非标准的自定义属性可以用下述方法操作.

```js
getAttribute(key);
setAttribute(key, value);
hasAttribute(key);
removeAttribute(key);
```

(5) 以节点树遍历文档(Node节点对象包含以下相关属性):

parentNode、childNodes、firstChild、lastChild、nexSibiling、previousSibiling、nodeType、

9Document节点 、1Element节点、11DoucmentFragement

详细资料可以参考：
[《DOM 概述》](https://developer.mozilla.org/zh-CN/docs/Web/API/Document_Object_Model/Introduction#DOM_interfaces)
[《原生 JavaScript 的 DOM 操作汇总》](https://harttle.land/2015/10/01/javascript-dom-api.html)
[《原生 JS 中 DOM 节点相关 API 合集》](https://microzz.com/2017/04/06/jsdom/)

#### 72. innerHTML 与 outerHTML 的区别？

```
对于这样一个 HTML 元素：<div>content<br/></div>。

innerHTML：内部 HTML，content<br/>；
outerHTML：外部 HTML，<div>content<br/></div>；
innerText：内部文本，content ；
outerText：内部文本，content ；
```

#### 73. .call() 和 .apply() 的区别？

```
它们的作用一模一样，用于间接调用函数、区别仅在于传入参数的形式的不同。

apply 接受两个参数，第一个参数指定了函数体内 this 对象的指向，第二个参数为一个带下标的集合，这个集合可以为数组，也可以为类数组，apply 方法把这个集合中的元素作为参数传递给被调用的函数。(不同于call方法其将第一个参数后面的参数都放入到一个数组中一次性传给简介调用的函数)

call 传入的参数数量不固定，跟 apply 相同的是，第一个参数也是代表函数体内的 this 指向，从第二个参数开始往后，每个参数被依次传入函数。
```

详细资料可以参考：
[《apply、call 的区别和用途》](https://juejin.im/entry/58d0a7b22f301e007e5a15ae)

#### 74. JavaScript 类数组对象的定义？

```
一个拥有 length 属性和若干索引属性的对象就可以被称为类数组对象，类数组对象和数组类似，但是不能直接调用数组的方法。

常见的类数组对象有 arguments 和 DOM 方法的返回结果。
```

常见的类数组转换为数组的方法有这样几种：

注：slice方法返回截取下来的新数组，且不改变原有的数组；

​		splice方法返回删除后的数组，改变原有的数组

​		concat方法返回拼接后的新数组，且不改变原有的数组，且传入的参数为数组，和直接传入参数起到的		数组拼接效果是一样的：[1,2,3].concat([4,5])-->[1,2,3,4,5]    [1,2,3].concat(4,5)->[1,2,3,4,5]

​		这一点和push不一样: [1,2,3].push(4,5)->[1,2,3,4,5]    [1,2,3].push([4,5])->[1,2,3,[4,5]]

​		push方法执行完返回顶部元素，且可以向数组中同时加入多个元素。

（1）通过 call 调用数组的 slice 方法来实现转换

```js
Array.prototype.slice.call(arrayLike);
```

（2）通过 call 调用数组的 splice 方法来实现转换

```js
Array.prototype.splice.call(arrayLike, 0);
```

（3）通过 apply 调用数组的 concat 方法来实现转换

```js
Array.prototype.concat.apply([], arrayLike);
```

（4）通过 Array.from 方法来实现转换

```js
Array.from(arrayLike);
```

（5）展开运算符 ...，只能将具有iterator接口的类数组对象转换为数组.

原生具有iterator接口的数据类型有：Array、String、Set、Map、nodeList、argument、TypeArray

详细的资料可以参考：
[《JavaScript 深入之类数组对象与 arguments》](https://github.com/mqyqingfeng/Blog/issues/14)
[《javascript 类数组》](https://segmentfault.com/a/1190000000415572)
[《深入理解 JavaScript 类数组》](https://blog.lxxyx.cn/2016/05/07/%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3JavaScript%E7%B1%BB%E6%95%B0%E7%BB%84/)

#### 75. 数组和对象有哪些原生方法，列举一下？

数组：ES3(12)、ES5(9)、ES6(14)

```
数组和字符串的转换方法：toString()、toLocalString()、join() 其中 join() 方法可以指定转换为字符串时的分隔符。
 
数组尾部操作的方法 pop() 和 push()，push 方法可以传入多个参数。

数组首部操作的方法 shift() 和 unshift() 重排序的方法 reverse() 和 sort()，sort() 方法可以传入一个函数来进行比较，传入前后两个值，如果返回值为正数，则交换两个参数的位置。

数组连接的方法 concat() ，返回的是拼接好的数组，不影响原数组。

数组截取办法 slice()，用于截取数组中的一部分返回，不影响原数组。

数组插入方法 splice()，影响原数组查找特定项的索引的方法，indexOf() 和 lastIndexOf() 迭代方法 every()、some()、filter()、map() 和 forEach() 方法

数组归并方法 reduce() 和 reduceRight() 方法
```

详细资料可以参考：
[《JavaScript 深入理解之 Array 类型详解》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8BArray%E8%AF%A6%E8%A7%A3.html)

#### 76. 数组的 fill 方法？

```
向指定长度的空数组中填充指定的值
fill() 方法用一个固定值填充一个数组中从起始索引到终止索引内的全部元素。不包括终止索引。
常结合new使用比如: new Array(5).fill('a')
fill 方法接受三个参数 value，start 以及 end，start 和 end 参数是可选的，其默认值分别为 0 和 this 对象的 length 属性值。
```

详细资料可以参考：
[《Array.prototype.fill()》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/fill)

#### 77. [,,,] 的长度？

```
尾后逗号 

JavaScript 一开始就支持数组字面值中的尾后逗号，随后向对象字面值（ECMAScript 5）中添加了尾后逗号。最近（ECMAS
cript 2017），又将其添加到函数参数中。但是 JSON 不支持尾后逗号。

如果使用了多于一个尾后逗号，会产生间隙。 带有间隙的数组叫做稀疏数组（密致数组没有间隙）。稀疏数组的长度为逗号的数量。
```

详细资料可以参考：
[《尾后逗号》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Trailing_commas)

#### 78. JavaScript 中的作用域与变量声明提升？

```
变量提升的表现是我们可以在变量声明前访问到而不会报错。
更进一步的，所有声明都存在变量提升包括函数声明和变量声明、同一个变量只能声明一次其他的会被覆盖掉、函数声明的优先级最高。

造成变量声明提升的本质原因是 js 引擎在代码执行前有一个解析的过程，创建了执行上下文，初始化了一些代码执行时需要用到的对象。主要是变量对象，它是执行上下文的一个属性，它包含了函数的形参、所有的函数和变量声明。初始化变量对象的过程，就是各种变量和函数声明进行提升的环节。
```

JS代码执行主要包括两个过程：

JS执行上下文的创建阶段，即JS的预解析过程，JS执行上下文的创建，本质就是3个步骤：初始化变量对象；确定作用域链；确定this指向

初始化变量对象：分析参数、分析变量、分析函数声明、

确定作用域链：父级执行上下文的作用域链[[scopeChain]]并压入当前执行上下文的变量对象于作用域链的顶部(确定一个执行上下文的作用域链，查看该执行上下文对应函数的作用域[[Scope]]情况可知道该函数父作用域的情况，则知道其父执行上下文的作用域链情况，在其父执行上下文的作用域链上压入当前执行上下文的变量对象即可) 

JS执行上下文的执行阶段，即将JS执行上下文压入执行栈中加以执行，包括变量赋值，函数引用等等...这个过程才是JS代码真正执行的过程。若果多个执行上下文之间存在闭包的关系，则先从栈顶开始执行最顶层的执行上下文，并按该执行上下文中代码的顺序依次一步一步执行，该执行上下文执行完毕，弹栈。执行权交由下一个执行上下文，然后代码再按次序一步一步的执行，以此类推...

定义函数==》词法函数作用域创建  

调用函数==》JS代码预解析创建函数执行上下文 ==》 函数执行上下文压入执行栈正式的执行函数中代码

打开浏览器窗口 ==》  词法全局作用域创建

开始要执行JS代码  ==》Js预解析创建全局执行上下文 ==》  全局执行上下文压入执行栈正式执行全局代码



详细资料可以参考：
[《JavaScript 深入理解之变量对象》](http://cavszhouyou.top/JavaScript%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3%E4%B9%8B%E5%8F%98%E9%87%8F%E5%AF%B9%E8%B1%A1.html)

#### 79. 如何编写高性能的 Javascript ？

- 1.使用位运算代替一些简单的四则运算。
- 2.避免使用过深的嵌套循环。
- 3.不要使用未定义的变量。
- 4.当需要多次访问数组长度时，可以用变量保存起来，避免每次都会去进行属性查找。

详细资料可以参考：
[《如何编写高性能的 Javascript？》](https://zhuanlan.zhihu.com/p/34780474)

#### 80. 简单介绍一下 V8 引擎的垃圾回收机制

JS引擎，解析并执行JS，谷歌的JS引擎是V8引擎

```
v8 的垃圾回收机制基于分代回收机制，这个机制又基于世代假说，这个假说有两个特点，一是新生的对象容易早死，另一个是不死的对象会活得更久。基于这个假说，v8 引擎将内存分为了新生代和老生代。

新创建的对象或者只经历过一次的垃圾回收的对象被称为新生代。经历过多次垃圾回收的对象被称为老生代。

新生代被分为 From 和 To 两个空间，To 一般是闲置的。当 From 空间满了的时候会执行 Scavenge 算法进行垃圾回收。当我们执行垃圾回收算法的时候应用逻辑将会停止，等垃圾回收结束后再继续执行。这个算法分为三步：
+
（1）首先检查 From 空间的存活对象，如果对象存活则判断对象是否满足晋升到老生代的条件，如果满足条件则晋升到老生代。如果不满足条件则移动 To 空间。

（2）如果对象不存活，则释放对象的空间。

（3）最后将 From 空间和 To 空间角色进行交换。

//=================================================

新生代对象晋升到老生代有两个条件：

（1）第一个是判断是对象否已经经过一次 Scavenge 回收。若经历过，则将对象从 From 空间复制到老生代中；若没有经历，则复制到 To 空间。

（2）第二个是 To 空间的内存使用占比是否超过限制。当对象从 From 空间复制到 To 空间时，若 To 空间使用超过 25%，则对象直接晋升到老生代中。设置 25% 的原因主要是因为算法结束后，两个空间结束后会交换位置，如果 To 空间的内存太小，会影响后续的内存分配。

老生代采用了标记清除法和标记压缩法。标记清除法首先会对内存中存活的对象进行标记，标记结束后清除掉那些没有标记的对象。由于标记清除后会造成很多的内存碎片，不便于后面的内存分配。所以了解决内存碎片的问题引入了标记压缩法。

由于在进行垃圾回收的时候会暂停应用的逻辑，对于新生代方法由于内存小，每次停顿的时间不会太长，但对于老生代来说每次垃圾回收的时间长，停顿会造成很大的影响。 为了解决这个问题 V8 引入了增量标记的方法，将一次停顿进行的过程分为了多步，每次执行完一小步就让运行逻辑执行一会，就这样交替运行。
```

详细资料可以参考：
[《深入理解 V8 的垃圾回收原理》](https://www.jianshu.com/p/b8ed21e8a4fb)
[《JavaScript 中的垃圾回收》](https://zhuanlan.zhihu.com/p/23992332)

#### 81. 哪些操作会造成内存泄漏？

相关知识点：

- 1.意外的全局变量
- 2.被遗忘的计时器或回调函数
- 3.脱离 DOM 的引用
- 4.闭包

回答：

```
第一种情况是我们由于使用未声明的变量，而意外的创建了一个全局变量，而使这个变量一直留在内存中无法被回收。

第二种情况是我们设置了 setInterval 定时器，而忘记取消它，如果循环函数有对外部变量的引用的话，那么这个变量会被一直留在内存中，而无法被回收。

第三种情况是我们获取一个 DOM 元素的引用，而后面这个元素被删除，由于我们一直保留了对这个元素的引用，所以它也无法被回收。

第四种情况是不合理的使用闭包，从而导致某些变量一直被留在内存当中。
```

详细资料可以参考：
[《JavaScript 内存泄漏教程》](http://www.ruanyifeng.com/blog/2017/04/memory-leak.html)
[《4 类 JavaScript 内存泄漏及如何避免》](https://jinlong.github.io/2016/05/01/4-Types-of-Memory-Leaks-in-JavaScript-and-How-to-Get-Rid-Of-Them/)
[《杜绝 js 中四种内存泄漏类型的发生》](https://juejin.im/entry/5a64366c6fb9a01c9332c706)
[《javascript 典型内存泄漏及 chrome 的排查方法》](https://segmentfault.com/a/1190000008901861)

#### 82. 需求：实现一个在浏览器前进、后退时可以无刷新更新页面的网站。给出你的技术实现方案？

浏览器前进后退按钮就是来查看历史记录的和history.go、history.forword、history.back功能一样

```
页面操作不会整页刷新的网站：
浏览器无刷新更新页面内容（无刷新更新局部页面内容）：ajax  +  
浏览器无刷新前进后退(无刷新更新整个页面内容)： HTML5提供的历史记录api，
主要有location.hash+hashchange；history.pushState()方法 + window.popState事件

1、location.hash  + window.hashchange事件
-给页面设置location.hash 会在浏览器历史记录中添加一条hash值与页面状态对应关系的历史记录(浏览器地址栏也会在url地址上更新设置的hash值)
-一旦hash值发生变化(前进、后退)就会触发window.hashChange事件，在事件处理函数中location.hash获取hash值，并根据历史记录中hash值与页面状态的对应关系，进行相应的页面状态展示即可.还是这个网站，只不过是通过前进后退按钮来实现不同页面状态的切换，比如说#a是a图片，#b是b图片，从#a前进按钮到#b，不会刷新这个网站，只是a图片展示变成了b图片展示，这样的网站页面状态变化。

2、history.pushState()方法 + window.popState事件
-pushState和replaceState方法操作浏览器历史，并且改变当前页面的URL，调用pushState将该页面相关状态信息添加到历史记录中，该方法第一个参数是一个包含用于恢复当前文档状态所需所有信息的对象，第二个参数是可选标题，第三个参数是可选url将其与页面进行关联。history.replaceState()方法其接收参数同pushState()，但是不是将新的页面状态添加到历史记录中，而是新的状态信息来代替老的状态信息

var state = { title: title, url: options.url, otherkey:othervalue};
window.history.pushState(state, document.title, url);

-当用户点击前进后退按钮来查看保存的历史记录时，会触发window.popState事件，该事件对象的state属性中就存储了pushState()方法存入历史记录的状态对象的副本。也就是说我们可以在事件处理函数中，拿到与页面相关联的记录状态信息的对象，然后进行相应页面状态的展示。

通过使用 pushState + ajax 实现浏览器无刷新前进后退，当一次 ajax 调用成功后我们将一条 state 记录加入到 history
对象中。一条 state 记录包含了 url、title 和 content 属性，在 popstate 事件中可以获取到这个 state 对象，我们可
以使用 content 来传递数据。最后我们通过对 window.onpopstate 事件监听来响应浏览器的前进后退操作。

//使用 pushState 来实现有两个问题，一个是打开首页时没有记录，我们可以使用 replaceState 来将首页的记录替换，另一个问
//题是当一个页面刷新的时候，仍然会向服务器端请求数据，因此如果请求的 url 需要后端的配合将其重定向到一个页面。
```

详细资料可以参考：
[《pushState + ajax 实现浏览器无刷新前进后退》](http://blog.chenxu.me/post/detail?id=ed4f0732-897f-48e4-9d4f-821e82f17fad)
[《Manipulating the browser history》](https://developer.mozilla.org/zh-CN/docs/Web/API/History_API)

#### 83. 如何判断当前脚本运行在浏览器还是 node 环境中？（阿里）

```
typeof window === 'undefined' ? 'node' : 'browser';

通过判断当前环境的 window 对象类型是否为 undefined，如果是undefined，则说明当前脚本运行在node环境，否则说明运行在window环境。

浏览器环境：顶层对象是window
Node环境：顶层对象是global
ES2020引入的globalThis可以获取不同环境的顶层对象
全局变量和顶层对象的属性直接挂钩，这是JS的一大败笔，会造成很多麻烦，为此let、const声明的全局变量不在与顶层对象属性挂钩，var声明的依然挂钩。比如在浏览器环境中：
var a = 111; window.a==》111
let b = 222; window.b==》undefined
```

#### 84. 把 script 标签放在页面的最底部的 body 封闭之前和封闭之后有什么区别？浏览器会如何解析它们(X)

详细资料可以参考：
[《为什么把 script 标签放在 body 结束标签之后 html 结束标签之前？》](https://www.zhihu.com/question/20027966)
[《从 Chrome 源码看浏览器如何加载资源》](https://zhuanlan.zhihu.com/p/30558018)

#### 85. 移动端的点击事件的延迟，时间是多久，为什么会有？ 怎么解决这个延时？

```
移动端点击有 300ms 的延迟是因为移动端会有双击缩放的这个操作，因此浏览器在 click 之后要等待 300ms，看用户有没有下一次点击，来判断这次操作是不是双击。
```

有三种办法来解决这个问题：

- 1.通过 meta 标签禁用网页的缩放。
- 2.通过 meta 标签将网页的 viewport 设置为 ideal viewport。
- 3.调用一些 js 库，比如 FastClick

```
click 延时问题还可能引起点击穿透的问题，就是如果我们在一个元素上注册了 touchStart 的监听事件，这个事件会将这个元素隐藏掉，当这个元素隐藏后，就触发了这个元素下的一个元素的点击事件，这就是点击穿透。
```

详细资料可以参考：
[《移动端 300ms 点击延迟和点击穿透》](https://juejin.im/post/5b3cc9836fb9a04f9a5cb0e0)

#### 86. 什么是“前端路由”？什么时候适合使用“前端路由”？“前端路由”有哪些优点和缺点？

```
（1）什么是前端路由？

	见下：

（2）什么时候使用前端路由？

在单页面应用，大部分页面结构不变，只改变部分内容的使用

（3）前端路由有什么优点和缺点？

优点：用户体验好，不需要每次都从服务器全部获取，快速展现给用户

缺点：单页面无法在前进，后退的时候记住滚动的位置

前端路由一共有两种实现方式，一种是通过 hash 的方式，一种是通过使用 pushState 的方式。
```

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/Snipaste_2021-06-18_14-48-14.png" style="zoom:50%;" />

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/Snipaste_2021-06-18_14-48-26.png" style="zoom:50%;" />

详细资料可以参考：
[《什么是“前端路由”》](https://segmentfault.com/q/1010000005336260)
[《浅谈前端路由》 ](https://github.com/kaola-fed/blog/issues/137)
[《前端路由是什么东西？》](https://www.zhihu.com/question/53064386)

#### 87. 如何测试前端代码么？ 知道 BDD, TDD, Unit Test 么？ 知道怎么测试你的前端工程么(mocha, sinon, jasmin, qUnit..)？

 单元测试：为检测特定的目标是否符合标准而采用专用的工具或者方法进行验证，并最终得出特定的结果。

在单元测试中，常用的方法论有两个：TDD（测试驱动开发）&BDD（行为驱动开发）

常见单元测试框架：mocha, sinon, jasmin, qUnit....

详细资料可以参考：
[《浅谈前端单元测试》](https://juejin.im/post/5b2da89cf265da597f1c7cab)

#### 88. 检测浏览器版本有哪些方式？

```
检测浏览器版本一共有两种方式：

一种是检测 window.navigator.userAgent 的值，但这种方式很不可靠，因为 userAgent 可以被改写，并且早期的浏览器如 ie，会通过伪装自己的 userAgent 的值为 Mozilla 来躲过服务器的检测。

第二种方式是功能检测，根据每个浏览器独有的特性来进行判断，如 ie 下独有的 ActiveXObject。

if (window.ActiveXObject)
return "IE";
else if (document.getBoxObjectFor)
return "Firefox";
else if (window.MessageEvent && !document.getBoxObjectFor)
return "Chrome";
else if (window.opera)
return "Opera";
else if (window.openDatabase)
return "Safari";
```

详细资料可以参考：
[《JavaScript 判断浏览器类型》](https://www.jianshu.com/p/d99f4ca385ac)

#### 89. 什么是 Polyfill ？

```
Polyfill 指的是用于实现浏览器并不支持的原生 API 的一类文件或库。

一个 shim 是一个库，有自己的 API，而不是单纯实现原生不支持的 API。
```

babel.config.js是Babel配置文件，

使用babel必须下载的三个官方的包

@babel/cli，Babel命令行转码工具，依赖@babel/core 

@babel/core ,  核心依赖

@babel/preset-env ，包提供了ES6转换ES5的语法转换规则

Babel的主要工作有两部分：语法转换、补齐API，但是Babel默认只转换新的JavaScript语法（syntax），而不转换新的 API。

让ES6新的API在低版本浏览器正常运行，我们就不能只做语法转换。前端web工程里，最常规的做法是使用polyfill，为当前环境提供一个垫片。polyfill广义上讲是为环境提供不支持的特性的一类文件或库

详细资料可以参考：
[《Web 开发中的“黑话”》](https://segmentfault.com/a/1190000002593432)
[《Polyfill 为何物》](https://juejin.im/post/5a579bc7f265da3e38496ba1)

#### 90. 使用 JS 实现获取文件扩展名？

```js
// String.lastIndexOf() 方法返回指定值（本例中的'.'）在调用该方法的字符串中最后出现的位置
// 字符串中没有点返回-1，以及索引为0的位置，这个文件都不符合规则，为了保证该方法的可用，需要无符号右移操作符
// 获取文件扩展名，应该是在查到的点的后面一位，所以之前减1后面要再加上2
// slice从点后面一位开始一直截取到最后，从而获取文件扩展名
// 以test.js为例，查到.在4的位置，减1位3，无符号右移不变，加二获取文件扩展名开始位置的索引，slice加以截取
function getFileExtension(filename) {
  return filename.slice(((filename.lastIndexOf(".") - 1) >>> 0) + 2);
}
```

详细资料可以参考：
[《如何更有效的获取文件扩展名》](https://segmentfault.com/a/1190000004993946)

#### 91. 介绍一下 js 的节流与防抖？

相关知识点：

```js
// 函数防抖： 不断的重置延迟时间，等延迟时间到了在执行一次回调函数

// 函数节流： 在一段时间内只执行一次回调函数

// 函数防抖的实现
function debounce(func,delay){
    let timer;
    return function(){
        let context = this,
            arg = arguments;
        clearTimeout(timer);
        timer = setTimeout(()=>{
            func.apply(context,arg);
        },delay) 
    }
}

// 函数节流的实现;
function throttle(func,delay){
    let timer;
    return function(){
        if(timer){
            return;
        }
        let context = this,
            arg = arguments;
        timer = setTimeout(()=>{
            func.apply(context,arg);
            timer = null;
        },delay)       
    }
    
}
```

回答：

```
// 函数防抖： 不断的重置延迟时间，等延迟时间到了在执行一次回调函数。这可以使用在一些点击请求的事件上，避免因为用户的多次点击向后端发送多次请求。

// 函数节流： 在一段时间内只执行一次回调函数。节流可以使用在 scroll 函数的事件监听上，通过事件节流来降低事件调用的频率。
```

详细资料可以参考：
[《轻松理解 JS 函数节流和函数防抖》](https://juejin.im/post/5a35ed25f265da431d3cc1b1)
[《JavaScript 事件节流和事件防抖》](https://juejin.im/post/5aa60b0e518825556b6c6d1a)
[《JS 的防抖与节流》](https://juejin.im/entry/5b1d2d54f265da6e2545bfa4)

#### 92. Object.is() 与原来的比较操作符 双等号、三等号 的区别？

相关知识点：

```
两等号判等，会在比较时进行类型转换。
三等号判等（判断严格），比较时不进行隐式类型转换，（类型不同则会返回false）。

Object.is 在三等号判等的基础上特别处理了 NaN 、-0 和 +0 ，保证 -0 和 +0 不再相同，但 Object.is(NaN, NaN) 会返回 true.

Object.is 应被认为有其特殊的用途，而不能用它认为它比其它的相等对比更宽松或严格。
```

回答：

```
使用双等号进行相等判断时，如果两边的类型不一致，则会进行强制类型转化后再进行比较。
null == undefined ~~~~》true
+0 == -0 ~~~~>true
NaN == NaN ~~~~> false

使用三等号进行相等判断时，如果两边的类型不一致时，不会做强制类型准换，直接返回 false。
null === undefined ~~~~》false
+0 === -0 ~~~~>true
NaN == NaN ~~~~> false

使用 Object.is 来进行相等判断时，一般情况下和三等号的判断相同，它处理了一些特殊的情况，比如 -0 和 +0 不再相等，两个 NaN 认定为是相等的。
Object.is(null, undefined)   ~~~~> false
Object.is(+0, -0)   ~~~~> false
Object.is(NaN, NaN)   ~~~~> true
```

#### 93. escape,encodeURI,encodeURIComponent 有什么区别？

回答：

```
encodeURI 是对整个 URI 进行转义，将 URI 中的非法字符转换为合法字符，所以对于一些在 URI 中有特殊意义的字符不会进行转义。

encodeURIComponent 是对 URI 的组成部分进行转义，所以一些特殊字符也会得到转义。

escape(已弃用) 和 encodeURI 的作用相同，不过它们对于 unicode 编码为 0xff 之外字符的时候会有区别，escape 是直接在字符的 unicode 编码前加上 %u，而 encodeURI 首先会将字符转换为 UTF-8 的格式，再在每个字节前加上 %。
```

详细资料可以参考：
[《escape,encodeURI,encodeURIComponent 有什么区别?》](https://www.zhihu.com/question/21861899)

#### 94. Unicode 和 UTF-8 之间的关系？

```
Unicode 是一种字符集合，现在可容纳 100 多万个字符。每个字符对应一个不同的 Unicode 编码，它只规定了符号的二进制代码，却没有规定这个二进制代码在计算机中如何编码传输。

UTF-8 是一种对 Unicode 的编码方式，它是一种变长的编码方式，可以用 1~4 个字节来表示一个字符。
```

详细资料可以参考：
[《字符编码详解》](https://blog.51cto.com/polaris/377468)
[《字符编码笔记：ASCII，Unicode 和 UTF-8》](http://www.ruanyifeng.com/blog/2007/10/ascii_unicode_and_utf-8.html)

#### 95. js 的事件循环是什么？

相关知识点：

```
事件队列是一个存储着待执行任务的队列，其中的任务严格按照时间先后顺序执行，排在队头的任务将会率先执行，而排在队尾的任务会最后执行。事件队列每次仅执行一个任务，在该任务执行完毕之后，再执行下一个任务。执行栈则是一个类似于函数调用栈的运行容器，当执行栈为空时，JS 引擎便检查事件队列，如果不为空的话，事件队列便将第一个任务压入执行栈中运行。
```

回答：

```
因为 js 是单线程运行的，在代码执行的时候，通过将不同函数的执行上下文压入执行栈中来保证代码的有序执行。在执行同步代码的时候，如果遇到了异步事件，js 引擎并不会一直等待其返回结果，而是会将这个事件挂起，继续执行执行栈中的其他任务。当异步事件执行完毕后，再将异步事件对应的回调加入到与当前执行栈中不同的另一个任务队列中等待执行。任务队列可以分为宏任务对列和微任务对列，当当前执行栈中的事件执行完毕后，js 引擎首先会判断微任务对列中是否有任务可以执行，如果有就将微任务队首的事件压入栈中执行。当微任务对列中的任务都执行完成后再去判断宏任务对列中的任务。

微任务包括了 promise 的回调、node 中的 process.nextTick 、对 Dom 变化监听的 MutationObserver。

宏任务包括了 script 脚本的执行、setTimeout ，setInterval ，setImmediate 一类的定时事件，还有如 I/O 操作、UI 渲
染等。
```

```
常见宏任务：setTimeout  setInterval   DOM事件  Ajax请求
常见微任务：promise   async/await
```

详细资料可以参考：
[《浏览器事件循环机制（event loop）》](https://juejin.im/post/5afbc62151882542af04112d)
[《详解 JavaScript 中的 Event Loop（事件循环）机制》](https://zhuanlan.zhihu.com/p/33058983)
[《什么是 Event Loop？》](http://www.ruanyifeng.com/blog/2013/10/event_loop.html)
[《这一次，彻底弄懂 JavaScript 执行机制》](https://juejin.im/post/59e85eebf265da430d571f89)

#### 96. js 中的深浅拷贝实现？

相关资料：

```js
// 浅拷贝的实现;

function shallowCopy(object) {
  // 只拷贝对象
  if (!object || typeof object !== "object") return;

  // 根据 object 的类型判断是新建一个数组还是对象
  let newObject = Array.isArray(object) ? [] : {};

  // 遍历 object，并且判断是 object 的属性才拷贝
  for (let key in object) {
    if (object.hasOwnProperty(key)) {
      newObject[key] = object[key];
    }
  }

  return newObject;
}

// 深拷贝的实现;

//1序列化反序列化快速实现
//(将堆内存引用类型的数据转为栈内存原始值类型，可以直接进行所有值的复制，而不会出现浅复制时只复制了引用数据地址的情况)
//需要注意一些序列化、反序列化存在问题的数据不能用这种方式实现深拷贝
//比如：函数、Error、RegExp、undefined   Infinity、-Infinity、null、Date

let newObj = JSON.Parse(JSON.Stringfy(obj))

function deepClone(obj){
    if(obj === null) return obj;
    if(typeof obj !== 'object') return obj;
    if(typeof obj === 'function') return new Function(obj);
    if(obj instanceof RegExp) return new RegExp(obj);
    if(obj instanceof Date) return new Date(obj);
    
    let newObj = new obj.constructor;
    
    for(let item in obj){
        if(obj.hasOwnProperty(item)){
            newObj[item] = deepClone(obj[item]);
        }
    }
    
    return newObj;
}
```

回答：

```
对象的浅拷贝，如果其值为一个引用类型的数据，只拷贝这个数据的引用地址，而深拷贝的话就拷贝这个数据的值
浅拷贝的常见实现：
...展开运算符、Object.assign()、
Array.prototype.slice()、Array.prototype.concat()、
lodash库中的_.clone()。

深拷贝的常见实现：
递归方式手动实现，lodash库提供的函数，JSON.parse(JSON.Stringfy(****))
```

详细资料可以参考：
[《JavaScript 专题之深浅拷贝》](https://github.com/mqyqingfeng/Blog/issues/32)
[《前端面试之道》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bed40d951882545f73004f6)

#### 97. ***手写 call、apply 及 bind 函数

Object.create(null)  创建一个没有原型的对象

call、apply第一个参数是null 则指向所处环境的顶层对象window、global

globalThis可以获取所处环境的顶层对象

arguments和this都指向调用call、apply、bind的那个函数

相关资料：

```js
// call函数实现
Function.prototype.myCall = function(context) {
  // 判断调用对象
  if (typeof this !== "function") {
    console.error("type error");
  }  

  // 获取参数
  let args = [...arguments].slice(1),
    result = null;

  // 判断 context 是否传入，如果未传入则设置为 window
  context = context || window;

  // 将调用函数设为对象的方法
  context.fn = this;

  // 调用函数
  result = context.fn(...args);

  // 将属性删除
  delete context.fn;

  return result;
};

// apply 函数实现

Function.prototype.myApply = function(context) {
  // 判断调用对象是否为函数
  if (typeof this !== "function") {
    throw new TypeError("Error");
  }

  let result = null;

  // 判断 context 是否存在，如果未传入则为 window
  context = context || window;

  // 将函数设为对象的方法
  context.fn = this;

  // 调用方法
  if (arguments[1]) {
    result = context.fn(...arguments[1]);
  } else {
    result = context.fn();
  }

  // 将属性删除
  delete context.fn;

  return result;
};

// bind 函数实现
Function.prototype.myBind = function(context) {
  // 判断调用对象是否为函数
  if (typeof this !== "function") {
    throw new TypeError("Error");
  }

  // 获取参数
  var args = [...arguments].slice(1),
    fn = this;

  return function Fn() {
    // 根据调用方式，传入不同绑定值
    return fn.apply(
      this instanceof Fn ? this : context,
      args.concat(...arguments)
    );
  };
};
```

回答：

call 函数的实现步骤：

- 1.判断调用对象是否为函数，即使我们是定义在函数的原型上的，但是可能出现使用 call 等方式调用的情况。
- 2.判断传入上下文对象是否存在，如果不存在，则设置为 window 。
- 3.处理传入的参数，截取第一个参数后的所有参数。
- 4.将函数作为上下文对象的一个属性。
- 5.使用上下文对象来调用这个方法，并保存返回结果。
- 6.删除刚才新增的属性。
- 7.返回结果。

apply 函数的实现步骤：

- 1.判断调用对象是否为函数，即使我们是定义在函数的原型上的，但是可能出现使用 call 等方式调用的情况。
- 2.判断传入上下文对象是否存在，如果不存在，则设置为 window 。
- 3.将函数作为上下文对象的一个属性。
- 4.判断参数值是否传入
- 4.使用上下文对象来调用这个方法，并保存返回结果。
- 5.删除刚才新增的属性
- 6.返回结果

bind 函数的实现步骤：

- 1.判断调用对象是否为函数，即使我们是定义在函数的原型上的，但是可能出现使用 call 等方式调用的情况。
- 2.保存当前函数的引用，获取其余传入参数值。
- 3.创建一个函数返回
- 4.函数内部使用 apply 来绑定函数调用，需要判断函数作为构造函数的情况，这个时候需要传入当前函数的 this 给 apply 调用，其余情况都传入指定的上下文对象。

详细资料可以参考：
[《手写 call、apply 及 bind 函数》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bdd0d8e6fb9a04a044073fe)
[《JavaScript 深入之 call 和 apply 的模拟实现》](https://github.com/mqyqingfeng/Blog/issues/11)

#### 98. ***函数柯里化的实现

```js
// 函数柯里化指的是一种将使用多个参数的一个函数转换成一系列使用一个参数的函数的技术。
// JavaScript中的柯里化其实是利用闭包的特性，将所有参数都搜集到之后再一并执行。
// 将多参数函数转换成单参数函数，就是fn本来是有很多参数的，我将其柯里化，转变成每次只传入一个或几个参数的函数，
// 等其所需用到的参数都收集完了，在一次性加以执行
//function fn(a, b, c, d, e...) {}
// 通过柯里化 转换为
//curryFn(a)(b)(c)(d)(e)(...)

// es6 实现
function curry(fn, ...args) {
    return function(...innerArgs) {
        let allArgs = [...args, ...innerArgs];
        
        if (fn.length <= allArgs.length) {
            // 说明已经接受完所有参数，这个时候可以执行了
            return fn.apply(this, allArgs);
        } else {
            // 继续返回函数，收集参数
            return curry(fn, ...allArgs);
        }
    }
}
```

详细资料可以参考：
[《JavaScript 专题之函数柯里化》](https://github.com/mqyqingfeng/Blog/issues/42)

#### 99. 为什么 0.1 + 0.2 != 0.3？如何解决这个问题？

JS中的数值以64位双精度浮点数进行存储，其只有53位的有效数字（也就是说用来有效存储数字的只有53位其他11位不用管，用不了）

双精度浮点数一共占据64位：

- 符号位（sign）占用1位
- 指数位（exponent）占用11位
- 小数位（fraction）占用52位

```
当计算机计算 0.1+0.2 的时候，实际上计算的是这两个数字在计算机里所存储的二进制，0.1 和 0.2 在转换为二进制表示的时候会出现位数无限循环的情况。js 中是以 64 位双精度格式来存储数字的，只有 53 位的有效数字，超过这个长度的位数会被截取掉这样就造成了精度丢失的问题。

在对两个以 64 位双精度格式的数据进行计算的时候，首先会进行对阶的处理，对阶指的是将阶码对齐，也就是将小数点的位置对齐后，再进行计算，一般是小阶向大阶对齐，因此小阶的数在对齐的过程中，有效数字会向右移动，移动后超过有效位数的位会被截取掉，这是第二个可能会出现精度丢失的地方。当两个数据阶码对齐后，进行相加运算后，得到的结果可能会超过 53 位有效数字，因此超过的位数也会被截取掉，这是可能发生精度丢失的第三个地方。

对于这样的情况，我们可以将其转换为整数后再进行运算，运算后再转换为对应的小数，以这种方式来解决这个问题。

我们还可以将两个数相加的结果和右边相减，如果相减的结果小于一个极小数，那么我们就可以认定结果是相等的，这个极小数可以
使用 es6 的 Number.EPSILON
```

详细资料可以参考：
[《十进制的 0.1 为什么不能用二进制很好的表示？》](https://blog.csdn.net/Lixuanshengchao/article/details/82049191)
[《十进制浮点数转成二进制》](https://blog.csdn.net/zhengyanan815/article/details/78550073)
[《浮点数的二进制表示》](http://www.ruanyifeng.com/blog/2010/06/ieee_floating-point_representation.html)
[《js 浮点数存储精度丢失原理》](https://juejin.im/post/5b372f106fb9a00e6714aa21)
[《浮点数精度之谜》](https://juejin.im/post/594a31d0a0bb9f006b0b2624)
[《JavaScript 浮点数陷阱及解法》](https://github.com/camsong/blog/issues/9)
[《0.1+0.2 !== 0.3？》](https://juejin.im/post/5bd2f10a51882555e072d0c4)
[《JavaScript 中奇特的~运算符》](https://juejin.im/entry/59cdd7fb6fb9a00a600f8eef)

#### 100. 原码、反码和补码的介绍

```
原码是计算机中对数字的二进制的定点表示方法，最高位表示符号位，其余位表示数值位。优点是易于分辨，缺点是不能够直接参与运算。

正数的反码和其原码一样；负数的反码，符号位为1，数值部分按原码取反。
如 [+7]原 = 00000111，[+7]反 = 00000111； [-7]原 = 10000111，[-7]反 = 11111000。

正数的补码和其原码一样；负数的补码为其反码加1。

例如 [+7]原 = 00000111，[+7]反 = 00000111，[+7]补 = 00000111；
[-7]原 = 10000111，[-7]反 = 11111000，[-7]补 = 11111001

之所以在计算机中使用补码来表示负数的原因是，这样可以将加法运算扩展到所有的数值计算上，因此在数字电路中我们只需要考虑加法器的设计就行了，而不用再为减法设置新的数字电路。
```

详细资料可以参考：
[《关于 2 的补码》](http://www.ruanyifeng.com/blog/2009/08/twos_complement.html)

#### 101. toPrecision 和 toFixed 和 Math.round 的区别？

```
toPrecision 用于处理精度，精度是从左至右第一个不为 0 的数开始数起。
toFixed 是对小数点后指定位数取整，从小数点开始数起。
Math.round 是将一个数字四舍五入到一个整数。 
n = 123456.789
n.toPrecision(7) ~~ 123456.8 对第7位进行取整
n.toFixed(2) ~~123456.79 对小数点后第几位进行取整
```

#### 102. 什么是 XSS 攻击？如何防范 XSS 攻击？

```
XSS 攻击指的是跨站脚本攻击，攻击者通过向目标网站注入恶意脚本从而进行攻击。

XSS 一般分为存储型、反射型和 DOM 型。

存储型指的是恶意代码提交到了网站的数据库中，当用户请求数据的时候，服务器将其拼接为 HTML 后返回给了用户，从而导致了恶意代码的执行。

反射型指的是攻击者构建了特殊的 URL，当服务器接收到请求后，从 URL 中获取数据，拼接到 HTML 后返回，从而导致了恶意代码的执行。

DOM 型指的是攻击者构建了特殊的 URL，用户打开网站后，js 脚本从 URL 中获取数据，从而导致了恶意代码的执行。

对XSS攻击的防范：
1.处理原则不相信用户输入的任何数据，具体是对用户的输入加以处理，主要是对一些特殊字符进行转译，包括....
2.使用白名单，告诉浏览器那些资源可以被加载和执行，不在其上的资源不准加载和执行。

```

详细资料可以参考：
[《前端安全系列（一）：如何防止 XSS 攻击？》](https://juejin.im/post/5bad9140e51d450e935c6d64)

#### 103. 什么是 CSP？

```
CSP 指的是内容安全策略，它的本质是建立一个白名单，告诉浏览器哪些外部资源可以加载和执行。我们只需要配置规则，如何拦截由浏览器自己来实现。

通常有两种方式来开启 CSP，一种是设置 HTTP 首部中的 Content-Security-Policy，一种是设置 meta 标签的方式 <meta
http-equiv="Content-Security-Policy">
```

详细资料可以参考：
[《内容安全策略（CSP）》](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/CSP)
[《前端面试之道》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bdc721851882516c33430a2)

#### 104. 什么是 CSRF 攻击？如何防范 CSRF 攻击？

```
CSRF 攻击指的是跨站请求伪造攻击：用户访问目标站点A时，被诱导至第三方恶意站点B，之后冒用用户登录站点A的身份凭证(cookie)，向目标站点A，发动相应的攻击。

//攻击一般发起在第三方网站，而不是被攻击的网站。
//整个过程攻击者并不能获取到受害者的登录凭证，仅仅是“冒用”
//攻击利用受害者在被攻击网站的登录凭证，冒充受害者提交操作；而不是直接窃取数据。
//CSRF 攻击的本质是利用了 cookie 会在同源请求中携带发送给服务器的特点，以此来实现用户的冒充。

一般的 CSRF 攻击类型有三种：

第一种是 GET 类型的 CSRF 攻击，比如在网站中的一个 img 标签里构建一个请求，当用户打开这个恶意网站的时候就会自动向目标网站发起提交。也就是说，这个提交会使得浏览器自动携带着cookie向目标站点发送请求，我恶意站点没有获取你的cookie，但是我让你浏览器向目标站点发请求，你浏览器自己把cookie给带上了，这样目标站点觉得这是合法请求了。这就是恶意站点冒用cookie，但是他不知道cookie。如果我们用token来标识用户身份，token只要不是放在cookie中的，我恶意站点让你浏览器发送请求，这个token是不会被自动带上，发去目标站点的。

第二种是 POST 类型的 CSRF 攻击，比如说构建一个表单，然后隐藏它，当用户进入页面时，自动提交这个表单。

第三种是链接类型的 CSRF 攻击，比如说在 a 标签的 href 属性里构建一个请求，然后诱导用户去点击。

CSRF 可以用下面几种方法来防护：

1.查看http头中的reffer字段，来看请求是来自哪里的，如果是不同源的可能就是CSRF攻击，缺点是reffer可能会被改写

2.用token标识用户身份的方式来取代用cookie标识用户身份的方式，由于token一般存储在localstorge中，在发送请求的时候不会被自动添加上，所以可以规避被冒用的问题，这也就是说如果你将token存储在cookie中，依然存在会被冒用的问题。这种方法存在一个缺点就是，我们需要给网站中的所有请求都添加上这个 token，操作比较繁琐。（服务器向用户返回一个随机数 Token并存储在服务器端的sessionid中 ，当网站再次发起请求时，在请求参数中加入服务器端返回的 token ，然后服务器从sessionid中拿出token对这个请求发过来的 token 进行验证。）改进可以在Http的头部自定义属性并添加cookie信息比如利用axios在头部引入token
config.header.authorization= localstorage.token；

3.对于一些重要的请求，要求用户输入验证码，引入人为的干预来规避CSRF攻击。

4.使用在设置 cookie 属性的时候设置 Samesite ，限制第三方使用 cookie ，从而可以避免被攻击者冒用cookie。Samesite 一共有两种模式，一种是严格模式，在严格模式下 cookie 在任何情况下都不可能作为第三方 Cookie 使用,也就是说只有当前网页的 URL 与请求目标一致，才会带上 Cookie；在宽松模式下，cookie 可以被GET 请求，且会发生页面跳转的请求所使用。
```

<img src="https://gitee.com/chenyipeng9/blog/raw/master/img/20180629193441658.png" style="zoom: 80%;" />



详细资料可以参考：
[《前端安全系列之二：如何防止 CSRF 攻击？》](https://juejin.im/post/5bc009996fb9a05d0a055192)
[《[ HTTP 趣谈] origin, referer 和 host 区别》](https://www.jianshu.com/p/1f9c71850299)

#### 105. 什么是 Samesite Cookie 属性？

```
Samesite Cookie 表示同站 cookie，避免 cookie 被第三方所利用。

将 Samesite 设为 strict ，这种称为严格模式，表示这个 cookie 在任何情况下都不可能作为第三方 cookie。只有当前网页的 URL 与请求目标一致，才会带上 Cookie。

将 Samesite 设为 Lax ，这种模式称为宽松模式，如果这个请求是个 GET 请求，并且这个请求改变了当前页面或者打开了新的页面，那么这个 cookie 可以作为第三方 cookie，其余情况下都不能作为第三方 cookie。

使用这种方法的缺点是，因为它不支持子域，所以子域没有办法与主域共享登录信息，每次转入子域的网站，都回重新登录。还有一个问题就是它的兼容性不够好。
```

#### 106. 什么是点击劫持？如何防范点击劫持？

```
点击劫持是一种视觉欺骗的攻击手段，攻击者使用一个或多个透明的 iframe 覆盖在一个正常的网页上，在页面中透出一个按钮诱导用户点击，这样一来用户的操作就被劫持到攻击者事先设计好的恶意网站了

我们可以在 http 响应头中设置 X-FRAME-OPTIONS 来防御用 iframe 嵌套的点击劫持攻击。通过不同的值，可以规定页面在特
定的一些情况才能作为 iframe 来使用。
```

详细资料可以参考：
[《web 安全之--点击劫持攻击与防御技术简介》](https://www.jianshu.com/p/251704d8ff18)

#### 107. SQL 注入攻击？

```
SQL 注入攻击指的是攻击者在 HTTP 请求中注入恶意的 SQL 代码，服务器使用参数构建数据库 SQL 命令时，恶意 SQL 被一起构
造，破坏原有 SQL 结构，并在数据库中执行，达到编写程序时意料之外结果的攻击行为。
```

#### 分布式拒绝服务攻击DDoS

详细资料可以参考：
[《Web 安全漏洞之 SQL 注入》](https://juejin.im/post/5bd5b820e51d456f72531fa8)
[《如何防范常见的 Web 攻击》](http://blog.720ui.com/2016/security_web/#SQL%E6%B3%A8%E5%85%A5%E6%94%BB%E5%87%BB)

#### 108. 什么是 MVVM？比之 MVC 有什么区别？什么又是 MVP ？

模式分为三层：架构模式，设计模式，实现模式。

```
MVC、MVP 和 MVVM 是三种常见的软件架构设计模式，主要通过分离关注点的方式来组织代码结构，优化我们的开发效率。

比如说我们实验室在以前项目开发的时候，使用单页应用时，往往一个路由页面对应了一个脚本文件，所有的页面逻辑都在一个脚本文件里。页面的渲染、数据的获取，对用户事件的响应所有的应用逻辑都混合在一起，这样在开发简单项目时，可能看不出什么问题，当时一旦项目变得复杂，那么整个文件就会变得冗长，混乱，这样对我们的项目开发和后期的项目维护是非常不利的。

MVC 通过分离 Model、View 和 Controller 的方式来组织代码结构。其中 View 负责页面的显示逻辑，Model 负责存储页面的业务数据，以及对相应数据的操作。并且 View 和 Model 应用了观察者模式，当 Model 层发生改变的时候它会通知有关 View 层更新页面。Controller 层是 View 层和 Model 层的纽带，它主要负责用户与应用的响应操作，当用户与页面产生交互的时候，Controller 中的事件触发器就开始工作了，通过调用 Model 层，来完成对 Model 的修改，然后 Model 层再去通知 View 层更新。

MVP 模式与 MVC 唯一不同的在于 Presenter 和 Controller。在 MVC 模式中我们使用观察者模式，来实现当 Model 层数据发生变化的时候，通知 View 层的更新。这样 View 层和 Model 层耦合在一起，当项目逻辑变得复杂的时候，可能会造成代码的混乱，并且可能会对代码的复用性造成一些问题。MVP 的模式通过使用 Presenter 来实现对 View 层和 Model 层的解耦。MVC 中的Controller 只知道 Model 的接口，因此它没有办法控制 View 层的更新，MVP 模式中，View 层的接口暴露给了 Presenter 因此我们可以在 Presenter 中将 Model 的变化和 View 的变化绑定在一起，以此来实现 View 和 Model 的同步更新。这样就实现了对 View 和 Model 的解耦，Presenter 还包含了其他的响应逻辑。

MVVM 模式中的 VM，指的是 ViewModel，它和 MVP 的思想其实是相同的，不过它通过双向的数据绑定，将 View 和 Model 的同步更新给自动化了。当 Model 发生变化的时候，ViewModel 就会自动更新；ViewModel 变化了，View 也会更新。这样就将 Presenter 中的工作给自动化了。我了解过一点双向数据绑定的原理，比如 vue 是通过使用数据劫持和发布订阅者模式来实现的这一功能。
```

一种架构模式往往使用了多种设计模式

MVC：

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/bg2015020105.png" style="zoom: 80%;" />

MVP：

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/45674659.png" style="zoom:80%;" />

MVVM：

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/bg2556456015020110.png" style="zoom:80%;" />

详细资料可以参考：
[《浅析前端开发中的 MVC/MVP/MVVM 模式》](https://juejin.im/post/593021272f301e0058273468)
[《MVC，MVP 和 MVVM 的图示》](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)
[《MVVM》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bdc72e6e51d45054f664dbf)
[《一篇文章了解架构模式：MVC/MVP/MVVM》](https://segmentfault.com/a/1190000015310674)

#### 109. vue 双向数据绑定原理？（####）

Vue的响应式就是数据影响视图，视图影响数据，从而实现视图view和数据model的同步更新，通俗一点理解就是数据的双向绑定。具体的，Vue的双向数据绑定主要是通过数据劫持和发布订阅相结合的方式实现的。

```
vue 通过使用双向数据绑定，来实现了 View 和 Model 的同步更新。vue 的双向数据绑定主要是通过使用数据劫持和发布订阅者模式来实现的。

首先我们通过 Object.defineProperty() 方法来对 Model 数据各个属性添加访问器属性，以此来实现数据的劫持，因此当 Model 中的数据发生变化的时候，我们可以通过配置的 setter 和 getter 方法来实现对 View 层数据更新的通知。

数据在 html 模板中一共有两种绑定情况，一种是使用 v-model 来对 value 值进行绑定，一种是作为文本绑定，在对模板引擎进行解析的过程中。

如果遇到元素节点，并且属性值包含 v-model 的话，我们就从 Model 中去获取 v-model 所对应的属性的值，并赋值给元素的 value 值。然后给这个元素设置一个监听事件，当 View 中元素的数据发生变化的时候触发该事件，通知 Model 中的对应的属性的值进行更新。

如果遇到了绑定的文本节点，我们使用 Model 中对应的属性的值来替换这个文本。对于文本节点的更新，我们使用了发布订阅者模式，属性作为一个主题，我们为这个节点设置一个订阅者对象，将这个订阅者对象加入这个属性主题的订阅者列表中。当 Model 层数据发生改变的时候，Model 作为发布者向主题发出通知，主题收到通知再向它的所有订阅者推送，订阅者收到通知后更改自己的数据。
```

详细资料可以参考：

[《Vue.js 双向绑定的实现原理》](http://www.cnblogs.com/kidney/p/6052935.html?utm_source=gold_browser_extension)

#### 110. Object.defineProperty 介绍？

```
Object.defineProperty 函数一共有三个参数，第一个参数是需要定义属性的对象，第二个参数是需要定义的属性，第三个是该属性描述符。

一个属性的描述符有四个属性，
数值属性：
分别是 value 属性的值，writable 属性是否可写，enumerable 属性是否可枚举，configurable 属性是否可配置修改。
存取器属性：
getter、enumerable 属性是否可枚举，configurable 属性是否可配置修改。
```

详细资料可以参考：
[《Object.defineProperty()》](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)

#### 111. 使用 Object.defineProperty() 来进行数据劫持有什么缺点？

```
有一些对属性的操作，使用这种方法无法拦截，比如说通过下标方式修改数组数据或者给对象新增属性，vue 内部通过重写函数解决了这个问题。在 Vue3.0 中已经不使用这种方式了，而是通过使用 Proxy 代理对象进行有关数据的拦截。使用 Proxy 的好处是它可以完美的监听到任何方式的数据改变，唯一的缺点是兼容性的问题，因为这是 ES6 的语法。
```

#### 112. 什么是 Virtual DOM？为什么 Virtual DOM 比原生 DOM 快？（######）

```
我对 Virtual DOM 的理解是：

Virtual DOM是对DOM的抽象，是更加轻量级的对DOM的描述

首先对我们将要插入到文档中的 DOM 树结构进行分析，使用 js 对象将其表示出来，比如一个元素对象，包含 TagName、props 和 Children 这些属性。然后我们将这个 js 对象树给保存下来，最后再将 DOM 片段插入到文档中。

当页面的状态发生改变，我们需要对页面的 DOM 的结构进行调整的时候，我们首先根据变更的状态，重新构建起一棵对象树，然后将这棵新的对象树和旧的对象树进行比较，记录下两棵树的的差异。

最后将记录的有差异的地方应用到真正的 DOM 树中去，这样视图就更新了。

我认为 Virtual DOM 这种方法对于我们需要有大量的 DOM 操作的时候，能够很好的提高我们的操作效率，通过在操作前确定需要做的最小修改，尽可能的减少 DOM 操作带来的重流和重绘的影响。其实 Virtual DOM 并不一定比我们真实的操作 DOM 要快，这种方法的目的是为了提高我们开发时的可维护性，在任意的情况下，都能保证一个尽量小的性能消耗去进行操作。
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-06_22-40-41.png" style="zoom: 67%;" />

虚拟DOM由h函数渲染产生，diff算法除了有精细化比较最小量更新的作用，还涵盖了将虚拟DOM变为真正的DOM的过程

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-06_22-48-49.png" style="zoom: 67%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-06_22-51-36.png" style="zoom: 67%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-24_08-03-50.png" style="zoom: 67%;" />

![](C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-07-24_08-04-09.png)

详细资料可以参考：
[《Virtual DOM》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bdc72e6e51d45054f664dbf)
[《理解 Virtual DOM》](https://github.com/y8n/blog/issues/5)
[《深度剖析：如何实现一个 Virtual DOM 算法》](https://github.com/livoras/blog/issues/13)
[《网上都说操作真实 DOM 慢，但测试结果却比 React 更快，为什么？》](https://www.zhihu.com/question/31809713/answer/53544875)

#### 113. 如何比较两个 DOM 树的差异？（#####）

```
diff算法概括来说就是精细化对比最小量更新

两个树的完全 diff 算法的时间复杂度为 O(n^3) ，但是在前端中，我们很少会跨层级的移动元素，所以我们只需要比较同一层级的元素进行比较，这样就可以将算法的时间复杂度降低为 O(n)。

算法首先会对新旧两棵树进行一个深度优先的遍历，这样每个节点都会有一个序号。在深度遍历的时候，每遍历到一个节点，我们就将这个节点和新的树中的节点进行比较，如果有差异，则将这个差异记录到一个对象中。

在对列表元素进行对比的时候，由于 TagName 是重复的，所以我们不能使用这个来对比。我们需要给每一个子节点加上一个 key，列表对比的时候使用 key 来进行比较，这样我们才能够复用老的 DOM 树上的节点。
```

#### 补充Vue和React的区别：

```
1.监听数据变化的实现原理不同：Vue通过getter/setter等函数劫持手段，可以准确知道数据的变化。而React并不采用精确监听数据变化的方式(diff)，之所以如此是因为两者的设计理念不同。Vue使用的是可变数据，而react强调数据的不可变，两者没有好坏之分，Vue更加简单，而React构建大型应用的时候更加鲁棒。
2.数据流不同：Vue支持双向数据流(数据的更改控制视图的显示；视图显示的变化更改数据的变动)，而React是单向数据流(默认只实现了数据的更改控制视图的显示，另外一个方向需要我们手动添加(onchange事件)).
3.组件间的通信
4.模板渲染方式不同：React是通过JSX渲染模板，Vue通过一种拓展的HTML语法进行渲染。此外，Vue可以更快地计算出Virtual DOM的差异，这是由于它在渲染过程中，会跟踪每一个组件的依赖关系，不需要重新渲染整个组件树。
5.框架本质不同：Vue本质是MVVM框架，由MVC发展而来；React是前端组件化框架，由后端组件化发展而来。
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/v2-f604862155689e675bdc3539f4242ba5_r.jpg" style="zoom:67%;" />



<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/v2-a82e1eafc7a220062812b6402e1546a3_r.jpg" style="zoom: 80%;" />



#### 补充Vue2.0和Vue3.0有哪些不同：

```进行
vue3.0的双向数据绑定是利用ES6的拦截器proxy实现的，Vue2.0的双向数据绑定时利用defineProperty实现的

Vue3.0对虚拟Dom进行了相关优化，相比于Vue2.0来说更快了，2是全部Dom比较而3引入静态标记只会对静态标记的dom进行比较。

Vue3.0的源码是用TypeScript重构的，可以更好的进行类型检查

Vue3.0的tree-shaking更友好，先比Vue2.0来说更小了，(摇动树，将无用的代码给删除掉(树上没用的果子给摇掉))

Vue3.0提供composition API，便于代码维护，复用性较高，最大的亮点解决了vue2.X在数据和功能业务逻辑相分离而不好维护的问题。相应的一些api比如setup、数据响应式的ref，reactive等。

3.0启动npm run serve。2.0启动npm run dev

composition api:
解决数据和功能业务逻辑相分离而不好维护的问题
setup(){
    // let count = 0;
    // 定义了一个名称叫做count变量, 这个变量的初始值是0
    // 这个变量发生改变之后, Vue会自动更新UI
    let count = ref(0);
    // 在组合API中, 如果想定义方法, 不用定义到methods中, 直接定义即可
    function myFn() {
      // alert(123);
      // console.log(count.value);
      count.value += 1;
    }
    // 注意点:
    // 在组合API中定义的变量/方法, 要想在外界使用, 必须通过return {xxx, xxx}暴露出去
    return{count, myFn}
  }
}
```

```
补充：
vue组件中data为什么是函数，
是因为js本身的特性带来的，跟vue本身设计无关。类比引用数据类型：Object是引用数据类型,如果不用function 返回,每个组件的data 都是内存的同一个地址,一个数据改变了其他也改变了;
```

#### 114. 什么是 requestAnimationFrame ？

动画是由浏览器按照一定的频率一帧一帧的绘制的，由css实现的动画的优势就是浏览器知道动画的开始及每一帧的循环间隔，能够在恰当的时间刷新UI，给用户一种流畅的体验。

浏览设备绘制间隔是`16.7ms` ，requestAnimationFrame  就按16.7ms间隔进行绘制，

css存在兼容性问题，css在滚动动画方面不行可以用requestAnimationFrame可以

详细资料可以参考：
[《你需要知道的 requestAnimationFrame》](https://juejin.im/post/5a82f0626fb9a06358657c9c)
[《CSS3 动画那么强，requestAnimationFrame 还有毛线用？》](https://www.zhangxinxu.com/wordpress/2013/09/css3-animation-requestanimationframe-tween-%E5%8A%A8%E7%94%BB%E7%AE%97%E6%B3%95/)

#### 115. 谈谈你对 webpack 的看法

```
webpack 是一个流行的前端项目构建工具（打包工具），可以解决当前 web 开发中所面临的一些问题，比如：文件依赖关系复杂、静态资源请求效率低、模块化支持不友好等等

我认为 webpack 的主要原理是，它将所有的资源都看成是一个模块，并且把页面逻辑当作一个整体，通过一个给定的入口文件，webpack 从这个文件开始，找到所有的依赖文件，将各个依赖文件模块通过 loader 和 plugins 处理后，然后打包在一起，最后输出一个浏览器可识别的 JS 文件。

Webpack 具有四个核心的概念，分别是 Entry（入口）、Output（输出）、loader 和 Plugins（插件）。在webpack.config.js文件中进行相应的设置

Entry 是 webpack 的入口起点，它指示 webpack 应该从哪个模块开始着手，来作为其构建内部依赖图的开始。

Output 属性告诉 webpack 在哪里输出它所创建的打包文件，也可指定打包文件的名称，默认位置为 ./dist。

loader 可以理解为 webpack 的加载器(编译器)，它使得 webpack 可以处理一些非 JS文件(使用loader加载器之前需要npm相应的加载器)。在对 loader 进行配置的时候，test 属性，标志有哪些后缀的文件应该被处理，是一个正则表达式。use 属性，指定 test 类型的文件应该使用哪个 loader 进行预处理。常用的 loader 有 css-loader、less-loader 等。

插件可以用于执行范围更广的任务，包括打包、优化、压缩、搭建服务器等等，要使用一个插件，一般是先使用 npm 包管理器进行安装，然后在配置文件中引入，最后将其实例化后传递给 plugins 数组属性。

使用 webpack 的确能够提供我们对于项目的管理，但是它的缺点就是调试和配置起来太麻烦了。但现在 webpack4.0 的免配置一定程度上解决了这个问题。但是我感觉就是对我来说，就是一个黑盒，很多时候出现了问题，没有办法很好的定位。
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621210619526.png" style="zoom: 80%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621210338791.png" style="zoom: 67%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621210235966.png" style="zoom: 50%;" />



详细资料可以参考：
[《不聊 webpack 配置，来说说它的原理》](https://juejin.im/post/5b38d27451882574d87aa5d5#heading-0)
[《前端工程化——构建工具选型：grunt、gulp、webpack》](https://juejin.im/entry/5b5724d05188251aa01647fd)
[《浅入浅出 webpack》](https://juejin.im/post/5afa9cd0f265da0b981b9af9#heading-0)
[《前端构建工具发展及其比较》](https://juejin.im/entry/5ae5c8c9f265da0b9f400d8e)

#### 116. offsetWidth/offsetHeight,clientWidth/clientHeight,scrollWidth/scrollHeight 的区别？

目标对象的属性：

```
clientWidth/clientHeight 返回的是元素的内部宽度，它的值只包含 content + padding，如果有滚动条，不包含滚动条。
clientTop 返回的是上边框的宽度。
clientLeft 返回的左边框的宽度。

offsetWidth/offsetHeight 返回的是元素的布局宽度，它的值包含 content + padding + border 包含了滚动条。
offsetTop 返回的是当前元素相对于其 offsetParent 元素的顶部的距离。
offsetLeft 返回的是当前元素相对于其 offsetParent 元素的左部的距离。

scrollWidth/scrollHeight 返回值包含 content + padding + 溢出内容的尺寸。
scrollTop 属性返回的是一个元素的内容垂直滚动的像素数。
scrollLeft 属性返回的是元素滚动条到元素左边的距离。
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621213158707.png" style="zoom:80%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621213240983.png" style="zoom:80%;" />

![](C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621213341233.png)

![](C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621214505236.png)

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621213633966.png" style="zoom:80%;" />

![](C:\Users\88520\Desktop\前端\3.面试\blog-master\img/image-20210621213529233.png)

详细资料可以参考：
[《最全的获取元素宽高及位置的方法》](https://juejin.im/post/5bc9366d5188255c4834e75a)
[《用 Javascript 获取页面元素的位置》](http://www.ruanyifeng.com/blog/2009/09/find_element_s_position_using_javascript.html)

#### 117. 谈一谈你理解的函数式编程？

```
简单说，"函数式编程"是一种"编程范式"（programming paradigm），也就是如何编写程序的方法论。

它具有以下特性：
函数是"第一等公民"：指的是函数与其他数据类型一样，处于平等地位，可以赋值给其他变量，也可以作为参数，传入另一个函数，或者作为别的函数的返回值
只用"表达式"。

常见的函数式编程:
闭包和高阶函数、递归、回调函数等等...
```

详细资料可以参考：
[《函数式编程初探》](http://www.ruanyifeng.com/blog/2012/04/functional_programming.html)

#### 118. 异步编程的实现方式？

相关资料：

```
回调函数
优点：简单、容易理解
缺点：不利于维护，代码耦合高

事件监听（采用时间驱动模式，取决于某个事件是否发生）：
优点：容易理解，可以绑定多个事件，每个事件可以指定多个回调函数
缺点：事件驱动型，流程不够清晰

发布/订阅（观察者模式）
类似于事件监听，但是可以通过‘消息中心’，了解现在有多少发布者，多少订阅者

Promise 对象
优点：可以利用 then 方法，进行链式写法；可以书写错误时的回调函数；
缺点：编写和理解，相对比较难

Generator 函数
优点：函数体内外的数据交换、错误处理机制
缺点：流程管理不方便

async 函数
优点：内置执行器、更好的语义、更广的适用性、返回的是 Promise、结构清晰。
缺点：错误处理机制
```

回答：

```
js 中的异步机制可以分为以下几种：

第一种最常见的是使用回调函数的方式，使用回调函数的方式有一个缺点是，多个回调函数嵌套的时候会造成回调函数地狱，上下两层的回调函数间的代码耦合度太高，不利于代码的可维护。

第二种是 Promise 的方式，使用 Promise 的方式可以将嵌套的回调函数作为链式调用。但是使用这种方法，有时会造成多个 then 的链式调用，可能会造成代码的语义不够明确。

第三种是使用 generator 的方式，当generator函数在执行过程中遇到异步的函数的时候，将函数执行权转移出去，当异步的函数执行完毕的时候我们再将执行权给转移回来。因此我们在 generator 内部对于异步操作的方式，可以以同步的顺序来书写。使用这种方式我们需要考虑的问题是何时将函数的控制权转移回来，因此我们需要有一个自动执行 generator 的机制，比如说 co 模块等方式来实现 generator 的自动执行。

任何函数，只要参数有回调函数，就能写成 Thunk 函数的形式
generator函数中yield命令用于将程序的执行权移出 Generator 函数
有两种常用方式可以将执行权交回generator函数：
（1）回调函数。将异步操作包装成 Thunk 函数，在回调函数里面交回执行权。
（2）Promise 对象。将异步操作包装成 Promise 对象，用then方法交回执行权

第四种是使用 async 函数的形式，async 函数是 generator函数的语法糖，内部再带自动执行器，相比于generator函数中yield 后面只能是thunk函数或promise对象而言，async函数await后面可以是原始值或promise对象，此外generator函数返回的是一个iterator对象而async函数放回的是一个promise对象更便于后续的处理。当函数内部执行到一个 await 语句的时候，如果语句返回一个 promise 对象，那么函数将会等待 promise 对象的状态变为 resolve 后再继续向下执行。因此我们可以将异步逻辑，转化为同步的顺序来书写。
```

#### 119. Js 动画与 CSS 动画区别及相应实现

```
CSS3 的动画的优点

动画是由浏览器按照一定的频率一帧一帧的绘制的，由css实现的动画的优势就是浏览器知道动画的开始及每一帧的循环间隔，能够在恰当的时间刷新UI，给用户一种流畅的体验。所以在性能上会稍微好一些，浏览器会对 CSS3 的动画做一些优化
代码相对简单

缺点

在动画控制上不够灵活
兼容性不好

JavaScript 的动画正好弥补了这两个缺点，控制能力很强，可以单帧的控制、变换，同时写得好完全可以兼容 IE6，并且功能强大。对于一些复杂控制的动画，使用 javascript 会比较靠谱。而在实现一些小的交互动效的时候，就多考虑考虑 CSS 吧
```

#### 120. get 请求传参长度的误区

```
误区：我们经常说 get 请求参数的大小存在限制，而 post 请求的参数大小是无限制的。

实际上 HTTP 协议从未规定 GET/POST 的请求长度限制是多少。对 get 请求参数的限制是来源与浏览器或web 服务器，浏览器或 web 服务器限制了 url 的长度。为了明确这个概念，我们必须再次强调下面几点:
```

- 1.HTTP 协议未规定 GET 和 POST 的长度限制
- 2.GET 的最大长度显示是因为浏览器和 web 服务器限制了 URI 的长度
- 3.不同的浏览器和 WEB 服务器，限制的最大长度不一样
- 4.要支持 IE，则最大长度为 2083byte，若只支持 Chrome，则最大长度 8182byte

#### 121. URL 和 URI 的区别？

```
URI: Uniform Resource Identifier      指的是统一资源标识符
URL: Uniform Resource Location        指的是统一资源定位符
URN: Universal Resource Name          指的是统一资源名称

URI 指的是统一资源标识符，用唯一的标识来确定一个资源，它是一种抽象的定义，也就是说，不管使用什么方法来定义，只要能唯一的标识一个资源，就可以称为 URI。

URL 指的是统一资源定位符，URN 指的是统一资源名称。URL 和 URN 是 URI 的子集，URL 可以理解为使用地址来标识资源，URN 可以理解为使用名称来标识资源。
```

详细资料可以参考：
[《HTTP 协议中 URI 和 URL 有什么区别？》](https://www.zhihu.com/question/21950864)
[《你知道 URL、URI 和 URN 三者之间的区别吗？》](http://web.jobbole.com/83452/)
[《URI、URL 和 URN 的区别》](https://segmentfault.com/a/1190000006081973)

#### 122. get 和 post 请求在缓存方面的区别

相关知识点：

```
get 请求类似于查找的过程，用户获取数据，可以不用每次都与数据库连接，所以可以使用缓存。

post 不同，post 做的一般是修改和删除的工作，所以必须与数据库交互，所以不能使用缓存。因此 get 请求适合于请求缓存。
```

回答：

```
缓存一般只适用于那些不会更新服务端数据的请求。一般 get 请求都是查找请求，不会对服务器资源数据造成修改，而 post 请求一般都会对服务器数据造成修改，所以，一般会对 get 请求进行缓存，很少会对 post 请求进行缓存。
```

详细资料可以参考：
[《HTML 关于 post 和 get 的区别以及缓存问题的理解》](https://blog.csdn.net/qq_27093465/article/details/50479289)

#### 123. 图片的懒加载和预加载

相关知识点：

```
预加载：提前加载图片，当用户需要查看时可直接从本地缓存中渲染。

懒加载：懒加载的主要目的是作为服务器前端的优化，减少请求数或延迟请求数。

两种技术的本质：两者的行为是相反的，一个是提前加载，一个是迟缓甚至不加载。 懒加载对服务器前端有一定的缓解压力作用，预加载则会增加服务器前端压力。
```

回答：

```
懒加载也叫延迟加载，指的是在长网页中延迟加载图片的时机，当用户需要访问时，再去加载，这样可以提高网站的首屏加载速度，提升用户的体验，并且可以减少服务器的压力。它适用于图片很多，页面很长的电商网站的场景。懒加载的实现原理是，将页面上的图片的 src 属性设置为空字符串，将图片的真实路径保存在一个自定义属性中，当页面滚动的时候，进行判断，如果图片进入页面可视区域内，则从自定义属性中取出真实路径赋值给图片的 src 属性，以此来实现图片的延迟加载。

预加载指的是将所需的资源提前请求加载到本地，这样后面在需要用到时就直接从缓存取资源。通过预加载能够减少用户的等待时间，提高用户的体验。我了解的预加载的最常用的方式是使用 js 中的 image 对象，通过为 image 对象来设置 scr 属性，来实现图片的预加载。

这两种方式都是提高网页性能的方式，两者主要区别是一个是提前加载，一个是迟缓甚至不加载。懒加载对服务器前端有一定的缓解压力作用，预加载则会增加服务器前端压力。
```

|                                                              | preload                                         | prefetch                                           |
| ------------------------------------------------------------ | ----------------------------------------------- | -------------------------------------------------- |
| 语法                                                         | <link rel="preload" href="bg-image-narrow.png"> | <link rel="prefetch" href="bg-image-narrow.png" /> |
| 加载时间                                                     | 立即加载                                        | 浏览器闲置的时候才会加载（一般而言）               |
| 用户正在登陆页面，登陆成功之后会跳转到首页。我是否可以在登陆页面就去请求首页的资源呢？ | 用户从A页面进入B页面，preload的会失效           | 而prefetch的内容可以在B页面使用。                  |

详细资料可以参考：
[《懒加载和预加载》](https://juejin.im/post/5b0c3b53f265da09253cbed0)
[《网页图片加载优化方案》](https://juejin.im/entry/5a73f38cf265da4e99575be3)
[《基于用户行为的图片等资源预加载》](https://www.zhangxinxu.com/wordpress/2016/06/image-preload-based-on-user-behavior/)

#### 124. mouseover 和 mouseenter 的区别？

```
当鼠标移动到元素上时就会触发 mouseenter 事件，类似 mouseover，它们两者之间的差别是 mouseenter 不会冒泡。

由于 mouseenter 不支持事件冒泡，导致在一个元素的子元素上进入或离开的时候会触发其 mouseover 和 mouseout 事件，但是却不会触发 mouseenter 和 mouseleave 事件。
```

常见的鼠标事件：

click 单击、 contextmenu 右击、 dbclick  双击、 mousedown 鼠标按下、 mouseup 鼠标弹起、 mousemove 鼠标移动

mouseover 鼠标移入元素、 mouseout 鼠标移出元素、 mouseenter 移入元素、 mouseleave 移出元素 （这两个不支持冒泡）

详细资料可以参考：
[《mouseenter 与 mouseover 为何这般纠缠不清？》](https://github.com/qianlongo/zepto-analysis/issues/1)

#### 125. js 拖拽功能的实现

相关知识点：

```
首先是三个事件，分别是 mousedown，mousemove，mouseup
当鼠标点击按下的时候，需要一个 tag 标识此时已经按下，可以执行 mousemove 里面的具体方法。
clientX，clientY 标识的是鼠标的坐标，分别标识横坐标和纵坐标，并且我们用 offsetX 和 offsetY 来表示
元素的元素的初始坐标，移动的举例应该是：
鼠标移动时候的坐标-鼠标按下去时候的坐标。
也就是说定位信息为：
鼠标移动时候的坐标-鼠标按下去时候的坐标+元素初始情况下的 offetLeft.
```

回答：

```
一个元素的拖拽过程，我们可以分为三个步骤，第一步是鼠标按下目标元素，第二步是鼠标保持按下的状态移动鼠标，第三步是鼠
标抬起，拖拽过程结束。

这三步分别对应了三个事件，mousedown 事件，mousemove 事件和 mouseup 事件。只有在鼠标按下的状态移动鼠标我们才会
执行拖拽事件，因此我们需要在 mousedown 事件中设置一个状态来标识鼠标已经按下，然后在 mouseup 事件中再取消这个状
态。在 mousedown 事件中我们首先应该判断，目标元素是否为拖拽元素，如果是拖拽元素，我们就设置状态并且保存这个时候鼠
标的位置。然后在 mousemove 事件中，我们通过判断鼠标现在的位置和以前位置的相对移动，来确定拖拽元素在移动中的坐标。
最后 mouseup 事件触发后，清除状态，结束拖拽事件。


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .calculator {
            position: absolute;
            /*设置绝对定位，脱离文档流，便于拖拽*/
            /* display: block; */
            width: 100px;
            height: 100px;
            background-color: pink;
            cursor: move;
            /*鼠标呈拖拽状*/
        }
    </style>
</head>

<body>
    <div class="calculator" id="drag"></div>
    <script>
        window.onload = function() {
            //拖拽功能(主要是触发三个事件：onmousedown\onmousemove\onmouseup)
            var drag = document.getElementById('drag');

            //点击某物体时，用drag对象即可，move和up是全局区域，也就是整个文档通用，应该使用document对象而不是drag对象
            (否则，采用drag对象时物体只能往右方或下方移动)
            drag.onmousedown = function(e) {
                var e = e || window.event; //兼容ie浏览器
                var diffX = e.clientX - drag.offsetLeft; //鼠标点击物体那一刻相对于物体左侧边框的距离=
                点击时的位置相对于浏览器最左边的距离-物体左边框相对于浏览器最左边的距离
                var diffY = e.clientY - drag.offsetTop;

                /*低版本ie bug:物体被拖出浏览器可是窗口外部时，还会出现滚动条，
                	解决方法是采用ie浏览器独有的2个方法setCapture()\releaseCapture(),这两个方法，
                	可以让鼠标滑动到浏览器外部也可以捕获到事件，而我们的bug就是当鼠标移出浏览器的时候，
                	限制超过的功能就失效了。用这个方法，即可解决这个问题。注：这两个方法用于onmousedown和onmouseup中*/
                // if (typeof drag.setCapture != 'undefined') {
                //     drag.setCapture();
                // }

                document.onmousemove = function(e) {
                    var e = e || window.event; //兼容ie浏览器
                    var left = e.clientX - diffX;
                    var top = e.clientY - diffY;

                    //控制拖拽物体的范围只能在浏览器视窗内，不允许出现滚动条
                    if (left < 0) {
                        left = 0;
                    } else if (left > window.innerWidth - drag.offsetWidth) {
                        left = window.innerWidth - drag.offsetWidth;
                    }
                    if (top < 0) {
                        top = 0;
                    } else if (top > window.innerHeight - drag.offsetHeight) {
                        top = window.innerHeight - drag.offsetHeight;
                    }

                    //移动时重新得到物体的距离，解决拖动时出现晃动的现象
                    drag.style.left = left + 'px';
                    drag.style.top = top + 'px';
                };
                document.onmouseup = function(e) { //当鼠标弹起来的时候不再移动
                    this.onmousemove = null;
                    this.onmouseup = null; //预防鼠标弹起来后还会循环（即预防鼠标放上去的时候还会移动）

                    //修复低版本ie bug
                    // if (typeof drag.releaseCapture != 'undefined') {
                    //     drag.releaseCapture();
                    // }
                };
            };
        };
    </script>
</body>

</html>
```

事件对象的属性：

clientX：当鼠标事件发生时（不管是onclick，还是omousemove，onmouseover等），鼠标相对于浏览器（这里说的是浏览器的有效区域）x轴的位置；
clientY：当鼠标事件发生时，鼠标相对于浏览器（这里说的是浏览器的有效区域）y轴的位置；
screenX：当鼠标事件发生时，鼠标相对于显示器屏幕x轴的位置；
screenY：当鼠标事件发生时，鼠标相对于显示器屏幕y轴的位置；
offsetX：当鼠标事件发生时，鼠标相对于事件源x轴的位置
offsetY：当鼠标事件发生时，鼠标相对于事件源y轴的位置

HTML5拖动事件集：

针对拖拽元素：

- **dragstart**  当鼠标点中元素并且开始移动时，就会触发dragstart事件（类比mousedown） 

- **drag**  拖拽过程中会持续不断地触发drag事件（类比mousemove） 

- **dragend**  松开鼠标取消拖拽时就会触发dragend事件（类比mouseup）

针对拖拽的目标元素：

- **dragenter**  拖拽元素到目标上，就会触发dragenter事件（类比mouseover） 
- **dragover**  当拖动元素在目标元素中，就会持续触发dragover事件 
- **dragleave**  离开目标元素，触发dragleave事件（类比mouseout）
- **drop**  若拖放元素到了目标元素中（在目标元素中松开鼠标），就会触发drop事件而不会触发dragleave事件

详细资料可以参考：
[《原生 js 实现拖拽功能基本思路》](https://blog.csdn.net/LZGS_4/article/details/43523465)

#### ***126. 如何使用 setTimeout 实现 setInterval？怎么模拟？

相关知识点：

```js
// 思路是使用递归函数，不断地去执行 setTimeout 从而达到 setInterval 的效果

function mySetInterval(fn, timeout) {
  // 控制器，控制定时器是否继续执行
  var timer = {
    flag: true
  };

  // 设置递归函数，模拟定时器执行。
  function interval() {
    if (timer.flag) {
      fn();
      setTimeout(interval, timeout);
    }
  }

  // 启动定时器
  setTimeout(interval, timeout);

  // 返回控制器
  return timer;
}
```

回答：

```
setInterval 的作用是每隔一段指定时间执行一个函数，但是这个执行不是真的到了时间立即执行，它真正的作用是每隔一段时间将事件函数加入事件队列中去，只有当当前的执行栈为空的时候，才能去从事件队列中取出事件函数并执行。所以可能会出现这样的情况，就是当前执行栈执行的时间很长，导致事件队列里边积累多个定时器加入的事件函数，当执行栈结束的时候，这些事件函数会依次执行，因此就不能到间隔一段时间执行的效果。

针对 setInterval 的这个缺点，我们可以使用定时器 setTimeout 递归调用来模拟 setInterval，这样我们就确保了只有一个事件函数执行结束了，我们才会触发下一个定时器，这样解决了 setInterval 的问题。
```

详细资料可以参考：
[《用 setTimeout 实现 setInterval》](https://www.jianshu.com/p/32479bdfd851)
[《setInterval 有什么缺点？》](https://zhuanlan.zhihu.com/p/51995737)

#### 127. let 和 const 的注意点？

- 1.声明的变量只在声明时的代码块内有效
- 2.不存在声明提升
- 3.存在暂时性死区，如果在变量声明前使用，会报错
- 4.不允许重复声明，重复声明会报错

#### 128. 什么是 rest 参数？

```
rest 参数（形式为...变量名），将函数的实参放入数组，其作用类似于arguments实参列表对象主要是获取多余形参个数的实参的引用
```

#### 129. 什么是尾调用，使用尾调用有什么好处？

```
尾调用指的是函数的最后一步调用另一个函数。我们代码执行是基于执行栈的，所以当我们在一个函数里调用另一个函数时，我们会保留当前的执行上下文，然后再新建另外一个执行上下文加入栈中。使用尾调用的话，因为已经是函数的最后一步，所以这个时候我们可以不必再保留当前的执行上下文，从而节省了内存，这就是尾调用优化。但是 ES6 的尾调用优化只在严格模式下开启，正常模式是无效的。

尾调用自身就是尾递归
```

#### 130. Symbol 类型的注意点？

- 1.Symbol 函数前不能使用 new 命令，否则会报错。
- 2.Symbol 函数可以接受一个字符串作为参数，表示对 Symbol 实例的描述，主要是为了在控制台显示，或者转为字符串时，比较容易区分。
- 3.Symbol 作为属性名，该属性不会出现在 for...in、for...of 循环中，也不会被 Object.keys()、Object.getOwnPropertyNames()、JSON.stringify() 返回。
- 4.Object.getOwnPropertySymbols 方法返回一个数组，成员是当前对象的所有用作属性名的 Symbol 值。
- 5.Symbol.for 接受一个字符串作为参数，然后搜索有没有以该参数作为名称的 Symbol 值。如果有，就返回这个 Symbol 值，否则就新建并返回一个以该字符串为名称的 Symbol 值。
- 6.Symbol.keyFor 方法返回一个已登记的 Symbol 类型值的 key。

#### 131. Set 和 WeakSet 结构？

- 1.ES6 提供了新的数据结构 Set。它类似于数组，但是成员的值都是唯一的，没有重复的值。

  set的实例方法以及属性：

  set初始化 new Set(***) 可以接受一个具有iterator接口的对象来初始化，最常见的比如数组

  add(value)  has(value)  delete(value)  clear()  size属性

  keys()  entries()  values()  返回相应的遍历器对象(其中键和值都返回的是值)  forEach()  用回调函数遍历每个成员

- 2.WeakSet 结构与 Set 类似，也是不重复的值的集合。但是 WeakSet 的成员只能是对象，而不能是其他类型的值。WeakSet 中的对象都是弱引用，即垃圾回收机制不考虑 WeakSet 对该对象的引用，当外界不引用该对象元素时该对象元素会直接消失，也就是说垃圾回收机制直接回收该对象元素所占用的内存.

  相关属性以及方法：

  WeakSet初始化  new WeakSet(***)  可以接受一个具有iterator接口的对象来初始化，且这个对象中的每一项元素也都是一个对象

  add()  has()  delete()

  由于其元素对象是弱引用的，随时都有可能从内存消失，所以没有遍历相关的方法

#### 132. Map 和 WeakMap 结构？

- 1.Map 数据结构。它类似于对象，也是键值对的集合，但是“键”的范围不限于字符串，各种类型的值（包括对象）都可以当作键

  将hash结构由对象的字符串--值的对应扩充到了值--值的对应。

  相关属性以及方法：

  Map初始化  new Map(***)  可以接受一个具有iterator接口的对象来初始化，且这个对象中的每一项元素都是一个双元素数组

  set(key, value)  get(key)  has(key)  delete(key)  clear()

  keys()  entries()  values()  返回相应的遍历器对象     forEach()  用回调函数遍历每个成员

- 2.WeakMap 结构与 Map 结构类似，也是用于生成键值对的集合。但是 WeakMap 只接受对象作为键名（ null 除外），不接受其他类型的值作为键名。而且 WeakMap 的键名所指向的对象，不计入垃圾回收机制，即键名所引用的对象采用的也是弱引用。也就是没有外界的引用，垃圾回收机制就会直接释放该对象键名以及相应键值所占用的内存。即，一旦不再需要，WeakMap 里面的键名对象和所对应的键值对会自动消失，不用手动删除引用。

  相关属性和方法：

  set(key, value)  get(key)  has(key)  delete(key)

  由于元素的键名是弱引用的，随时都有可能从内存消失，所以没有遍历相关的方法。

#### 133. 什么是 Proxy ？

```
Proxy 用于修改某些操作的默认行为，等同于在语言层面做出修改，所以属于一种“元编程”，即对编程语言进行编程。

Proxy 可以理解成，在目标对象之前架设一层“拦截”，外界对该对象的访问，都必须先通过这层拦截，因此提供了一种机制，可以对外界的访问进行过滤和改写。Proxy 这个词的原意是代理，用在这里表示由它来“代理”某些操作，可以译为“代理器”。

var proxy = new Proxy(target, handler);
new Proxy()表示生成一个Proxy实例，target参数表示所要拦截的目标对象，handler参数也是一个对象，用来定制拦截行为。
```

#### 134. Reflect 对象创建目的？

- 1.将 Object 对象的一些明显属于语言内部的方法（比如 Object.defineProperty，放到 Reflect 对象上。
- 2.修改某些 Object 方法的返回结果，让其变得更合理。如上述方法在，无法定义属性时，会抛出一个错误，而调用reflect对象上相关的方法，无法定义属性时只会返回一个false。
- 3.让 Object 操作都变成函数行为。如`Reflect.has(obj, name)`和`Reflect.deleteProperty(obj, name)`让它们变成了函数行为
- 4.Reflect 对象的方法与 Proxy 对象的方法一一对应，只要是 Proxy 对象的方法，就能在 Reflect 对象上找到对应的方法。这就让 Proxy 对象可以方便地调用对应的 Reflect 方法，完成默认行为，作为修改行为的基础。也就是说，不管 Proxy 怎么修改默认行为，你总可以在 Reflect 上获取默认行为。

#### 135. require 模块引入的查找方式？

```
当 Node 遇到 require(X) 时，按下面的顺序处理。

（1）如果 X 是内置模块（比如 require('http')）
　　a. 返回该模块。
　　b. 不再继续执行。

（2）如果 X 以 "./" 或者 "/" 或者 "../" 开头
　　a. 根据 X 所在的父模块，确定 X 的绝对路径。
　　b. 将 X 当成文件，依次查找下面文件，只要其中有一个存在，就返回该文件，不再继续执行。
    X
    X.js
    X.json
    X.node

　　c. 将 X 当成目录，依次查找下面文件，只要其中有一个存在，就返回该文件，不再继续执行。
    X/package.json（main字段）
    X/index.js
    X/index.json
    X/index.node

（3）如果 X 不带路径
　　a. 根据 X 所在的父模块，确定 X 可能的安装目录。
　　b. 依次在每个目录中，将 X 当成文件名或目录名加载。

（4）抛出 "not found"
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-06-22_19-06-05.png" style="zoom: 80%;" />

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-06-22_19-06-45.png" style="zoom:80%;" />

package.json  npm init -y (初始化才会出现在项目目录中记录安装了那些三方包) dependencies 项目依赖   devDependencies  开发依赖

 package-lock.json

详细资料可以参考：
[《require() 源码解读》](http://www.ruanyifeng.com/blog/2015/05/require.html)

#### 136. 什么是 Promise 对象，什么是 Promises/A+ 规范？

```
简单来说promise相当于一个容器，里面存放着某个未来才会结束的事件的结果，通常是个异步操作。
从语法上来看promise作为一个对象，他会产生成功的结果或者失败的拒因。

Promise 对象是异步编程的一种解决方案，最早由社区提出。Promises/A+ 规范规定了一个 Promise 所必须具有的特性。

Promise 是一个构造函数，接收一个函数作为参数，返回一个 Promise 实例。一个 Promise 实例有三种状态:
分别是 pending(进行中)、resolved(已成功) 和 rejected(已失败)。
实例的状态只能由 pending 转变 resolved 或者 rejected 状态，并且状态一经改变，就无法再被改变了。

const promise = new Promise(function(resolve, reject) {
  // ... some code

  if (/* 异步操作成功 */){
    resolve(value);
  } else {
    reject(error);
  }
});
Promise构造函数接受一个函数作为参数，该函数的两个参数也是函数分别是resolve和reject。
resolve函数的作用是，将Promise对象的状态从 pending 变为 resolved,并将成功的结果作为参数传递出去
reject函数的作用是，将Promise对象的状态从pending 变为 rejected,并将失败的拒因作为参数传递出去，其作用等价于throw个错误出去

promise.then(function(value) {
  // success
}, function(error) {
  // failure
});
Promise实例生成以后，可以用then方法分别指定resolved状态和rejected状态的回调函数，从回调函数的参数中拿取传递出来的成功结果或者失败的拒因。

这里的回调函数属于微任务，会在本轮事件循环的末尾执行。

//==================================================================================
Promise实例的相关方法：
1.Promise.prototype.then()  
第一个参数是resolved状态(成功结果)的回调函数，第二个参数是rejected状态(失败拒因)的回调函数；then方法返回一个新的Promise实例，因此可以采用链式写法。

2.Promise.prototype.catch() 
参数是rejected状态(失败拒因)的回调函数，catch方法可以捕捉到Promise实例rejected状态时的拒因，同时也可以抓到在他之前的then方法或catch方法中回调函数的错误

3.Promise.prototype.finally()
用于指定不管 Promise 对象最后状态如何，都会执行的操作

//===============================================================================
Promise的相关静态方法：

1.Promise.all()方法用于将多个 Promise 实例，包装成一个新的 Promise 实例，
const p = Promise.all([p1, p2, p3]);
参数为一个具有iterator接口的数据，一般就用数组，数组中的每一项都是一个promise实例，如果不是则会先被转为promise实例
只有p1、p2、p3的状态都变成fulfilled，p的状态才会变成fulfilled，此时p1、p2、p3的返回值组成一个数组，传递给p的回调函数。
只要p1、p2、p3之中有一个被rejected，p的状态就变成rejected，此时第一个被reject的实例的返回值，会传递给p的回调函数。

2.Promise.race()方法同样是将多个 Promise 实例，包装成一个新的 Promise 实例。
const p = Promise.race([p1, p2, p3]);
只要p1、p2、p3之中有一个实例率先改变状态，p的状态就跟着改变。那个率先改变的 Promise 实例的返回值，就传递给p的回调函数。

3.Promise.allSettled()方法接受一组 Promise 实例作为参数，包装成一个新的 Promise 实例。
只有等到所有这些参数实例都返回结果，不管是fulfilled还是rejected，包装实例才会结束，且状态只能是总是fulfilled，所有实例的返回值组成一个数组，传递给包装实例的回调函数。

4.Promise.any()方法。该方法接受一组 Promise 实例作为参数，包装成一个新的 Promise 实例返回，
只要参数实例有一个变成fulfilled状态，包装实例就会变成fulfilled状态；
如果所有参数实例都变成rejected状态，包装实例就会变成rejected状态。

5.Promise.resolve()方法将现有对象转为 Promise 对象，状态为resolved
6.Promise.reject(reason)方法也会返回一个新的 Promise 实例，该实例的状态为rejected
7.Promise.try()代码块中的同步错误，异步错误，都可以被catch到。
```

详细资料可以参考：
[《Promises/A+ 规范》](http://www.ituring.com.cn/article/66566)
[《Promise》](http://es6.ruanyifeng.com/#docs/promise#Promise-resolve)

```javascript
数字打印的顺序
const first = () => (new Promise((resolve, reject) => {
    console.log(3);
    let p = new Promise((resolve, reject) => {
        console.log(7);
        setTimeout(() => {
            console.log(5);
            //6不会被执行了，因为promise的状态在resolve(1)的时候就已经发生改变了，不会在重新改变了
            resolve(6);
        }, 0)
        resolve(1);
    });
    resolve(2);
    p.then((arg) => {
        console.log(arg);
    });
}));
 
first().then((arg) => {
    console.log(arg);
});
console.log(4);


//同步的代码（最高）
//3
//7
//4

//微任务的异步代码（次高，then）
//1
//2

//宏任务的异步代码（最低，setTimeout）
//5

//6 不执行
```

```javascript
// 画出以下异步函数执行的可能的路线。
// https://developers.google.com/web/fundamentals/primers/promises
// 蓝线表示执行的 promise 路径，红路表示拒绝的 promise 路径。
// https://developers.google.com/web/fundamentals/primers/imgs/promise-flow.svg
asyncThing1()
  .then(function() {
    return asyncThing2();
  })
  .then(function() {
    return asyncThing3();
  })
  .catch(function(err) {
    return asyncRecovery1();
  })
  .then(
    function() {
      return asyncThing4();
    },
    function(err) {
      return asyncRecovery2();
    }
  )
  .catch(function(err) {
    console.log("Don't worry about it");
  })
  .then(function() {
    console.log("All done!");
  });


then方法中第一个参数是resolved状态的回调函数、第二个参数是rejected状态的回调函数，前者捕捉promise对象成功的结果，后者捕捉promise对象失败的拒因
而catch方法的参数作为rejected状态的回调函数，他除了捕捉promise对象失败的拒因，还可以捕捉他前面then方法中可能出现的错误，所以最好使用catch
而不是then方法的第二个参数，来捕捉失败的拒因。
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/0082zybpgy1gbx4j86yaaj30oi0mdwn1.jpg" style="zoom: 50%;" />

#### 137. 手写一个 Promise

只是最简单的promise功能的实现，并不完整，完整版git-code

```js
const PENDING = "pending";
const RESOLVED = "resolved";
const REJECTED = "rejected";

function MyPromise(fn) {
  // 保存初始化状态
  var self = this;

  // 初始化状态
  this.state = PENDING;

  // 用于保存 resolve 或者 rejected 传入的值
  this.value = null;

  // 用于保存 resolve 的回调函数
  this.resolvedCallbacks = [];

  // 用于保存 reject 的回调函数
  this.rejectedCallbacks = [];

  // 状态转变为 resolved 方法
  function resolve(value) {
    // 判断传入元素是否为 Promise 值，如果是，则状态改变必须等待前一个状态改变后再进行改变
    if (value instanceof MyPromise) {
      return value.then(resolve, reject);
    }

    // 保证代码的执行顺序为本轮事件循环的末尾
    setTimeout(() => {
      // 只有状态为 pending 时才能转变，
      if (self.state === PENDING) {
        // 修改状态
        self.state = RESOLVED;

        // 设置传入的值
        self.value = value;

        // 执行回调函数
        self.resolvedCallbacks.forEach(callback => {
          callback(value);
        });
      }
    }, 0);
  }

  // 状态转变为 rejected 方法
  function reject(value) {
    // 保证代码的执行顺序为本轮事件循环的末尾
    setTimeout(() => {
      // 只有状态为 pending 时才能转变
      if (self.state === PENDING) {
        // 修改状态
        self.state = REJECTED;

        // 设置传入的值
        self.value = value;

        // 执行回调函数
        self.rejectedCallbacks.forEach(callback => {
          callback(value);
        });
      }
    }, 0);
  }

  // 将两个方法传入函数执行
  try {
    fn(resolve, reject);
  } catch (e) {
    // 遇到错误时，捕获错误，执行 reject 函数
    reject(e);
  }
}

MyPromise.prototype.then = function(onResolved, onRejected) {
  // 首先判断两个参数是否为函数类型，因为这两个参数是可选参数
  onResolved =
    typeof onResolved === "function"
      ? onResolved
      : function(value) {
          return value;
        };

  onRejected =
    typeof onRejected === "function"
      ? onRejected
      : function(error) {
          throw error;
        };

  // 如果是等待状态，则将函数加入对应列表中
  if (this.state === PENDING) {
    this.resolvedCallbacks.push(onResolved);
    this.rejectedCallbacks.push(onRejected);
  }

  // 如果状态已经凝固，则直接执行对应状态的函数

  if (this.state === RESOLVED) {
    onResolved(this.value);
  }

  if (this.state === REJECTED) {
    onRejected(this.value);
  }
};
```

async+await：

async 函数中遇到await，则先将await 后面的操作执行完成之后，才会执行后续的代码，也就是说如果有两个console.log同步代码，await之前就同步执行，await之后就异步执行，await之后的console.log就相当于任务的第二段，等到await后面的异步操作完成，满足了条件在去执行其之后的console.log，相当于await后续的同步代码会变成异步的，而如果await后面是同步操作则其仍是同步执行的.

async function test(){

console.log(1);  //同步执行

await  console.log('2‘); //同步执行

console.log(3) //异步执行

} 

test(); console.log(4)

执行顺序：1 2 4 3 

```
console.log(0)
new Promise((resolve) => {
    console.log(1);
    resolve(console.log(2));
    console.log(3);
}).then(() => { console.log(5) })
console.log(4)

执行顺序0 1 2 3 4 5
```

```
综上：对于promise而言只有你then方法中的东西是异步的，其他地方的是同步的就是同步的，异步的就是异步的
对于async+await而言，await后面的代码是异步的就异步执行，同步的就同步执行，其他地方是同步的
```

```
new Promise((resolve) => {
    console.log('0')
    setTimeout(() => {
        console.log(1);
        resolve(2);
    }, 1000);
    console.log('00');
}).then(res => console.log(res))
console.log('000');

0
00
000
//这里是在异步setTimeout中触发了promise的第二段任务
1
2
```

*async函数返回一个promise对象，可以供后续的链式操作

*await只能出现在async函数中，其后接一个promise对象，如果接的是原始值，则会转为状态为resolved的promise对象，如果是包含then方法的对象，也会将其等同于promise对象。

*async函数中return出来的结果会被then方法回调函数的参数捕捉到；throw出来的结果()会被catch方法回调函数的参数捕捉到；如果是await 后面promise对象的状态变为reject，则reject出来的结果也会被catch捕捉到，就等同于throw个错误出来。也就是说不管throw还是await 后面promise对象的状态变为reject都会被catch抓住。如果想，即使当前异步操作失败后续异步操作还能继续执行，可以将这个await 连同后面的promise对象 都try catch一下（try catch这个throw），或者await后面跟的promise对象先catch。

可以发现`reject()`方法的作用，等同于抛出错误

*async函数返回的promise对象，必须等到其内部所有await命令后面的 Promise 对象执行完，才会发生状态改变，除非遇到 return语句或者throw出错误。也就是说，只有`async`函数内部的异步操作执行完，才会执行`then`方法指定的回调函数。此外如果你await都执行完了，没有return、throw什么东西、或者是await后的promise也没有失败，则这个异步函数返回的promise对象也只是状态发生了改变，而不能then、或是catch出什么结果出来。

*多个`await`命令后面的异步操作，如果不存在继发关系，最好让它们同时触发。

```
Promise中如果想要同步代码同步执行，异步代码异步执行有三种方法：
现有代码fn()

第一种，将代码fn()放到resolve函数中，resolve用来触发promise的状态为resolved，其函数参数作为then方法回调函数的参数，你把代码塞到resolve中，同步代码同步执行，异步代码异步执行。

第二种，将代码fn()放到async函数await 关键字后面，它要是同步代码他就同步执行，就相当于状态已经为resolved的promise对象，他要是异步代码就等其状态发生了改变再去执行他下面的代码(变为resolved,
rejected)

第三种，利用Promise.try方法，塞到这代码块里面，同步代码同步执行，异步代码异步执行，除此之外还有个本事就是，它既可以捕获同步代码的错误，也可以捕获异步代码的错误，只需后面再加一个catch就可以对捕获的错误进行处理。

```

```
前面说了，async函数返回的promise对象的状态，要等里面所有await后面的promise对象都执行完成，才会发生改变。 而且只是状态发生改变，你不return，或者throw东西出来async函数返回的promise对象是没有结果的。然后就是还有个情况，就是如果你await关键字后面的promise对象的状态变为rejected了，也就相当于你throw东西出来了，为了解决这个情况，你可以try catch代码块包含await ...这句代码，或者在这句代码后面来个.catch抓一下错误。这样这句promise状态可能为rejected的后面的await还能接着执行。要不这样处理，你promise状态rejected直接结束这个async函数的执行，后续的代码也就都不执行了。
```

```
new Promise((resolve, reject) => {
    let i = 0;
    resolve(i + 1);
}).then(val => { console.log(val) })

new Promise((resolve, reject) => {
    let i = 0;
    resolve(setTimeout(() => { i + 2 }, 3000));
}).then(val => { console.log(val) })

resolve中传入的参数，或者表达式啥的会得到结果，会传递给then方法的回调函数的参数
你resolve中如果传递一个定时器，那then方法回调函数的参数会接收到一个定时器，而不是你定时器结束之后返回的结果
反正一般情况就是在定时器中去包含resolve/reject即过多久我在去触发promise的状态，从而执行相应then方法或者catch方法的回调函数，还很少有说resolve里面塞一个定时器的。
```

#### 138. 如何检测浏览器所支持的最小字体大小？

```
用 JS 设置 DOM 的字体为某一个值，然后再取出来，如果值设置成功，就说明支持。
```

#### 139. 怎么做 JS 代码 Error 统计？

```
error 统计使用浏览器的 window.error 事件。
```

#### 140. 单例模式模式是什么？

```
保证一个类仅有一个实例，并提供一个访问它的全局访问点。比如说常用的如弹框组件的实现和全局状态的实现。

```

#### 141. 策略模式是什么？

```
定义一系列的策略算法，把它们一个个封装起来，并使它们可以替换 核心是将算法的实现和算法的使用相分离

比如说年终奖，根据绩效等级是工资的不同倍数（根据不同参数可以命中不同的策略）
```

#### 142. 代理模式是什么？

```
 代理模式是为一个对象提供一个代用品或占位符，以便控制对它的访问。比如说加载图片、需要一段时间、这时候会产生空白、用户体验不好、我们可以用一张loading占位图片、等真正的图片加载下来之后，再将其通过图片元素的src属性显示出来.-
```

#### 143. 中介者模式是什么？

```
中介者模式指的是，多个对象通过一个中介者进行交流，而不是直接进行交流，中介者能够对通信的多个对象进行解耦。
```

#### 144. 适配器模式是什么？

```
适配器模式的作用就是解决两个软件实体间的接口不兼容的问题。适配器不需要改变已有的接口，通过包装一层的方式即可实现两个软件实体的正常协作。假如我们需要一种新的接口返回方式，但是老的接口由于在太多地方已经使用了，不能随意更改，这个时候就可以使用适配器模式。
```

更多关于设计模式的资料可以参考：
[《前端面试之道》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bdc74186fb9a049ab0d0b6b)
[《JavaScript 设计模式》](https://juejin.im/post/59df4f74f265da430f311909#heading-3)
[《JavaScript 中常见设计模式整理》](https://juejin.im/post/5afe6430518825428630bc4d)

常见的设计模式：

创建型：

工程模式、原型模式、单例模式

结构型：

适配器模式、代理模式

行为型：

策略模式、迭代器模式、观察者模式(发布订阅模式)、命令模式、状态模式

#### 145. 观察者模式和发布订阅模式有什么不同？

```
发布订阅模式其实属于广义上的观察者模式

在观察者模式中，观察者需要直接订阅目标事件。在目标发出内容改变的事件后，直接接收事件并作出响应。

而在发布订阅模式中，发布者和订阅者之间多了一个调度中心。调度中心一方面从发布者接收事件，另一方面向订阅者发布事件，订阅者需要在调度中心中订阅事件。通过调度中心实现了发布者和订阅者关系的解耦。使用发布订阅者模式更利于我们代码的可维护性。
```

详细资料可以参考：
[《观察者模式和发布订阅模式有什么不同？》](https://www.zhihu.com/question/23486749)

#### 146. Vue 的生命周期是什么？

```
Vue 的生命周期指的是组件从创建到销毁的一系列的过程。通过提供的 Vue 在生命周期各个阶段的钩子函数，我们可以很好的在 Vue 的各个生命阶段实现一些操作。
```

<img src="C:\Users\88520\Desktop\前端\3.面试\blog-master\img/lifecycle.png" style="zoom: 33%;" />

#### 147. Vue 的各个生命阶段是什么？

```
Vue 一共有8个生命阶段，分别是创建前、创建后、加载前、加载后、更新前、更新后、销毁前和销毁后，每个阶段对应了一个生命周期的钩子函数。

（1）beforeCreate 钩子函数，在实例初始化之后，在数据监听和事件配置之前触发。因此在这个事件中我们是获取不到 data 数据的。

（2）created 钩子函数，在实例创建完成后触发，此时可以访问 data、methods 等属性。但这个时候组件还没有被挂载到页面中去，所以这个时候访问不到 $el 属性。一般我们可以在这个函数中进行一些页面初始化的工作，比如通过 ajax 请求数据来对页面进行初始化。

（3）beforeMount 钩子函数，在组件被挂载到页面之前触发。在 beforeMount 之前，会找到对应的 template，并编译成 render 函数。

（4）mounted 钩子函数，在组件挂载到页面之后触发。此时可以通过 DOM API 获取到页面中的 DOM 元素。

（5）beforeUpdate 钩子函数，在响应式数据更新时触发，发生在虚拟 DOM 重新渲染和打补丁之前，这个时候我们可以对可能会被移除的元素做一些操作，比如移除事件监听器。

（6）updated 钩子函数，虚拟 DOM 重新渲染和打补丁之后调用。

（7）beforeDestroy 钩子函数，在实例销毁之前调用。一般在这一步我们可以销毁定时器、解绑全局事件等。

（8）destroyed 钩子函数，在实例销毁之后调用，调用后，Vue 实例中的所有东西都会解除绑定，所有的事件监听器会被移除，所有的子实例也会被销毁。

当我们使用 keep-alive 的时候，还有两个钩子函数，分别是 activated 和 deactivated 。用 keep-alive 包裹的组件在切换时不会进行销毁，而是缓存到内存中并执行 deactivated 钩子函数，命中缓存渲染后会执行 actived 钩子函数。
```

详细资料可以参考：
[《vue 生命周期深入》](https://juejin.im/entry/5aee8fbb518825671952308c)
[《Vue 实例》](https://cn.vuejs.org/v2/guide/instance.html)

#### 148. Vue 组件间的参数传递方式？

```
（1）父子组件间通信

第一种方法是子组件通过 props 属性来接受父组件的数据，然后父组件在子组件上注册监听事件，子组件通过 emit 触发事件来向父组件发送数据。

第二种是通过 ref 属性给子组件设置一个名字。父组件通过 $refs 组件名来获得子组件，子组件通过 $parent 获得父组件，这样也可以实现通信。

第三种是使用 provider/inject，在父组件中通过 provider 提供变量，在子组件中通过 inject 来将变量注入到组件中。不论子组件有多深，只要调用了 inject 那么就可以注入 provider 中的数据。

（2）兄弟组件间通信

第一种是使用 eventBus 的方法，它的本质是通过创建一个空的 Vue 实例来作为消息传递的对象，通信的组件引入这个实例，通信的组件通过在这个实例上监听和触发事件，来实现消息的传递。

第二种是通过 $parent.$refs 来获取到兄弟组件，也可以进行通信。

（3）任意组件之间

使用 eventBus ，其实就是创建一个事件中心，相当于中转站，可以用它来传递事件和接收事件。

如果业务逻辑复杂，很多组件之间需要同时处理一些公共的数据，这个时候采用上面这一些方法可能不利于项目的维护。这个时候
可以使用 vuex ，vuex 的思想就是将这一些公共的数据抽离出来，将它作为一个全局的变量来管理，然后其他组件就可以对这个公共数据进行读写操作，这样达到了解耦的目的。
```

详细资料可以参考：
[《VUE 组件之间数据传递全集》](https://juejin.im/entry/5ba215ac5188255c6d0d8345)

#### 149. computed 和 watch 的差异？

```
（1）computed 是计算一个新的属性，并将该属性挂载到 Vue 实例上，而 watch 是监听已经存在且已挂载到 Vue 实例上的数据，所以用 watch 同样可以监听 computed 计算属性的变化。

（2）computed 本质是一个惰性求值的观察者，具有缓存性，只有当依赖变化后，第一次访问 computed 属性，才会计算新的值。而 watch 则是当数据发生变化便会调用执行函数。

（3）从使用场景上说，computed 适用一个数据被多个数据影响，而 watch 适用一个数据影响多个数据。
```

详细资料可以参考：
[《做面试的不倒翁：浅谈 Vue 中 computed 实现原理》](https://juejin.im/post/5b98c4da6fb9a05d353c5fd7)
[《深入理解 Vue 的 watch 实现原理及其实现方式》](https://juejin.im/post/5af908ea5188254265399009)

#### 150. vue-router 中的导航钩子函数

```
Vue-router的导航守卫其作用就是用来监听路由的进入和离开，然后作相应的处理，通俗来讲主要用来作用是拦截导航，让他完成跳转或取消，比如在不同路由切换相应的不同组件时，进行title的修改。

（1）全局的钩子函数 beforeEach 和 afterEach

beforeEach 有三个参数，to 代表要进入的路由对象，from 代表离开的路由对象。next 是一个必须要执行的函数，如果不传参数，那就执行下一个钩子函数，如果传入 false，则终止跳转，如果传入一个路径，则导航到对应的路由，如果传入 error ，则导航终止，error 传入错误的监听函数。

（2）单个路由独享的钩子函数 beforeEnter，它是在路由配置上直接进行定义的。(只有进到某个路由里面才能使用的钩子函数，比如说我可以用beforeEnter监听一下，我什么时候进入到首页路由中)
 
（3）组件内的导航钩子主要有这三种：beforeRouteEnter、beforeRouteUpdate、beforeRouteLeave。它们是直接在路由组
件内部直接进行定义的。
```

详细资料可以参考：
[《导航守卫》](https://router.vuejs.org/zh/guide/advanced/navigation-guards.html#%E5%85%A8%E5%B1%80%E5%89%8D%E7%BD%AE%E5%AE%88%E5%8D%AB)

#### 151. $route$和router 的区别？

```
$route 是“路由信息对象”，包括 path，params，hash，query，fullPath，matched，name 等路由信息参数。而 $router 是“路由实例”对象包括了路由的跳转方法，钩子函数等。
```

#### 152. vue 常用的修饰符？

```
.prevent: 提交事件不再重载页面；.stop: 阻止单击事件冒泡；.self: 当事件发生在该元素本身而不是子元素的时候会触发；
```

#### 153. vue 中 key 值的作用？

```
vue 中 key 值的作用可以分为两种情况来考虑。

第一种情况是 v-if 中使用 key。由于 Vue 会尽可能高效地渲染元素，通常会复用已有元素而不是从头开始渲染。因此当我们使用 v-if 来实现元素切换的时候，如果切换前后含有相同类型的元素，那么这个元素就会被复用。如果是相同的 input 元素，那么切换前后用户的输入不会被清除掉，这样是不符合需求的。因此我们可以通过使用 key 来唯一的标识一个元素，这个情况下，使用 key 的元素不会被复用。这个时候 key 的作用是用来标识一个独立的元素。

第二种情况是 v-for 中使用 key。用 v-for 更新已渲染过的元素列表时，它默认使用“就地复用”的策略。如果数据项的顺序发生了改变，Vue 不会移动 DOM 元素来匹配数据项的顺序，而是简单复用此处的每个元素。因此通过为每个列表项提供一个 key 值，来以便 Vue 跟踪元素的身份，从而高效的实现复用。这个时候 key 的作用是为了高效的更新渲染虚拟 DOM。
```

详细资料可以参考：
[《Vue 面试中，经常会被问到的面试题 Vue 知识点整理》](https://segmentfault.com/a/1190000016344599)很重要！！！！！
[《Vue2.0 v-for 中 :key 到底有什么用？》](https://www.zhihu.com/question/61064119)
[《vue 中 key 的作用》](https://www.cnblogs.com/RainyBear/p/8563101.html)

#### 155. keep-alive 组件有什么作用？

```
如果你需要在组件切换的时候，保存一些组件的状态防止多次渲染，就可以使用 keep-alive 组件包裹需要保存的组件。
```

#### 156. vue 中 mixin 和 mixins 区别？

```
mixin 用于全局混入，会影响到每个组件实例，尽可能避免使用。

mixins 可以很方便的进行组件功能的复用或扩展，比如将多个组件中相同的业务逻辑，剥离出来，通过 mixins 混入代码进行功能代码的复用。
另外需要注意的是 mixins 混入的钩子函数会先于组件内的钩子函数执行，并且在遇到同名选项的时候也会有选择性的进行合并。

ES6:Mixin 指的是多个对象合成一个新的对象，新对象具有各个组成成员的接口。
```

详细资料可以参考：
[《前端面试之道》](https://juejin.im/book/5bdc715fe51d454e755f75ef/section/5bdc731b51882516c56ced6f)
[《混入》](https://cn.vuejs.org/v2/guide/mixins.html)

#### 补充Vue相关面试题：

**1.Vue中的nexttick：**

```
Vue的响应式采用的是异步更新，即Vue修改数据后，视图不会立即更新，而是等同一事件循环中的所有数据变化完成之后在统一进行视图更新。
反过来理解就是说，nexttick是一个异步任务，会在下一个Dom更新完成之后去执行回调函数。即数据发生变动，不可能立即读取到，只有当下一个Dom更新完成触发$nexttick,才能完整的从回调函数中拿取到了。
```

#### 157. 开发中常用的几种(POST)Content-Type ？

Content-Type 标头告诉客户端实际返回的内容的内容类型。

```
（1）application/x-www-form-urlencoded

浏览器的原生 form 表单，如果不设置 enctype 属性，那么最终就会以 application/x-www-form-urlencoded 方式提交数据。该种方式提交的数据放在 body 里面，数据按照 key1=val1&key2=val2 的方式进行编码，key 和 val 都进行了 URL转码。

（2）multipart/form-data

该种方式也是一个常见的 POST 提交方，通常表单上传文件时使用该种方式。

（3）application/json

告诉服务器消息主体是序列化后的 JSON 字符串。

（4）text/xml

该种方式主要用来提交 XML 格式的数据。
```

详细资料可以参考：
[《常用的几种 Content-Type》](https://honglu.me/2015/07/13/%E5%B8%B8%E7%94%A8%E7%9A%84%E5%87%A0%E7%A7%8DContent-Type/)

#### 158. 如何封装一个 javascript 的类型判断函数？

```js
function getType(value) {
  // 判断数据是 null 的情况
  if (value === null) {
    return value + "";
  }

  // 判断数据是引用类型的情况
  if (typeof value === "object") {
    let valueClass = Object.prototype.toString.call(value),
     // "[Object Array]"
     //  ['[Object','Array]']
     //  ['A','r','r','a','y',']']
     //  ['A','r','r','a','y']
     //	 'Array'
      type = valueClass.split(" ")[1].split("");

    type.pop();

    return type.join("").toLowerCase();
  } else {
    // 判断数据是基本数据类型的情况和函数的情况
    return typeof value;
  }
}
```

typeof 内置的构造函数类 Array、Function、Object这样的返回是function 因为这些构造函数本质势函数。

typeof 内置的构造函数类的实例  返回的是object 因为这些构造函数创建了对象。

详细资料可以参考：
[《JavaScript 专题之类型判断(上)》](https://github.com/mqyqingfeng/Blog/issues/28)

#### 159. 如何判断一个对象是否为空对象？

```js
function checkNullObj(obj) {
  return Object.keys(obj).length === 0 && Object.getOwnPropertySymbols(obj).length === 0;
}
```

详细资料可以参考：
[《js 判断一个 object 对象是否为空》](https://blog.csdn.net/FungLeo/article/details/78113661)

#### 160. 使用闭包实现每隔一秒打印 1,2,3,4

```js
// 使用闭包实现
for (var i = 0; i < 5; i++) {
  (function(i) {
    setTimeout(function() {
      console.log(i);
    }, i * 1000);
  })(i);
}

// 使用 let 块级作用域

for (let i = 0; i < 5; i++) {
  setTimeout(function() {
    console.log(i);
  }, i * 1000);
}
```

#### 161. 手写一个 jsonp

JSONP只适合get方式的跨域请求

```js
function jsonp(url, params, callback) {
  // 要访问的非同源服务器的url
  // 要向非同源服务器传递的params参数
  // 对非同源服务器传递回来参数进行处理的回调函数callback
  // 判断url是否含有参数，有的话直接&接着往下拼
  // 没有的话就先来个？往下拼接
  let queryString = url.indexOf("?") === "-1" ? "?" : "&";

  // url地址中拼接参数
  for (var k in params) {
    if (params.hasOwnProperty(k)) {
      queryString += k + "=" + params[k] + "&";
    }
  }

  // 处理回调函数名，
  // 将回调函数名，放入url地址中，让服务器知道传个什么函数调用回来，客户端就能跨域拿到数据了
  // 此外向非同源服务器传递回调函数名，不能每次都一样，
  // 是对JSONP的一种优化，则引入随机数
  let random = Math.random()
      .toString()
      .replace(".", ""),
    callbackName = "myJsonp" + random;

  // 添加回调函数
  queryString += "callback=" + callbackName;

  // 通过script标签的src属性发起跨域请求
  // 则操作dom新建script标签即可
  let scriptNode = document.createElement("script");
  scriptNode.src = url + queryString;

  // 在真正利用script标签的src属性发起跨域请求之前，
  // 要先声明跨域服务器传递回来的函数调用的函数
  // 全局函数就是顶层对象的属性
  window[callbackName] = function() {
    // 调用回调函数，用回调函数处理跨域服务器出传递回来的实参
    callback(...arguments);

    // 删除处理好的script标签就是断开跨域请求
      document.body.removeChild(scriptNode);
  };
  // 建立处理好的script标签就是发起跨域请求
  // 发起请求
  document.body.appendChild(scriptNode);
}

//使用范例
jsonp("www.jd.com",{num:10},function(){
  console.log(para);
})
```

详细资料可以参考：
[《原生 jsonp 具体实现》](https://www.cnblogs.com/zzc5464/p/jsonp.html)
[《jsonp 的原理与实现》](https://segmentfault.com/a/1190000007665361#articleHeader1)

#### 162. 手写一个观察者模式？

```js
var events = (function() {
  var topics = {};

  return {
    // 注册监听函数
    subscribe: function(topic, handler) {
      if (!topics.hasOwnProperty(topic)) {
        topics[topic] = [];
      }
      topics[topic].push(handler);
    },

    // 发布事件，触发观察者回调事件
    publish: function(topic, info) {
      if (topics.hasOwnProperty(topic)) {
        topics[topic].forEach(function(handler) {
          handler(info);
        });
      }
    },

    // 移除主题的一个观察者的回调事件
    remove: function(topic, handler) {
      if (!topics.hasOwnProperty(topic)) return;

      var handlerIndex = -1;
      topics[topic].forEach(function(item, index) {
        if (item === handler) {
          handlerIndex = index;
        }
      });

      if (handlerIndex >= 0) {
        topics[topic].splice(handlerIndex, 1);
      }
    },

    // 移除主题的所有观察者的回调事件
    removeAll: function(topic) {
      if (topics.hasOwnProperty(topic)) {
        topics[topic] = [];
      }
    }
  };
})();

//主题监听函数
var handler = function(info) {
    console.log(info);
}
//订阅hello主题
events.subscribe('hello', handler);

//发布hello主题
events.publish('hello', 'hello world');
```

详细资料可以参考：
[《JS 事件模型》](https://segmentfault.com/a/1190000006934031#articleHeader1)

#### ####163. EventEmitter 实现(发布订阅模式)

```js
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(event, callback) {
    let callbacks = this.events[event] || [];
    callbacks.push(callback);
    this.events[event] = callbacks;

    return this;
  }

  off(event, callback) {
    let callbacks = this.events[event];
    this.events[event] = callbacks && callbacks.filter(fn => fn !== callback);

    return this;
  }

  emit(event, ...args) {
    let callbacks = this.events[event];
    callbacks.forEach(fn => {
      fn(...args);
    });

    return this;
  }

  once(event, callback) {
    let wrapFun = function(...args) {
      callback(...args);

      this.off(event, wrapFun);
    };
    this.on(event, wrapFun);

    return this;
  }
}
```

#### 164. 一道常被人轻视的前端 JS 面试题

```js
// 下述代码的执行过程：
// 创建全局执行上下文，这里主要是预解析中的变量提升，然后将全局上下文压入执行栈加以执行，即执行上下文的执行
// 全局执行上下文按照代码出现的顺序依次向下执行，变量赋值、函数引用等。
// 执行到函数调用时，创建相应的函数执行上下文，压入栈中执行，执行完之后弹出

function Foo() {
  // 这里不是实例的方法，只是构造函数内部又塞了个函数(内嵌函数),只是赋值操作没其他意思
  // 如果想写成实例自身的方法，则要写成：
  // this. getName = function() {  alert(1)  };
  getName = function() {
    alert(1);
  };
  return this;
}
// 同上Foo的静态方法
Foo.getName = function() {
  alert(2);
};
// 实例的getName方法真正来自与其原型对象
Foo.prototype.getName = function() {
  alert(3);
};
var getName = function() {
  alert(4);
};
function getName() {
  alert(5);
}

//请写出以下输出结果：
Foo.getName(); 
getName(); 
Foo().getName(); //这里只是修改了全局的getName方法
getName(); 
new Foo.getName();// 而对于Foo作为类的静态方法仍然没变
new Foo().getName(); 
new new Foo().getName(); 

```

详细资料可以参考：
[《前端程序员经常忽视的一个 JavaScript 面试题》](https://github.com/Wscats/Good-text-Share/issues/85)
[《一道考察运算符优先级的 JavaScript 面试题》](https://segmentfault.com/q/1010000008430170)
[《一道常被人轻视的前端 JS 面试题》](https://www.cnblogs.com/xxcanghai/p/5189353.html)

//2 4 1 1 2 3 3

#### 165. 如何确定页面的可用性时间，什么是 Performance API？

```
Performance API 用于精确度量、控制、增强浏览器的性能表现。这个 API 为测量网站性能，提供以前没有办法做到的精度。

使用 getTime 来计算脚本耗时的缺点，首先，getTime方法（以及 Date 对象的其他方法）都只能精确到毫秒级别（一秒的千分之一），想要得到更小的时间差别就无能为力了。其次，这种写法只能获取代码运行过程中的时间进度，无法知道一些后台事件的时间进度，比如浏览器用了多少时间从服务器加载网页。

为了解决这两个不足之处，ECMAScript 5引入“高精度时间戳”这个 API，部署在 performance 对象上。它的精度可以达到1毫秒
的千分之一（1秒的百万分之一）。

navigationStart：当前浏览器窗口的前一个网页关闭，发生 unload 事件时的 Unix 毫秒时间戳。如果没有前一个网页，则等于 fetchStart 属性。

loadEventEnd：返回当前网页 load 事件的回调函数运行结束时的 Unix 毫秒时间戳。如果该事件还没有发生，返回 0。
```

根据上面这些属性，可以计算出网页加载各个阶段的耗时。比如，网页加载整个过程的耗时的计算方法如下：

```js
var t = performance.timing;
var pageLoadTime = t.loadEventEnd - t.navigationStart;
```

详细资料可以参考：
[《Performance API》](http://javascript.ruanyifeng.com/bom/performance.html)

#### 166. js 中的命名规则

```
（1）第一个字符必须是字母、下划线（_）或美元符号（$）
（2）余下的字符可以是下划线、美元符号或任何字母或数字字符
一般我们推荐使用驼峰法来对变量名进行命名，因为这样可以与 ECMAScript 内置的函数和对象命名格式保持一致。
```

详细资料可以参考：
[《ECMAScript 变量》](http://www.w3school.com.cn/js/pro_js_variables.asp)

#### 167. js 语句末尾分号是否可以省略？

```
在 ECMAScript 规范中，语句结尾的分号并不是必需的。但是我们一般最好不要省略分号，因为加上分号一方面有
利于我们代码的可维护性，另一方面也可以避免我们在对代码进行压缩时出现错误。
```

#### 168. Object.assign()

```
Object.assign() 方法用于将所有可枚举属性的值从一个或多个源对象复制到目标对象。它将返回目标对象。
```

#### 169. Math.ceil 和 Math.floor

```
Math.ceil() === 向上取整，函数返回一个大于或等于给定数字的最小整数。

Math.floor() === 向下取整，函数返回一个小于或等于给定数字的最大整数。
```

#### 170. js for 循环注意点

```js
for (var i = 0, j = 0; i < 5, j < 9; i++, j++) {
  console.log(i, j);
}

// 当判断语句含有多个语句时，以最后一个判断语句的值为准，因此上面的代码会执行 10 次。
// 当判断语句为空时，循环会一直进行。
```

#### 171. 一个列表，假设有 100000 个数据，这个该怎么办？

```
我们需要思考的问题：该处理是否必须同步完成？数据是否必须按顺序完成？

解决办法：

（1）将数据分页，利用分页的原理，每次服务器端只返回一定数目的数据，浏览器每次只对一部分进行加载。

（2）使用懒加载的方法，每次加载一部分数据，其余数据当需要使用时再去加载。

（3）使用数组分块技术，基本思路是为要处理的项目创建一个队列，然后设置定时器每过一段时间取出一部分数据，然后再使用定时器取出下一个要处理的项目进行处理，接着再设置另一个定时器。

Element-ui的分页组件
```

#### 172. js 中倒计时的纠偏实现？

```
在前端实现中我们一般通过 setTimeout 和 setInterval 方法来实现一个倒计时效果。但是使用这些方法会存在时间偏差的问题，这是由于 js 的程序执行机制造成的，setTimeout 和 setInterval 的作用是隔一段时间将回调事件加入到事件队列中，因此事件并不是立即执行的，它会等到当前执行栈为空的时候再取出事件执行，因此事件等待执行的时间就是造成误差的原因。

一般解决倒计时中的误差的有这样两种办法：

（1）第一种是通过前端定时向服务器发送请求获取最新的时间差，以此来校准倒计时时间。

（2）第二种方法是前端根据偏差时间来自动调整间隔时间的方式来实现的。这一种方式首先是以 setTimeout 递归的方式来实现倒计时，然后通过一个变量来记录已经倒计时的秒数。每一次函数调用的时候，首先将变量加一，然后根据这个变量和每次的间隔时间，我们就可以计算出此时无偏差时应该显示的时间。然后将当前的真实时间与这个时间相减，这样我们就可以得到时间的偏差大小，因此我们在设置下一个定时器的间隔大小的时候，我们就从间隔时间中减去这个偏差大小，以此来实现由于程序执行所造成的时间误差的纠正。

   当前执行倒计时的时间与实际应执行时间的偏差
   const offset = new Date().getTime() - (startTime + count * interval) // A  
   在下一次进行倒计时的基础上去掉偏差值
   let nextTime = interval - offset
```

详细资料可以参考：
[《JavaScript 前端倒计时纠偏实现》](https://juejin.im/post/5badf8305188255c8e728adc)

#### 173. 进程间通信的方式？

- 1.管道通信
- 2.消息队列通信
- 3.信号量通信
- 4.信号通信
- 5.共享内存通信
- 6.套接字通信

详细资料可以参考：
[《进程间 8 种通信方式详解》](https://blog.csdn.net/violet_echo_0908/article/details/51201278)
[《进程与线程的一个简单解释》](http://www.ruanyifeng.com/blog/2013/04/processes_and_threads.html)

计算机的核心是CPU，它承担了所有的计算任务。它就像一座工厂，时刻在运行。

假定工厂的电力有限，一次只能供给一个车间使用。也就是说，一个车间开工的时候，其他车间都必须停工。

进程就好比工厂的车间，它代表CPU所能处理的单个任务，背后的含义就是，单个CPU一次只能运行一个任务。

线程就好比车间里的工人，一个进程可以包括多个线程，他们协同完成一个任务。

车间的空间是工人们共享的，比如许多房间是每个工人都可以进出的。

这象征一个进程的内存空间是共享的，每个线程都可以使用这些共享内存。

先到先使用，就有了锁的概念。

一个CPU执行一个进程，一个进程里面包含多个线程，实际上是串行执行多个线程的，但是由于执行的太快，感觉像是并行执行的

多核处理器，多个cpu同时处理多个进程，同时并行的处理多个串行的线程，真正的高并发

进程是cpu用于资源分配的最小单位，线程是所能调度资源的最小单位。

#### 174. 如何查找一篇英文文章中出现频率最高的单词？

```js
function findMostWord(article) {
  // 合法性判断
  if (!article) return;
  // 参数处理
  article = article.trim().toLowerCase();
  let wordList = article.match(/[a-z]+/g),
    visited = [],
    maxNum = 0,
    maxWord = "";
  article = " " + wordList.join("  ") + " ";
  // 遍历判断单词出现次数
  wordList.forEach(function(item) {
    if (visited.indexOf(item) < 0) {

      // 加入 visited 
      visited.push(item);

      let word = new RegExp(" " + item + " ", "g"),
        num = article.match(word).length;

      if (num > maxNum) {
        maxNum = num;
        maxWord = item;
      }
    }
  });
  return maxWord + "  " + maxNum;
}
```

技术栈：IT术语，某项工作或某个职位需要掌握的一系列技能组合的统称。

#### 175.Vue3.0六大亮点：

Performance：性能比Vue 2.x快1.2~2倍

Tree shaking support：按需编译,体积比Vue2.x更小

Composition API: 组合API(类似React Hooks)(解决了vue2.x中数据和业务逻辑分散的问题)

Better TypeScript support：更好的 Ts 支持

Custom Renderer API：暴露了自定义渲染API

Fragment, Teleport(Protal), Suspense：更先进的组件

#### 176.跨端开发

**移动端开发的方案：**

```
比如native（IOS和Android）、 hybrid和react native等。
其中hybrid、react native等方案对前端很友好，毕竟是用我们熟悉的JavaScript开发，但JavaScript无法直接调用native本身提供的能力，比如获取相册信息。
所以就需要通过一种方式将native能力提供给JavaScript，同时native也可能需要调用JavaScript的一些功能，
```

**！！而JSBridge就是JavaScript和native之间的桥梁，提供两者相互调用的能力。**

![](https://gitee.com/chenyipeng9/blog/raw/master/img/v2-85832215bfabdb0ed32bdecac8dd3e2c_r.jpg)

```
Hybrid App主要以JS+Native两者相互调用为主，从开发层面实现“一次开发，多处运行”的机制，成为真正适合跨平台的开发。Hybrid App兼具了Native App良好用户体验的优势，也兼具了Web App使用HTML5跨平台开发低成本的优势。
```

```
Android需要非常熟练的掌握WebView、WebSettings、WebChromeClient、WebClient四大对象。
iOS需要非常熟练掌握UIWebView对象。
```

#### 移动应用开发的三种方式：

- Native App： 本地应用程序（原生App）

- Web App：网页应用程序（移动web）

- Hybrid App：混合应用程序（混合App）

  ![](https://gitee.com/chenyipeng9/blog/raw/master/img/Snipaste_2021-08-05_12-22-52.png)

```
Hybrid App它综合了Web App的开发速度和Native App的高性能体验。
之所以说学习成本高，是因为开发高性能的Hybrid App有难度
```

```
uni-app（uni，读you ni，是统一的意思）是一个使用Vue.js开发所有前端应用的框架，开发者编写一套代码，可发布到iOS、Android、Web（响应式）、以及各种小程序、快应用等多个平台。
```

#### 一帧所做的事情

## **进阶-浏览器-渲染机制-仔细看**

```
当 Event loop 执行完 Microtasks 后，会判断 document 是否需要更新。因为浏览器是 60Hz的刷新率，每 16ms才会更新一次。
然后判断是否有 resize 或者 scroll ，有的话会去触发事件，所以 resize 和 scroll 事件也是至少 16ms 才会触发一次，并且自带节流功能。
判断是否触发了media query
更新动画并且发送事件
判断是否有全屏操作事件
执行 requestAnimationFrame 回调
执行 IntersectionObserver 回调，该方法用于判断元素是否可见，可以用于懒加载上，但是兼容性不好
更新界面
以上就是一帧中可能会做的事情。如果在一帧中有空闲时间，就会去执行 requestIdleCallback 回调
```

####  CRP,即关键渲染路径

#### 1.渲染是在宏任务完成之后还是微任务完成之后

```
 Call Stack清空
 执行当前的微任务
 尝试DOM渲染
 触发Event Loop
```

1. 微任务：DOM渲染前执行，微任务是ES6语法规定

2. 宏任务：DOM渲染后触发，由浏览器规定（Web APIs）

   

   ```
   Vue渲染过程：
   1.  函数,生成 render 函数字符串 ,编译过程如下:
   
      - parse 使用大量的正则表达式对template字符串进行解析，将标签、指令、属性等转化为抽象语法树AST。`模板 -> AST （最消耗性能）`
      - optimize 遍历AST，找到其中的一些静态节点并进行标记，方便在页面重渲染的时候进行diff比较时，直接跳过这一些静态节点，`优化runtime的性能`
      - generate 将最终的AST转化为render函数字符串
   
      - 调用 `new Watcher` 函数,监听数据的变化,当数据发生变化时，Render 函数执行生成 vnode 对象
      - 调用 `patch` 方法,对比新旧 vnode 对象,通过 DOM diff 算法,添加、修改、删除真正的 DOM 元素
   
   
   ```

   ```
   开启GPU加速的方法
   
   开启后，会将 dom元素提升为独立的渲染层，它的变化不会再影响文档流中的布局。
   
   transform: translateZ(0)
   opacity
   filters
   Will-change
   ```

   

![](C:\Users\88520\Desktop\前端\3.面试\blog-master\img/Snipaste_2021-09-12_21-20-59.png)

#### 4.对前端工程化的理解

前端工程化就是为了让前端开发能够“自成体系”，个人认为主要应该从**模块化**、**组件化**、**规范化**、**自动化**四个方面思考。

**模块化：**将一个大文件拆分成相互依赖的小文件，再进行统一的拼装和加载。(**WebPack**)

**组件化：**模块化只是在文件层面上，对代码或资源的拆分；而组件化是在设计层面上，对UI（用户界面）的拆分。

**规范化：**规范制定的好坏会直接影响到后期的开发质量。

**自动化：**任何简单机械的重复劳动都应该让机器去完成。