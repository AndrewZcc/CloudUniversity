#### 1. DOM 继承树 与 DOM 基本操作

-----

```
Node
|-- Document
			|-- HTMLDocument -- document
			|-- XMLDocument
|-- Element
			|-- HTMLElement
							|-- HTMLHeadElement
							|-- HTMLBodyElement ...
```

注意：

1. document.getElementsByTagName('div')[0] 该方法是定义在 Document 和 Element 上的，所以本质上页面中的 document 以及 element 都能使用该方法！

   ```js
   var div = document.getElementsByTagName('div')[0];
   var span = div.getElementsByTagName('span')[0];
   ```

2. HTMLDocument 类上已经预置了三个常用属性：body, head, documentElement。

-----

#### 2. Date 对象 与 定时器 setInterval

主要用途：

1. 记录 执行时刻 的时间信息 date = new Date()
2. 可以计算时间戳 date.getTime()，用于计算时间差
3. 设置一个未来的时间，用于实现 ‘秒杀’功能！

举例：

```js
date.setMinutes(22)

setInterval(function () {
  if (new Date().getTime() - date.getTime() > 1000 ) {
    clock.start(); (闹钟可运行)
  }
}, 1000);

备注：setInterval(func, 1000) 代表 每隔1000ms会执行一次 func!
  从而实现定时监控的目的！
```

* 注意：定时器 setInterval 是不准的！

---

#### 3. 定时器功能

1. 创建 定时器

   ```js
   var timer = setInterval(function(){
     TODO...
   }, 1000);
   ```

2. 清除 定时器

   ```js
   clearInterval(timer);
   ```

3. 推迟器 var timer = setTimeout(function(){}, 1000);

4. 清除 推迟器 clearTimeout(timer);

举例：实现一个计时器

![image-20190715213335705](/images/image-20190715213335705.png)