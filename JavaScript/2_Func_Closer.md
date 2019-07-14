### Javascript 函数 及 闭包 

#### 1. 函数定义 三种方式

* 直接声明函数

  ```js
  function func() {
    statement;
  }
  ```

* 函数表达式 (匿名函数表达式/显式函数表达式)

  ```js
  var func = function (){
    statement; 
  }
  ```

* 立即执行函数 (全局只执行一次 执行完就销毁)

  ```js
  var ret = (function () {
    statement;
  return ret;
  }())
  ```
  
------

#### 2. 闭包（怎么解耦？）

- 采用 立即执行函数（将共享内存 拷贝成 N份，变成非共享，从而解耦闭包）

  ```js
  function test() {
    var liCollection = document.getElementsByTagName('li');
    
    for (var i=0; i<liCollection.length; i++) {
      ( function (j) { # 每次执行 形参都相当于是实参的一份拷贝，从而实现了解耦
        liCollection[j].onClick = function (){
          console.log(j)
        }
      }(i) ) # 使用 立即执行函数，将 i 作为实参传递给形参
    }
  }
  
  test()
  ```

  