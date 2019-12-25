# 01Javascript 初体验

### 1 页面内容输出

#### 1.1 在网页中弹出显示框，显示信息

```xml
  <script>
        alert("Hello，JavaScript！"); 
  </script>
```

#### 1.2 在控制台输出消息，一般用来调试程序

```xml
   <script>
         console.log("Hello，JavaScript！"); 
         console.warn("警告输出！"); 
         console.error("错误输出！"); 
   </script>
```

#### 1.3 在网页中弹出输入框，一般用于接收用户输入的信息

```xml
  <script>
        prompt("Hello，JavaScript！"); 
  </script>
```

#### 1.4 在网页中弹出提示框，显示信息，该方法一般与if判断语句结合使用

```xml
 <script>
       comfirm("Hello，JavaScript！"); 
 </script>
```

注意事项

- 编写Javascript注意语法规范，一行代码结束后必须在代码最后加上;如果不写分号，浏览器会自动添加，但是会消耗一些系统资源；此外，容易加错分号，所以在开发中分号必须要写。

- 在JavaScript中是严格区分大小写的

```cpp
   comfirm("Hello，JavaScript！");   // 正确
   COMFIRM("Hello，JavaScript！");   // 错误 
```

- JavaScript中会忽略多个空格和换行

```cpp
 console.log
 (
     "Hello，JavaScript！"
 );  
```

### 2  JavaScript注释语法 

#### 2.1 什么是注释？

- 注释是就是注解、解释的意思； 在JavaScript中它可以用来解释某一段程序或者某一行代码是什么意思，方便开发者之间的交流；
- 注释可以是任何文字，包括中文、英文和各种字符；
- 在开发工具中注释一般是灰色或者绿色

#### 2.2 为什么要写注释？

- 方便自己，方便他人（便于检查代码，排除错误）

#### 2.3 如何写注释？

- 单行注释

  ```csharp
     // 单行注释
     var name;
  ```

  > 使用范围:任何地方都可以写注释：函数外面、里面，每一条语句后面
  >  作用范围: 从第二个斜线到这一行末尾
  >  快捷键:Ctrl+/

- 多行注释

  ```csharp
     /*多行注释*/
     var name;
  ```

  > 使用范围:任何地方都可以写注释：函数外面、里面，每一条语句后面
  >  作用范围: 从第一个/*到最近的一个*/ 之间

#### 2.4 注释使用注意

- 单行注释可以嵌套单行注释、多行注释
   // 北京
   // 北京 // 南京
   // /* 北京 */
- 多行注释可以嵌套单行注释
   /*
   // author：jack
   // intro：It's good
   */
- 多行注释不能嵌套多行注释

