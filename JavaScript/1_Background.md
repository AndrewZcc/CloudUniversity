### JavaScript 前端开发语言

---

1. JS 是 解释型 语言

2. JS 三大部分：ECMAScript, DOM (Document), BOM (Browser)

3. Web 开发过程中注意：**”结构(html) - 行为(js) - 样式(css)“ 相互分离**！

   Web 开发企业级标准：**HJC 分离**，不要混到一起，好处在于：结构清晰 且 便于后期维护！

---

编辑器推荐：

* Sublime3 + PackageControl (插件 Emmet && JsPrettify )
  * PackageControl 在线安装方法 [here](https://packagecontrol.io/installation)
  * Emmet 自动补齐代码
  * JsPrettify 自动格式化代码 (包括 html / css / js 代码)

----

1. 基本语法： 

  ```js
  <script type="text/javascript">
    # 定义变量
    var a;
  
    # 打印
    document.write('hello-world.')
  
  	----
  	# 数组中添加元素的方法 (push)
    var arr = [1];
  	arr.push(2);
  </script>
  ```

2. 堆和栈的区别

   ![image-20190707224515935](/images/image-20190707224515935.png)

   - 引用型的值：数据存放在堆内存中，而在栈内存中存的是仅仅是指向堆内存的地址！