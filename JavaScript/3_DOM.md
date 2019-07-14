### DOM (Document Operation Model)

---

#### 1. DOM 操作 之 查

* 提供 *对文档中各节点元素 的 增删改查* 功能！

  - 使用 **内置方法-选择器**： `document` 代表 整个文档
    - document.getElementById(): id 字段在很多大型网站中已经被作为保留字类似的东西 保留了，一般也不建议使用
    - **document.getElementsByTagName()**: 适用性最好
    - **document.getElementsByClassName()**: ie8 及 ie8以下 浏览器不支持
    - document.getElementsByName()
    - document.querySelector() // css 选择器（因为是非实时静态选择器，所以不建议使用）
    - document.querySelectorAll() 
  - 遍历 **元素节点树**
    - parentElement
    - children
    - node.childElementCount
    - firstElementChild / lastElementChild
    - nextElementSibling / previousElementSibling
  - **遍历节点树** 选择节点
    - parentNode (父节点)
    - childNodes (子节点列表, 包含文本节点-注释节点-属性节点-元素节点 等)
    - firstChild
    - lastChild
    - nextSibling (previousSibling)
* 节点的四个属性
  1. nodeName : 元素 标签名
  2. nodeType : 节点的类型
  3. attributes ：所有 Element节点 的属性集合
  4. node.hasChildNodes() 判断节点是否有子节点
  5. nodeValue : 元素 内容

#### 2. DOM 操作 之 增删改

* 增
  1. <u>document.createElement('div')</u>, div.innerHTML = 123;
  2. parentnode.**appendChild()**  // 剪切式插入
  3. parentnode.insertBefore(a, b) // insert a before b
  4. document.createTextNode() / createComment() / createDocumentFragment()
* 删
  1. parent.<u>removeChild</u>()
  2. <u>child.remove</u>()
* 改 (替换)
  1. parentNode.replaceChild(new, old) // 用 new元素 替换 old元素

----

#### 3. DOM 元素 属性及方法

* **innerHTML**：用于 获取/改变 某个元素节点里面的html内容
* innerText / textContent
* element**.setAttribute() / getAttribute()** ，可以 获取/设置 某个元素节点内的**属性值**

-----

#### 4. 可用来做的效果 举例

* 用 DOM 实现 选项卡功能（根据点击为按钮动态添加 active属性， 同时显示内容）

  ![image-20190713122404716](/images/image-20190713122404716.png)
  
  （注意：用 立即执行函数 传递参数 处理闭包问题）
  
* 用 DOM 实现 方块运动

  ![image-20190713123036477](/images/image-20190713123036477.png)

  * **setInterval(func, 100)** 函数：每隔 100ms 会一次执行func，实现动态移动的目的！

  ![image-20190713123929779](/images/image-20190713123929779.png)

  * 使用 js 监听键盘事件 实现 “用键盘控制小方块的运行方向 (上下左右移动)”