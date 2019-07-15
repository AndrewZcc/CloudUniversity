### DOM 方式操纵 CSS

---

1. 读写 css 属性

   ```js
   dom.style.width ...
   ---
   dom.style.properties
   
   特殊场景
   1. 特殊字符：font-family --> fontFamily
   2. 保留字：float --> cssFloat
   ```

2. 查询 样式

   window.*getComputedStyle(div, null)* # 第二个参数 null 其实代表的是: 选取某个元素的 伪元素

   div.currentStyle() # IE 浏览器独有

   ```js
   function getCssStyle(elem, prop) {
     if (window.getComputedStyle) {
       return window.getComputedStyle(elem, null)[prop];
     } else {
       return elem.currentStyle[prop]; # 为了适配 IE
     }
   }
   ```


3. 为 **选项卡** 添加 class 属性

   ```js
   div.onclick = function () {
   	div.className = "active";
   }
   ```

   