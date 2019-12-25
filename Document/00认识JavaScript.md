# 00认识JavaScript

### 1 编程语言

- 编程语言是人和计算机交流的工具，工程师通过编程语言基于计算机去开发一款款软件

- 编程语言就是一门语言，只不过语法比较特殊，我们得学习之后才能用这门语言来开发相应的东西

- 编程语言大致可以分为以下几类： 机器语言、汇编语言、高级语言 

  ```
    机器语言    000000101 000000010  000000000
    汇编语言    MOV AX, 1 ADD AX, 1
    高级语言    int  a = 10
  ```

- JavaScript就是一门编程语言，属于高级语言

### 2 JavaScript的诞生

> 1994 年，网景公司（NetScape）发布了Navigator浏览器0.9版， 这是历史上第一个比较成熟的浏览器，引起了广泛关注。但是，这个版本的浏览器只能用来浏览，不具备与访问者互动的能力。。。。网景公司急需要一门网页脚本语言，使得浏览器可以与网页进行互动。

- 1995年5月，网景公司做出决策，未来的网页脚本语言必须"看上去与Java足够相似"，但是比Java简单，使得非专业的网页作者也能很快上手。

- 1995年4月，网景公司录用了34岁的系统程序员Brendan Eich, 他只用10天时间就把Javascript设计出来。

### 3 JavaScript语言的前世今生

- 1995.2月 Netscape公司发布LiveScript，后临时改为JavaScript，为了蹭上Java的热浪。

- 欧洲计算机制造商协会（ECMA）英文名称是European Computer Manufacturers Association

- 1997 年，以JavaScript 1.1 为基础。由来自 Netscape、Sun、微软、Borland 和其他一些对脚本编程感兴趣的公司的程序员组成的 TC39（ECMA的小组） 锤炼出了 ECMA-262，也就是ECMAScript1.0。

- 1998年6月，ECMAScript 2.0版发布。

- 1999年12月，ECMAScript 3.0版发布，成为JavaScript的通行标准，得到了广泛支持。

- 2007年10月，ECMAScript 4.0版草案发布：分歧太大，失败告终。

- 2009年12月，ECMAScript 5.0版正式发布

- 2015年6月17日，ECMAScript 6发布正式版本，即ECMAScript 2015。

- ...

### 4 JavaScript来源于借鉴

- 借鉴C语言的基本语法；
- 借鉴Java语言的数据类型和内存管理；
- 借鉴Scheme语言，将函数提升到"第一等公民"（first class）的地位；
- 借鉴Self语言，使用基于原型（prototype）的继承机制。

### 5 什么是JavaScript?

- JavaScript是一种脚本语言，其源代码在发往客户端运行之前不需经过编译，而是将文本格式的字符代码发送给浏览器由浏览器解释运行。

> 解释型语言：程序执行之前，不需要编译，直接运行时边解析边执行的语言
> 编译型语言：程序执行之前，需要一个专门的编译过程，把程序编译成为机器语言的文件，比如exe文件

- 简单易用
   可以使用任何文本编辑工具编写
   只需要浏览器就可以执行程序
- 解释执行（解释语言）
   事先不编译
   逐行执行
   无需进行严格的变量声明
- 基于对象
   内置大量现成对象，编写少量程序可以完成目标

### 6 JavaScript的组成

- ECMAScript：JavaScript的语法标准 
  - ECMA是一个组织，即欧洲计算机制造商协会
  - ECMAScript是ECMA制定的脚本语言的标准, 规定了一种脚本语言实现应该包含的基本内容
  - JavaScript是脚本语言的一种,所以JavaScript也必须遵守ECMAScript标准,包含ECMAScript标准中规定的基本内容
- DOM：JavaScript操作网页上的元素的API
- BOM：JavaScript操作浏览器的部分功能的API

 ![img](https://upload-images.jianshu.io/upload_images/1268909-cc41e66df57d083b.png?imageMogr2/auto-orient/strip|imageView2/2/w/555/format/webp) 



### 7 JavaScript的使用场景

随着JavaScript这门语言的完善，我们可以用它来进行前端开发、后端开发和移动端开发。当然，学习这门语言最开始的突破口在于前端开发。我们一起看看在前端领域它能做什么吧！ 

- 客户端数据计算
- 客户端表单合法性验证
- 浏览器对象的调用
- 浏览器事件的触发
- 网页特殊显示效果制作
- ....

### 8 JavaScript和HTML、CSS的关系

- Html：是用来制作网页，简单来说就是编写网页结构
- CSS： 美化网页（样式）
- Javascript:   实现网页与客户之间互动的桥梁，让网页具有丰富的生命力

### 9 JavaScript的语法规范

JavaScript有三种书写格式, 分别是"行内式"、"页内式"、"外链式" 

#### 9.1 行内式

```xml
 <button onclick="alert('今天天气很好！');">今天天气很好！</button>
```

####  9.2 页内式

```xml
 </body>
      ......
     <script type="text/javascript">
        alert("今天天气很好！");
     </script>
 </body>
```

- 页内式注意点 
  - <script></script>标签中的js代码一半写在文档的尾部；
  - 网页是从上至下加载, 而js代码通常是给标签添加交互(操作元素), 所以需要先加载HTML, 否则如果执行js代码时HTML还未被加载, 那么js代码将无法添加交互(操作元素);
  - HTML页面中出现<script>标签后，就会让页面暂停等待脚本的解析和执行。无论当前脚本是内嵌式还是外链式，页面的下载和渲染都必须停下来等待脚本的执行完成才能继续。所以如果把js代码如果写在head中, 那么js代码执行完毕之前后续网页无法被加载。

#### 9.3 外链式格式

```xml
 <script type="text/javascript" src="01-js书写格式.js"></script>
```

- 外链式注意点
   外链式的script代码块中不能编写js代码, 即便写了也不会执行

```xml
      <script type="text/javascript" src="index.js">
            alert("今天天气很好！"); // 不会被执行
       </script>
```

- 由于每次加载外链式的js文件都会发送一次请求, 这样非常消耗性能, 所以在企业开发中推荐将多个JS文件打包成为一个JS文件,以提升网页的性能和加载速度。