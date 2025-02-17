## **<font style="color:rgb(25, 27, 31);">前言</font>**
<font style="color:rgb(25, 27, 31);">一边学习，一边记录，前前后后花了至少2个月的时间，算是把TS大部分都搞明白了。</font>

<font style="color:rgb(25, 27, 31);">这篇文章的篇幅有点长，是我本人学习过程中的一些记录，参考了很多优秀博主的一些文章，以及在B站看了一些TS的视频，把几乎所有TS涵盖到的基础知识点都总结了下来，所以，对于想学习TS的小伙伴下来，一定一定要认认真真把这篇文章看完。</font>

**<font style="color:rgb(25, 27, 31);">8万多字的教程，不敢说是全网最好，但可以说是全网最详细。</font>**

<font style="color:rgb(25, 27, 31);">对于新手入门来说是一篇非常不错的宝藏文章，几乎每个 TypeScript 的知识点都有详细的讲到，并且附上一些简单的示例，通俗易懂，希望可以给想学习 TS 的小伙伴带来动力！</font>

## **<font style="color:rgb(25, 27, 31);">一、了解TypeScript</font>**
## **<font style="color:rgb(25, 27, 31);">1. 什么是TypeScript</font>**
+ <font style="color:rgb(25, 27, 31);">TypeScript是由微软开发的一门开源的编程语言。</font>
+ <font style="color:rgb(25, 27, 31);">TypeScript，简称TS，是JavaScript的超集（以JavaScript为基础构建的语言，JS有的TS都有）。</font>
+ <font style="color:rgb(25, 27, 31);">Typescript = Type + JavaScript（在JS基础之上，为JS添加了类型支持）。</font>
+ <font style="color:rgb(25, 27, 31);">可以在任何支持JavaScript的平台中执行。</font>

## **<font style="color:rgb(25, 27, 31);">2. 为什么需要TypeScript</font>**
<font style="color:rgb(25, 27, 31);">我们都知道，JavaScript是弱类型的编程语言，很多的错误只有在运行的时候才会被发现，而TS在代码编译的时候（代码执行前）就可以发现错误。</font>

## **<font style="color:rgb(25, 27, 31);">3. TypeScript的特点</font>**
+ <font style="color:rgb(25, 27, 31);">支持最新的ECMAScript语法</font>
+ <font style="color:rgb(25, 27, 31);">在代码编译阶段就能发现错误</font>
+ <font style="color:rgb(25, 27, 31);">在JS基础上增加了类型支持</font>

## **<font style="color:rgb(25, 27, 31);">4. TypeScript和JavaScript的区别</font>**
| **<font style="color:rgb(25, 27, 31);">TypeScript</font>** | **<font style="color:rgb(25, 27, 31);">JavaScript</font>** |
| :--- | :--- |
| <font style="color:rgb(25, 27, 31);">编译期发现错误</font> | <font style="color:rgb(25, 27, 31);">运行时发现错误</font> |
| <font style="color:rgb(25, 27, 31);">强类型语言，支持静态和动态类型</font> | <font style="color:rgb(25, 27, 31);">弱类型语言，没有静态类型选项</font> |
| <font style="color:rgb(25, 27, 31);">支持模块、泛型和接口</font> | <font style="color:rgb(25, 27, 31);">不支持模块、泛型和接口</font> |
| <font style="color:rgb(25, 27, 31);">代码运行时会被编译成JavaScript代码，浏览器才能识别</font> | <font style="color:rgb(25, 27, 31);">可以直接在浏览器使用</font> |


## **<font style="color:rgb(25, 27, 31);">二、TypeScript环境搭建</font>**
## **<font style="color:rgb(25, 27, 31);">1. 安装编译TS的工具包</font>**
```plain
npm i -g typescript
```

## **<font style="color:rgb(25, 27, 31);">2. 验证TS是否安装成功</font>**
```plain
tsc -v
```

## **<font style="color:rgb(25, 27, 31);">3. TypeScript初体验</font>**
1. <font style="color:rgb(25, 27, 31);">创建一个TS文件，hello.ts（注意：</font>[<font style="color:rgb(9, 64, 142);">TS文件</font>](https://zhida.zhihu.com/search?content_id=234903611&content_type=Article&match_order=2&q=TS%E6%96%87%E4%BB%B6&zhida_source=entity)<font style="color:rgb(25, 27, 31);">的后缀名为</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">.ts</font>**<font style="color:rgb(25, 27, 31);">），并输入以下的内容</font>

```plain
typescript复制代码function greet(name: string): string {
   return `hello, ${name}`
 }
 
 let user = "Echo"
 console.log(greet("Echo"))
```

1. <font style="color:rgb(25, 27, 31);">将TS文件编译为JS文件，在终端中输入命令：</font>**<font style="color:rgb(25, 27, 31);">tsc hello.ts，</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">（此时，在同级目录中会出现一个同名的JS文件）</font>

```plain
typescript复制代码"use strict";
 function greet(name) {
     return "Hello, ".concat(name);
 }
 var user = "Echo";
 console.log(greet(user));
```

1. <font style="color:rgb(25, 27, 31);">执行JS代码：在终端中输入命令，</font>**<font style="color:rgb(25, 27, 31);">node hello.js</font>**<font style="color:rgb(25, 27, 31);">，终端会输出 hello, Echo。</font>

```plain
typescript
 复制代码"hello, Echo"
```

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763902827-3b1753c0-537e-4a1f-9149-f4948f24b279.png)

## **<font style="color:rgb(25, 27, 31);">4. 简化运行TS的步骤</font>**
<font style="color:rgb(25, 27, 31);">每次修改代码后，都要重复执行两个命令，才能运行TS代码，我们可以直接使用</font>**<font style="color:rgb(25, 27, 31);">ts-node</font>**<font style="color:rgb(25, 27, 31);">工具包，直接在</font>[<font style="color:rgb(9, 64, 142);">node.js</font>](https://zhida.zhihu.com/search?content_id=234903611&content_type=Article&match_order=1&q=node.js&zhida_source=entity)<font style="color:rgb(25, 27, 31);">中执行TS代码。</font>

<font style="color:rgb(25, 27, 31);">安装命令：</font>**<font style="color:rgb(25, 27, 31);">npm i -g ts-node</font>**

<font style="color:rgb(25, 27, 31);">使用方式：</font>**<font style="color:rgb(25, 27, 31);">ts-node hello.ts</font>**

## **<font style="color:rgb(25, 27, 31);">5. 运行TS文件的另一种方法</font>**
<font style="color:rgb(25, 27, 31);">在VSCode中安装</font>**<font style="color:rgb(25, 27, 31);">Code Runner</font>**<font style="color:rgb(25, 27, 31);">扩展插件，在需要运行的ts文件中按鼠标右键，选择</font>**<font style="color:rgb(25, 27, 31);">Run Code</font>**<font style="color:rgb(25, 27, 31);">(快捷键：</font>**<font style="color:rgb(25, 27, 31);">Ctrl+Alt+N</font>**<font style="color:rgb(25, 27, 31);">)。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763902736-122b0dad-82ff-4fd0-b298-8ad92c8d0933.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">6. TypeScript Playground线上环境</font>**
<font style="color:rgb(25, 27, 31);">对于刚入门TypeScript的小伙伴来说，我们可以不用安装本地的运行环境，而是直接使用线上的</font><font style="color:rgb(25, 27, 31);"> </font>[TypeScript Playground](https://link.zhihu.com/?target=https%3A//link.juejin.cn/%3Ftarget%3Dhttps%253A%252F%252Fwww.typescriptlang.org%252Fplay%253F%2523code%252FGYVwdgxgLglg9mABAcwKZQGIgDbYHICGAtqgBTAwBOAzlISQFyK2UxjIA0i2Bt9qTFm2QBKQVFbtEAbwCwAKESJK6EJSQUadYqkQBqRACIA%252Bof3de2kgoC%252BChRAS1EoXP0QBeFOixudpQwBRCAALOEMuQwAFVHZDEQcnOGxUADpsOGRyHHwdESA)<font style="color:rgb(25, 27, 31);">，我们就可以在浏览器中学习和编写TypeScript代码，通过配置TS Config的Target，可以设置不同的编译目标，从而编译生成不同的目标代码。</font>

<font style="color:rgb(25, 27, 31);">彩蛋 ，关于TypeScript的学习或者说关于前端技术的学习，看书时一个能非常好的帮助我们查漏补缺的方式，书相较于文档护着视频都更加的详细，如果你需要电子书的话，可以联系我</font>

**<font style="color:rgb(25, 27, 31);">以下这份包含103本前端经典书籍的书单（其中32本是豆瓣评分8分+），是我花费一个月时间整理的：</font>**

[免费领取103本前端开发电子书（含代码）i.uiuin.cn/cEGzVc](https://link.zhihu.com/?target=https%3A//i.uiuin.cn/cEGzVc)

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763906668-01c9a740-53ed-472a-befb-dabbccbf50e4.png)

## **<font style="color:rgb(25, 27, 31);">三、TypeScript类型注解</font>**
## **<font style="color:rgb(25, 27, 31);">1. 类型注解作用</font>**
**<font style="color:rgb(25, 27, 31);">TS类型注解的作用是为变量、函数、类等添加类型信息，用于在静态类型检查阶段检查代码的类型正确性。</font>**

## **<font style="color:rgb(25, 27, 31);">2. 类型注解用途</font>**
1. <font style="color:rgb(25, 27, 31);">提供类型提示：类型注解使得开发人员可以清晰地知道变量的类型，编辑器能够根据类型注解给出相应的代码提示，提高代码的可读性和可维护性。</font>
2. <font style="color:rgb(25, 27, 31);">静态类型检查：通过给变量添加类型注解，在编译阶段可以对代码进行静态类型检查。它会检查变量的类型是否符合预期的类型，并发现潜在的类型错误。</font>
3. <font style="color:rgb(25, 27, 31);">函数参数类型检查：类型注解可以帮助开发人员在编写函数时明确参数的类型，并在调用函数时进行参数类型检查。这样可以避免因参数类型不匹配引发的潜在错误。</font>
4. <font style="color:rgb(25, 27, 31);">对象属性类型约束：通过类型注解，可以约束对象的属性类型，确保对象的属性符合特定的类型要求。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763902373-4a6d3ae3-0644-41f7-868f-f5f8b0d72a2a.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">例如，上述代码中的</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">: number</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">就是</font>**<font style="color:rgb(25, 27, 31);">类型注解。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">约定变量num的类型为number（数值类型）。</font>

## **<font style="color:rgb(25, 27, 31);">3. 类型注解注意事项</font>**
1. **<font style="color:rgb(25, 27, 31);">约定了什么类型，就只能给变量赋值该类型的值</font>**<font style="color:rgb(25, 27, 31);">，否则，就会报错。</font>

<font style="color:rgb(25, 27, 31);">例如，我们将变量num的值123，重新赋值为字符串的“456”，此时我们就可以看到编辑器的错误提示：不能将类型“string”分配给类型“number”。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763903197-0e9397de-8e27-4e28-a0bc-7dcc2c69a3e2.png)

<font style="color:rgb(25, 27, 31);">  
</font>

1. **<font style="color:rgb(25, 27, 31);">类型注解只在编译阶段起作用，并不会影响运行时的行为。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">在编译后的 JavaScript 代码中，类型注解会被编译器忽略。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763902933-1b07181f-4296-4f08-92ef-01f96118a4d8.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">四、TypeScript类型</font>**
## **<font style="color:rgb(25, 27, 31);">1. TS中常用的基础类型</font>**
<font style="color:rgb(25, 27, 31);">我们可以将TS中常用的基础类型分为两类：</font>

1. <font style="color:rgb(25, 27, 31);">JS已有的类型</font>
2. <font style="color:rgb(25, 27, 31);">TS新增的类型</font>

<font style="color:rgb(25, 27, 31);">JS已有的类型，我们又可以分为两类：</font>

1. <font style="color:rgb(25, 27, 31);">原始数据类型：</font>**<font style="color:rgb(25, 27, 31);">number、string、boolean、null、undefined、symbol（ES6中的新类型）、bigint（ES10中的新类型）。</font>**
2. <font style="color:rgb(25, 27, 31);">对象类型：</font>**<font style="color:rgb(25, 27, 31);">object（包括数组、对象、函数等对象）。</font>**

<font style="color:rgb(25, 27, 31);">TS新增的类型：</font>**<font style="color:rgb(25, 27, 31);">any、void、自定义类型（类型别名）、联合类型、接口、元组、字面量类型、枚举等。</font>**

### **<font style="color:rgb(25, 27, 31);">1.1. 数值（number）</font>**
<font style="color:rgb(25, 27, 31);">和JS一样，TS里的所有数字都是浮点数。 这些浮点数的类型是 number。 除了支持十进制和十六进制字面量，TS还支持ECMAScript 2015中引入的二进制和八进制字面量。</font>

<font style="color:rgb(25, 27, 31);">在TS中，使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">number</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来定义数值类型：</font>

```plain
typescript复制代码// 十进制
 let decLiteral: number = 6
 // 十六进制
 let hexLiteral: number = 0xf00d
 // 二进制
 let binaryLiteral: number = 0b1010
 // 八进制
 let octalLiteral: number = 0o744
 let notANumber: number = NaN
 let infinityNumber: number = Infinity
```

<font style="color:rgb(25, 27, 31);">编译结果：</font>

```plain
typescript复制代码// 十进制
 var decLiteral = 6;
 // 十六进制
 var hexLiteral = 0xf00d;
 // 二进制
 var binaryLiteral = 10;
 // 八进制
 var octalLiteral = 484;
 var notANumber = NaN;
 var infinityNumber = Infinity;
```

### **<font style="color:rgb(25, 27, 31);">1.2. 布尔值（boolean）</font>**
<font style="color:rgb(25, 27, 31);">在TS中，使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">boolean</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来定义布尔值类型：</font>

```plain
typescript
 复制代码let flag: boolean = false;
```

<font style="color:rgb(25, 27, 31);">编译结果：</font>

```plain
typescript
复制代码var flag = false;
```

### **<font style="color:rgb(25, 27, 31);">1.3. 字符串（string）</font>**
<font style="color:rgb(25, 27, 31);">在TS中，使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">string</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来定义字符串类型：</font>

<font style="color:rgb(25, 27, 31);">在TS中，字符串的表现形式主要有以下三种方式：</font>

1. <font style="color:rgb(25, 27, 31);">使用单引号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">'</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）</font>
2. <font style="color:rgb(25, 27, 31);">使用双引号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">"</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）</font>
3. <font style="color:rgb(25, 27, 31);">使用模板字符串，它可以定义多行文本和内嵌表达式。这种字符串是被反引号包围（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">`</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">），并且以</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">${ expr }</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">这种形式嵌入表达式</font>

```plain
typescript复制代码let myName: string = "Echo"
let age: number = 25

// 模板字符串
let sentence: string = `Hello, my name is ${ myName }. I'll be ${ age + 1} years old next month.`

// 上面定义的sentence的语句与下面定义的sentence1语句的效果相同
let sentence1: string = "Hello, my name is " + myName + ". I'll be " + ( age + 1) +" years old next month."
```

<font style="color:rgb(25, 27, 31);">编译结果：</font>

```plain
typescript复制代码var myName = "Echo";
var age = 25;
// 模板字符串
var sentence = "Hello, my name is ".concat(myName, ". I'll be ").concat(age + 1, " years old next month.");
// 上面定义的sentence的语句与下面定义的sentence1语句的效果相同
var sentence1 = "Hello, my name is " + myName + ". I'll be " + (age + 1) + " years old next month.";
```

### **<font style="color:rgb(25, 27, 31);">1.4. null 和 undefined</font>**
<font style="color:rgb(25, 27, 31);">null 和 undefined 是所有类型的子类型，默认情况下，可以把null 和 undefined赋值给其他类型。</font>

<font style="color:rgb(25, 27, 31);">注意：如果你将</font><font style="color:rgb(25, 27, 31);"> </font>[<font style="color:rgb(9, 64, 142);">tsconfig.json</font>](https://zhida.zhihu.com/search?content_id=234903611&content_type=Article&match_order=1&q=tsconfig.json&zhida_source=entity)<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">文件中的</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">strictNullChecks</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">选项设置为</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">false</font>**<font style="color:rgb(25, 27, 31);">，下面这种操作不会报错，不过尽量不要这么做。</font>

```plain
typescript复制代码// 将 null 和 undefined 赋值给 string 类型
let str: string = "哈哈哈"
str = null
str = undefined

// 将 null 和 undefined 赋值给 number 类型
let num: number = 123
num = null
num = undefined

// 将 null 和 undefined 赋值给 object 类型
let obj: object = {}
obj = null
obj = undefined

// 将 null 和 undefined 赋值给 boolean 类型
let flag: boolean = false
flag = null
flag = undefined

// 将 null 和 undefined 赋值给 symbol 类型
let sym: symbol = Symbol("abc")
sym = null
sym = undefined

// 将 null 和 undefined 赋值给 bigint 类型
let big: bigint =  10n;
big = null
big = undefined
```

<font style="color:rgb(25, 27, 31);">编译结果：</font>

```plain
typescript复制代码// 将 null 和 undefined 赋值给 string 类型
 var str = "哈哈哈";
 str = null;
 str = undefined;
 // 将 null 和 undefined 赋值给 number 类型
 var num = 123;
 num = null;
 num = undefined;
 // 将 null 和 undefined 赋值给 object 类型
 var obj = {};
 obj = null;
 obj = undefined;
 // 将 null 和 undefined 赋值给 boolean 类型
 var flag = false;
 flag = null;
 flag = undefined;
 // 将 null 和 undefined 赋值给 symbol 类型
 var sym = Symbol("abc");
 sym = null;
 sym = undefined;
 // 将 null 和 undefined 赋值给 bigint 类型
 var big = 10n;
 big = null;
 big = undefined;
```

<font style="color:rgb(25, 27, 31);">注意：如果你在</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">tsconfig.json</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">文件中指定了“</font>**<font style="color:rgb(25, 27, 31);">strictNullChecks：true</font>**<font style="color:rgb(25, 27, 31);">”，null 和 undefined 只能赋值给</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">void</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">和它们各自的类型。</font>

<font style="color:rgb(25, 27, 31);">下面这种情况会报错：</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763903860-45668a14-a048-49a5-a376-991f73d24161.png)

<font style="color:rgb(25, 27, 31);">  
</font>

### **<font style="color:rgb(25, 27, 31);">1.5. symbol</font>**
**<font style="color:rgb(25, 27, 31);">symbol</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">是ES6新增的一种基本数据类型，</font>**<font style="color:rgb(25, 27, 31);">Symbol()函数</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">会返回</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">symbol</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">类型的值，</font>**<font style="color:rgb(25, 27, 31);">每个从 Symbol()函数 返回的 symbol 的值都是唯一的。</font>**

```plain
typescript复制代码const sym1: symbol = Symbol()
 const sym2: symbol = Symbol('temp')
 const sym3: symbol = Symbol('temp')
```

<font style="color:rgb(25, 27, 31);">上面的代码创建了三个新的 symbol 类型，但是注意的是，每个从 Symbol()函数 返回的值都是唯一的。</font>

<font style="color:rgb(25, 27, 31);">此时，如果我们在控制台打印下面的代码，两者并不相等。</font>

```plain
typescript
 复制代码console.log(sym2 === sym3) // false
```

### **<font style="color:rgb(25, 27, 31);">1.6. bigint</font>**
**<font style="color:rgb(25, 27, 31);">bigint</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">是ES10新增的一种基本数据类型，在JS中，可以用 Number 表示的最大整数为 2^53 - 1，可以写为 Number.MAX_SAFE_INTEGER。如果超过了这个界限，那么就可以用 BigInt 来表示，它可以表示任意大的整数。</font>

<font style="color:rgb(25, 27, 31);">在一个整数字面量后面加 n 的方式定义一个 bigint，或者调用函数 BigInt()。</font>

```plain
typescript复制代码let big1: bigint = 10n
 let big2: bigint = BigInt(10)
 
 console.log(big1 === big2) // true
```

### **<font style="color:rgb(25, 27, 31);">1.7. 区别</font>**
### **<font style="color:rgb(25, 27, 31);">1.7.1. null 和 undefined 的区别</font>**
1. <font style="color:rgb(25, 27, 31);">在JS中，null 表示“什么都没有”，而 undefined 是一个没有设置值的变量</font>
2. <font style="color:rgb(25, 27, 31);">用 typeof 检测 null，返回 object；typeof 一个没有值的变量会返回 undefined</font>
3. <font style="color:rgb(25, 27, 31);">null 是一个只有一个值的特殊类型，表示一个空对象的引用</font>
4. <font style="color:rgb(25, 27, 31);">null 和 undefined 是其它任何类型（包括void）的子类型，可以赋值给其它类型，如数字类型，此时，赋值后的类型会变成 null 或 undefined。而在TS中启用严格的空校验（strictNullChecks）特性，就可以使得 null 和 undefined 只能被赋值给 void 或本身对应的类型</font>

### **<font style="color:rgb(25, 27, 31);">1.7.2. bigint 和 number 的区别</font>**
1. <font style="color:rgb(25, 27, 31);">number 和 bigint 都可以表示数字，但是两者不能进行相互转换</font>
2. <font style="color:rgb(25, 27, 31);">仅在值大于 2^53 - 1时，才使用 bigint，否则尽量使用 number</font>
3. <font style="color:rgb(25, 27, 31);">用 typeof 检测 bigint 对象时，返回 bigint，用 typeof 检测 number，返回 number</font>

```plain
typescript复制代码console.log(typeof 10) // number
 console.log(typeof Number(10)) // number
 console.log(typeof 10n) // bigint
 console.log(typeof BigInt(10)) // bigint
```

### **<font style="color:rgb(25, 27, 31);">1.8. 对象类型</font>**
### **<font style="color:rgb(25, 27, 31);">1.8.1. 数组（Array）类型</font>**
<font style="color:rgb(25, 27, 31);">数组类型的写法有两种：</font>

1. <font style="color:rgb(25, 27, 31);">在类型后面加上 []，例如</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">number[]</font>**

```plain
typescript
复制代码let num: number[] = [1, 2, 3, 4]
```

1. <font style="color:rgb(25, 27, 31);">使用数组泛型 <>，例如</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">Array</font>**

```plain
typescript
复制代码let num: Array<number> = [1, 2, 3, 4]
```

<font style="color:rgb(25, 27, 31);">推荐使用第一种写法。</font>

**<font style="color:rgb(25, 27, 31);">注意：</font>**

1. <font style="color:rgb(25, 27, 31);">如果我们定义了一个number类型的数组，此时数组的项中就不能出现其它的类型。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763904007-3b42ab67-d32a-4453-8015-c49bb02b2225.png)

<font style="color:rgb(25, 27, 31);">  
</font>

1. <font style="color:rgb(25, 27, 31);">如果我们希望数组中既有number类型，又有string类型，此时我们可以用联合类型来写（关于联合类型，后面会详细讲到）。</font>

```plain
typescript
复制代码let arr: (number | string)[] = [1, 'a', 2, 'b']
```

<font style="color:rgb(25, 27, 31);">上面的代码，表示的是，定义一个arr数组，这个数组中可以出现 number 或者 string 类型的元素。</font>

```plain
typescript复制代码let arr1: number | string[] = 123
let arr2: number | string[] = ['a', 'b', 'c']
```

<font style="color:rgb(25, 27, 31);">上面的代码，arr1 和 arr2 都表示即可以是number类型，又可以是string[]，加了小括号和不加小括号，含义不同。</font>

### **<font style="color:rgb(25, 27, 31);">1.8.2. 函数类型</font>**
<font style="color:rgb(25, 27, 31);">函数类型实际上指的是：</font>**<font style="color:rgb(25, 27, 31);">函数参数和返回值的类型</font>**<font style="color:rgb(25, 27, 31);">。</font>

<font style="color:rgb(25, 27, 31);">为函数指定类型的两种方式：</font>

1. <font style="color:rgb(25, 27, 31);">单独指定参数、返回值的类型</font>
2. <font style="color:rgb(25, 27, 31);">同时指定参数、返回值的类型</font>

<font style="color:rgb(25, 27, 31);">在JS中，有两种常见的定义函数的方式：</font>

1. <font style="color:rgb(25, 27, 31);">函数声明</font>
2. <font style="color:rgb(25, 27, 31);">函数表达式</font>

### **<font style="color:rgb(25, 27, 31);">1.8.2.1. 单独指定参数、返回值的类型</font>**
```plain
typescript复制代码// 函数声明写法
function sum(num1: number, num2: number): number {
  return num1 + num2
}
// 函数表达式写法
const sum1 = (num1: number, num2: number): number => {
  return num1 + num2
}

console.log(sum(10, 20))  // 30
console.log(sum1(10, 20)) // 30
```

### **<font style="color:rgb(25, 27, 31);">1.8.2.2. 同时指定参数、返回值的类型</font>**
```plain
typescript复制代码const sum: (num1: number, num2: number) => number = (num1, num2) => {
  return num1 + num2
}

console.log(sum(10, 20)) // 30
```

<font style="color:rgb(25, 27, 31);">注意：不要把ES6中的 => 和 TypeScript 中的 =>混淆了。</font>

<font style="color:rgb(25, 27, 31);">在ES6中，=>叫做箭头函数。而在 TypeScript 的类型定义中，=>用来表示函数的定义，左边是输入类型，需要用括号括起来，右边是输出类型。</font>

### **<font style="color:rgb(25, 27, 31);">1.8.2.3. 函数没有返回值</font>**
<font style="color:rgb(25, 27, 31);">如果函数没有返回值，那么，函数返回值类型为：</font>**<font style="color:rgb(25, 27, 31);">void</font>**<font style="color:rgb(25, 27, 31);">。</font>

```plain
typescript复制代码function greet(name: string): void {
  console.log("Hello, ", name);
}

greet("Echo")
```

### **<font style="color:rgb(25, 27, 31);">1.8.2.4. 可选参数</font>**
<font style="color:rgb(25, 27, 31);">使用函数实现某个功能时，参数可以传也可以不传，这种情况下，在给函数参数指定类型时，就用到</font>**<font style="color:rgb(25, 27, 31);">可选参数</font>**<font style="color:rgb(25, 27, 31);">了。</font>

<font style="color:rgb(25, 27, 31);">可选参数使用问号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">?</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）标记，表示该参数可以省略。</font>

```plain
typescript复制代码function greet(name: string, greeting?: string): string {
  if (greeting) {
    return `${greeting}, ${name}!`;
  } else {
    return `Hello, ${name}!`;
  }
}

console.log(greet("Echo")) // "Hello, Echo!"
console.log(greet("Echo", "Hi")) // "Hi, Echo!"
```

<font style="color:rgb(25, 27, 31);">上面的代码中，我们在第二个参数 greeting 的后面加了个问号，表示在调用 greet() 函数时，该参数可传可不传。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">可选参数只能出现在</font>**[**<font style="color:rgb(9, 64, 142);">参数列表</font>**](https://zhida.zhihu.com/search?content_id=234903611&content_type=Article&match_order=1&q=%E5%8F%82%E6%95%B0%E5%88%97%E8%A1%A8&zhida_source=entity)**<font style="color:rgb(25, 27, 31);">的最后面，也就是说，可选参数后面不能再出现必选参数。</font>**

<font style="color:rgb(25, 27, 31);">错误演示：下面代码中，我们把第一个参数改为可选的，第二个参数改为必选的，然后将鼠标移到必选参数上面，可以看到错误提示：“必选参数不能位于可选参数后”。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763904142-16990b23-acce-42c6-b830-e88c06b08a83.png)

<font style="color:rgb(25, 27, 31);">  
</font>

### **<font style="color:rgb(25, 27, 31);">1.8.2.5. 参数默认值</font>**
<font style="color:rgb(25, 27, 31);">在ES6中，允许给函数的参数添加默认值，而TypeScript会将添加了默认值的参数识别为可选参数。</font>

<font style="color:rgb(25, 27, 31);">默认参数使用等号（</font>**<font style="color:rgb(25, 27, 31);">=</font>**<font style="color:rgb(25, 27, 31);">）赋予默认值。</font>

```plain
typescript复制代码function buildName(firstName: string, lastName: string = 'Cat') {
    return firstName + ' ' + lastName;
}

console.log(buildName('Tom', 'Cat')) // Tom Cat
console.log(buildName('Tom')) // Tom Cat
```

<font style="color:rgb(25, 27, 31);">注意：与可选参数不同的是，</font>**<font style="color:rgb(25, 27, 31);">带默认值的参数不需要放在必选参数的后面</font>**<font style="color:rgb(25, 27, 31);">。如果带默认值的参数出现在必选参数的前面，我们在调用函数时，必须明确的传入</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">undefined</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">值来获得默认值。</font>

```plain
typescript复制代码function buildName(firstName = "Echo", lastName: string) {
    return firstName + " " + lastName;
}

console.log(buildName("james"))           // 报错，未提供“lastName”自变量
console.log(buildName("Jerk", "Lose"))    // Jerk Lose
console.log(buildName(undefined, "Deno")) // Echo Deno
```

### **<font style="color:rgb(25, 27, 31);">1.8.2.6. 剩余参数</font>**
<font style="color:rgb(25, 27, 31);">使用三个点（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">...</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）前缀和参数名来定义剩余参数。</font>

<font style="color:rgb(25, 27, 31);">剩余参数允许我们将不确定数量的参数表示为一个数组。</font>

```plain
typescript复制代码function sum(x: number, ...rest: number[]): number {
  let result = x;
  for (let num of rest) {
    result += num;
  }
  return result;
}


console.log(sum(1, 2, 3, 4, 5)) // 15
console.log(sum(1, 2, 3))       // 6
```

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">剩余参数必须是函数参数列表中的最后一个参数</font>**<font style="color:rgb(25, 27, 31);">。</font>

### **<font style="color:rgb(25, 27, 31);">1.8.2.7. 函数重载</font>**
<font style="color:rgb(25, 27, 31);">函数重载允许我们为同一个函数提供多个函数类型定义，以便在不同的参数类型或返回值类型下进行不同的处理。</font>

<font style="color:rgb(25, 27, 31);">例如，我们现在需要实现一个函数，需求是：输入数字123，输出反转的数字321，输入字符串"hello"，输出反转的字符串"olleh"。</font>

<font style="color:rgb(25, 27, 31);">利用联合类型，我们可以这么实现：</font>

```plain
typescript复制代码function reverse(x: number | string): number | string {
  if (typeof x === 'number') {
    return Number(x.toString().split('').reverse().join(''));
  } else if (typeof x === 'string') {
    return x.split('').reverse().join('');
  }
}

console.log(reverse(123))     // 321
console.log(reverse("hello")) // olleh
```

<font style="color:rgb(25, 27, 31);">然后这样会有一个问题，就是输出的类型不能准确的知道，我们想输入为数字的时候，输出的类型应该也为数值类型，输入为字符串的时候，输出类型应该也为字符串类型。</font>

<font style="color:rgb(25, 27, 31);">这时，我们可以用</font>**<font style="color:rgb(25, 27, 31);">重载</font>**<font style="color:rgb(25, 27, 31);">定义多个reserve的函数类型：</font>

```plain
typescript复制代码function reverse(x: number): number;
function reverse(x: string): string;
function reverse(x: number | string): number | string {
  if (typeof x === 'number') {
    return Number(x.toString().split('').reverse().join(''));
  } else if (typeof x === 'string') {
    return x.split('').reverse().join('');
  }
}

console.log(reverse(123), typeof reverse(123))     // 321 number
console.log(reverse("hello"), typeof reverse("hello")) // olleh string
```

<font style="color:rgb(25, 27, 31);">上述代码中，第1-2行是函数定义，第3-9行是函数实现。第11行代码，我们调用reverse函数，并传入数值123，使用typeof检测类型为number，第12行代码，我们调用reverse函数，并传入字符串"hello"，使用typeof检测类型为string，这样我们利用函数重载就实现了输入为什么类型，输出应该也是什么类型。</font>

### **<font style="color:rgb(25, 27, 31);">1.8.3. 对象类型</font>**
<font style="color:rgb(25, 27, 31);">JS中的对象是由属性和方法构成的，而TS中对象的类型就是在描述对象的结构（有什么类型的属性和方法）。</font>

### **<font style="color:rgb(25, 27, 31);">1.8.3.1. 定义对象类型</font>**
+ <font style="color:rgb(25, 27, 31);">使用花括号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">{}</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）来定义对象类型，属性采用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">属性名: 类型</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">的形式；方法采用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">方法名(): 返回值类型</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">的形式。</font>
+ <font style="color:rgb(25, 27, 31);">如果方法有参数，就在方法名后面的小括号中指定参数类型（比如：greet(name: string): void）。</font>
+ <font style="color:rgb(25, 27, 31);">在一行代码中指定对象的多个属性类型时，使用分号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">;</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）来分隔。</font>
+ <font style="color:rgb(25, 27, 31);">如果一行代码只指定一个属性类型（通过换行来分隔多个属性类型），可以去掉分号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">;</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）。</font>
+ <font style="color:rgb(25, 27, 31);">方法的类型也可以使用箭头函数形式，比如：{ sayHi: () => void }。</font>

```plain
typescript复制代码let person: { name: string; age: number; sayHi(): void; greet(name: string): void } = {
  name: 'John',
  age: 25,
  sayHi() {},
  greet(name) {}
}
```

<font style="color:rgb(25, 27, 31);">上面的代码，也可以写成下面这种形式：</font>

```plain
typescript复制代码let person: {
  name: string
  age: number
  // sayHi(): void
  sayHi: () => void
	// greet(name: string): void
  greet: (name: string) => void
} = {
  name: 'John',
  age: 25,
  sayHi() {},
  greet(name) {}
}
```

### **<font style="color:rgb(25, 27, 31);">1.8.3.2. 对象可选属性</font>**
<font style="color:rgb(25, 27, 31);">对象类型中的属性或方法可以是可选的，使用问号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">?</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）标记。</font>

<font style="color:rgb(25, 27, 31);">可选属性表示该属性可以存在，也可以不存在。</font>

<font style="color:rgb(25, 27, 31);">比如，我们在使用axios({...})时，如果发送GET请求，method属性就可以省略。</font>

```plain
typescript复制代码function myAxios(config: { url: string; method?: string}) {
  console.log(config)
}

myAxios({ url: 'http://localhost:3000' })
```

### **<font style="color:rgb(25, 27, 31);">1.8.3.3. 对象只读属性</font>**
<font style="color:rgb(25, 27, 31);">对象的属性也可以是只读的，使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">readonly</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字标记。</font>

<font style="color:rgb(25, 27, 31);">只读属性表示该属性的值在创建后就不能被修改。</font>

```plain
typescript复制代码let person: {
  name: string
  age: number
	readonly id: number
} = {
  name: 'John',
  age: 25,
	id: 1
}
```

## **<font style="color:rgb(25, 27, 31);">2. 元组（Tuple）</font>**
### **<font style="color:rgb(25, 27, 31);">2.1. 元组的定义</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，</font>**<font style="color:rgb(25, 27, 31);">元组（Tuple）是一种特殊的数组类型，它允许</font>**<font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">存储具有固定数量和特定类型顺序的元素。</font>**

<font style="color:rgb(25, 27, 31);">声明一个元组的语法是在类型注解中使用方括号</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">[]</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">，并使用逗号分隔元素的类型。</font>

<font style="color:rgb(25, 27, 31);">例如，下面是一个包含两个元素的元组：</font>

```plain
typescript复制代码let tuple: [string, number];
tuple = ["Echo", 26];
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们声明了一个名为 tuple 的变量，它被注解为一个元组类型 [string, number]。我们可以将一个包含两个元素的数组赋值给 tuple，其中第一个元素是一个字符串，第二个元素是一个数字。</font>

### **<font style="color:rgb(25, 27, 31);">2.2. 元组的特点</font>**
1. <font style="color:rgb(25, 27, 31);">元组可以包含多个不同类型的元素，但每个元素的类型和顺序是固定的。</font>
2. <font style="color:rgb(25, 27, 31);">元组的长度是固定的，在创建元组时必须指定元素的数量。</font>
3. <font style="color:rgb(25, 27, 31);">可以通过索引访问元组中的元素，索引从 0 开始。</font>
4. <font style="color:rgb(25, 27, 31);">元组中的每个元素可以具有不同的类型注解。</font>
5. <font style="color:rgb(25, 27, 31);">当访问元组中的元素时，会根据其类型注解提供相关的类型检查和智能提示。</font>

<font style="color:rgb(25, 27, 31);">下面是一些操作元组的示例：</font>

```plain
typescript复制代码// 声明一个 tuple 变量，它的类型注解为：[string, number, boolean]，然后把一个包含3个元素的数组赋值给 tuple，其中，数组的第一个元素为字符串类型，第二个元素为数值类型，第三个元素为布尔值类型
 let tuple: [string, number, boolean] = ["Echo", 26, true];
 
 // 通过索引访问元组中的元素，索引从 0 开始
 console.log(tuple[0]); // 输出：Echo
 console.log(tuple[1]); // 输出：26
 console.log(tuple[2]); // 输出：true
 
 // 可以通过索引重新赋值，赋值的类型需要跟类型注解中的固定位置的类型一样
 tuple[0] = "june";
 tuple[1] = 28;
 
 console.log(tuple); // 输出：["june", 28, true]
 
 // 下面的代码会报错：不能将类型 "[string, number, boolean, string]" 分配给类型 "[string, number, boolean]"，源具有 4 个元素，但目标仅允许3个
 tuple = ["Echo", 26, true, "hhhh"]
 
 // 下面的代码也会报错，因为元组的第一个元素类型要求为字符串类型，不能将 number 类型分配给 string 类型。
 tuple = [1, 28, true]
```

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">当访问元组中的元素以及进行元素的赋值时，要确保索引和类型注解的一致性，否则可能会导致类型错误。</font>**

### **<font style="color:rgb(25, 27, 31);">2.3. 元组类型的解构赋值</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，可以使用解构赋值语法来从元组中提取和赋值元素。</font>

<font style="color:rgb(25, 27, 31);">下面是一个简单的示例，展示了如何使用解构赋值从元组中获取各个元素：</font>

```plain
typescript复制代码let tuple: [string, number] = ["Echo", 26];
 
 let [str, num] = tuple;
 
 console.log(str); // 输出：Echo
 console.log(num); // 输出：26
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们首先声明了一个元组 tuple，其中包含一个字符串类型的元素和一个数值类型的元素。接着，我们使用解构赋值语法将元组中的元素分别赋值给变量 str 和 num。</font>

<font style="color:rgb(25, 27, 31);">通过解构赋值，我们可以直接使用对应位置的变量来获取元组中的元素值，而不需要通过索引访问。这样可以以一种简洁、语义明确的方式从元组中解构得到各个元素。</font>

**<font style="color:rgb(25, 27, 31);">解构赋值还支持忽略某些元素，或者只提取部分元素。</font>**

<font style="color:rgb(25, 27, 31);">例如，如果只想获取元组中的第一个元素，可以使用以下方式：</font>

```plain
typescript复制代码let tuple: [string, number] = ["Echo", 26];
 
 let [str] = tuple;
 
 console.log(str); // 输出：Echo
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们只声明了一个变量 str，而忽略了后面的元素。通过解构赋值只获取所需元素，可以简化代码并提高可读性。</font>

<font style="color:rgb(25, 27, 31);">另外，</font>**<font style="color:rgb(25, 27, 31);">解构赋值还支持使用默认值。</font>**

<font style="color:rgb(25, 27, 31);">当从元组中解构一个不存在的元素时，可以提供一个默认值作为备选值。例如：</font>

```plain
typescript复制代码let tuple: [string, number?] = ["Echo"];
 
 let [str, num = 26] = tuple;
 
 console.log(str); // 输出：Echo
 console.log(num); // 输出：26
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们声明了一个带有可选的数字元素的元组 tuple，但是没有给出对应的数字值。在解构赋值时，如果元组中缺少对应的元素，就会使用默认值 undefined，这里我们将默认值设置为 26。</font>

<font style="color:rgb(25, 27, 31);">总而言之，使用解构赋值可以轻松地从元组中提取和赋值元素，使得代码更加简洁和可读。它是一种方便的语法，特别适用于处理具有固定结构的数据。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">在解构赋值时，如果解构数组元素的个数超过元组中元素的个数，会出现错误。</font>**

```plain
typescript复制代码let tuple: [string, number] = ["Echo", 26];

let [str, num, sex] = tuple;
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们解构时新增了一个 sex 变量，但元组的长度为 2，在索引 "2" 处没有元素。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763904138-adb15662-99d9-4c39-8124-a47a9e2f9428.png)

<font style="color:rgb(25, 27, 31);">  
</font>

### **<font style="color:rgb(25, 27, 31);">2.4. 元组类型的可选元素</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，可以使用问号</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">?</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来将元素定义为可选的，以表示元组中某些位置的元素是可选的。</font>

```plain
typescript复制代码let tuple: [string, number?] = ["Echo"];

console.log(tuple);   // 输出 [ 'Echo', undefined ]

tuple = ["june", 26];

console.log(tuple);  // 输出 [ 'june', 26 ]
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个元组 tuple，该元组有两个元素，第一个是一个字符串类型的元素，而第二个是一个可选的数值类型的元素。当我们只提供第一个元素时，第二个元素会被默认设置为 undefined。然后，我们更新了元组的值，提供了第二个元素的值。此时，元组中的两个元素都有具体的值。</font>

<font style="color:rgb(25, 27, 31);">注意，</font>**<font style="color:rgb(25, 27, 31);">当一个元组中包含一个可选元素时，该元素可以存在或不存在，但是顺序必须与元组类型定义一致。在解构赋值时，可以使用默认值来处理可选元素的缺失情况。</font>**

```plain
typescript复制代码let tuple: [string, number?] = ["Echo"];

let [str, num = 26] = tuple;

console.log(str); // 输出：Echo
console.log(num); // 输出：26
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用解构赋值将元组中的元素分别赋值给变量 str 和 num。由于元组只提供了一个元素，没有提供可选的第二个元素，所以 num 的值将使用默认值 26。</font>

<font style="color:rgb(25, 27, 31);">通过使用可选元素，可以更灵活地定义元组类型，允许元组中特定位置的元素是可选的。这样，我们可以在处理数据时更好地适应不完整或可变的情况。</font>

### **<font style="color:rgb(25, 27, 31);">2.5. 元组类型的剩余元素</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，可以使用剩余元素（Rest Elements）来表示元组中剩余的元素，即将剩余的元素放入一个数组中。</font>

```plain
typescript复制代码let tuple: [string, number, ...boolean[]] = ["Echo", 26, true, true, false];

console.log(tuple); // 输出：[ 'Echo', 26, true, true, false ]
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个元组 tuple，包含一个字符串元素、一个数字元素，以及剩余元素使用剩余元素语法</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">...</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">定义的布尔类型数组。在创建元组时，我们提供了多个布尔类型的元素，它们会被放入一个数组并作为剩余元素。这样，元组中除了前两个元素以外的其他元素都会被放入数组中，并以数组的形式表示。</font>

```plain
typescript复制代码let tuple: [string, number, ...boolean[]] = ["Echo", 26, true, true, false];

let [str, num, ...boolArr] = tuple;

console.log(str);      // 输出：Echo
console.log(num);      // 输出：26
console.log(boolArr);  // 输出：[true, true, false]
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用解构赋值从元组中提取出各个元素。通过使用 ...boolArr，我们将剩余的布尔类型元素提取到名为 boolArr 的数组中。</font>

<font style="color:rgb(25, 27, 31);">使用剩余元素可以处理元组中数量不确定的元素，可以更灵活地处理和操作这些元素。它提供了一种方便的方式来处理由不固定数量的元素组成的结构数据。</font>

### **<font style="color:rgb(25, 27, 31);">2.6. 只读的元组类型</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，可以使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">readonly</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">修饰符来创建只读的元组类型，即元组中的元素不可被修改。</font>

```plain
typescript复制代码let tuple: readonly [string, number] = ["Echo", 26];

console.log(tuple);    // 输出：[ 'Echo', 26 ]

tuple[0] = "world";    // 编译错误：无法为“0”赋值，因为它是只读属性
tuple.push('abc');     // 编译错误：类型 "readonly [string, number]" 上不存在 "push"
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用 readonly 修饰符将 tuple 声明为只读的元组类型。这意味着在运行时，我们无法修改元组中的元素的值。</font>

<font style="color:rgb(25, 27, 31);">尝试对 tuple 进行赋值或调用修改元素的方法（如 push）时，TypeScript 编译器会报错，因为元组被声明为只读，无法被修改。</font>

<font style="color:rgb(25, 27, 31);">只读的元组类型在某些场景下非常有用，特别是当希望确保元组中的数据不会被意外修改时。它提供了一种强制保护元组数据不可变性的机制。</font>

## **<font style="color:rgb(25, 27, 31);">3. 字面量类型</font>**
<font style="color:rgb(25, 27, 31);">当我们在 TypeScript 中使用字面量类型，我们可以明确指定变量只能取特定的字面量值，而不是其他可能性。这样可以在编译时捕获潜在的错误，并提供更好的类型推断和类型检查支持。</font>

<font style="color:rgb(25, 27, 31);">在 TypeScript 中，可以使用多种类型的字面量进行类型定义，包括字符串字面量类型、数字字面量类型、布尔字面量类型和符号字面量类型。</font>

### **<font style="color:rgb(25, 27, 31);">3.1. 字符串字面量类型</font>**
<font style="color:rgb(25, 27, 31);">使用字符串字面量表示的类型，只能取特定的字符串值。</font>

```plain
typescript复制代码let direction: "Up" | "Right" | "Down" | "Left";

direction = "Right";   // 合法
direction = "none";    // 错误，只能取值为 "Up" | "Right" | "Down" | "Left"
```

### **<font style="color:rgb(25, 27, 31);">3.2. 数字字面量类型</font>**
<font style="color:rgb(25, 27, 31);">使用数字字面量表示的类型，只能取特定的数字值。</font>

```plain
typescript复制代码let num: 1 | 2 | 3;
num = 2; // 合法
num = 4; // 错误，只能取值为 1、2 或 3
```

### **<font style="color:rgb(25, 27, 31);">3.3. 布尔字面量类型</font>**
<font style="color:rgb(25, 27, 31);">使用布尔字面量表示的类型，只能取特定的布尔值。</font>

```plain
typescript复制代码let isShow: true | false;
isShow = true;  // 合法
isShow = false; // 合法
isShow = 1;     // 错误，只能取值为 true 或 false
```

### **<font style="color:rgb(25, 27, 31);">3.4. 符号字面量类型</font>**
<font style="color:rgb(25, 27, 31);">使用符号字面量表示的类型，只能取特定的符号值。</font>

```plain
typescript复制代码const apple: unique symbol = Symbol("apple");
const orange: unique symbol = Symbol("orange");

let fruit: typeof apple | typeof orange;

fruit = apple;           // 合法
fruit = orange;          // 合法
fruit = Symbol("apple"); // 错误，只能取预定义的 apple 或 orange
```

<font style="color:rgb(25, 27, 31);">字面量类型不仅可以用于变量的定义，还可以用于</font>**<font style="color:rgb(25, 27, 31);">函数的参数、返回值、对象属性</font>**<font style="color:rgb(25, 27, 31);">等地方。通过使用字面量类型，我们可以在编写代码时明确指定特定的取值范围，提高代码的可读性和可维护性。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，字面量类型具有一个特殊的用途，即与联合类型结合使用，以实现更精确的类型约束。例如，联合类型 string | number 表示可以是字符串或数字类型的值，而字面量类型 "success" | "error" 表示只能是字符串 "success" 或 "error"，它们可以一起使用来实现更精确的类型定义。</font>

```plain
typescript复制代码let result: "success" | "error" | number;
result = "success"; // 合法
result = 42;        // 合法
result = true;      // 错误，只能取值为 "success"、"error" 或 number 类型
```

### **<font style="color:rgb(25, 27, 31);">3.5. 函数参数中的字面量类型</font>**
```plain
typescript复制代码function move(direction: "up" | "right" | "down" | "left"): void {
  console.log(direction);
}

move("up");    // 合法
move("left");  // 合法
move(10);      // 错误，只能取值为 "up" 或 "right" 或 "down" 或 "left"
```

<font style="color:rgb(25, 27, 31);">在上述示例中，函数 move 的参数 direction 的类型被指定为 "up" | "right" | "down" | "left"，这意味着参数 direction 只能接受这四个特定的值。</font>

### **<font style="color:rgb(25, 27, 31);">3.6. 函数返回值中的字面量类型</font>**
```plain
typescript复制代码function getMove(direction: string): "up" | "right" | "down" | "left" {
  if (direction === 'W') {
    return "up";
  } else if (direction === 'D') {
    return "right";
  } else if (direction === 'S') {
    return "down";
  } else {
    return "left";
  }
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，函数 getMove 的返回值被指定为 "up" | "right" | "down" | "left"，这表示函数的返回值只能是这四个特定的值之一。</font>

### **<font style="color:rgb(25, 27, 31);">3.7. 对象属性中的字面量类型</font>**
```plain
typescript复制代码interface Options {
  mode: "light" | "dark";
  size: "small" | "medium" | "large";
}

let config: Options = {
  mode: "light",
  size: "medium"
};
```

<font style="color:rgb(25, 27, 31);">在上述示例中，Options 接口中的 mode 属性的类型被指定为 "light" | "dark"，size 属性的类型被指定为 "small" | "medium" | "large"，这意味着对象 config 的 mode 属性只能是其中一个值，size 属性也只能是其中一个值。</font>

### **<font style="color:rgb(25, 27, 31);">3.8. let 和 const 分析</font>**
### **<font style="color:rgb(25, 27, 31);">3.8.1 let 声明的字面量类型</font>**
```plain
typescript复制代码let direction: "Up" | "Right" | "Down" | "Left";

direction = "Right";   // 合法
direction = "none";    // 错误，只能取值为 "Up" | "Right" | "Down" | "Left"
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用 let 关键字声明了变量 direction，并将其类型指定为 "Up" | "Right" | "Down" | "Left"，因此 direction 只能取值为 "Up" 或 "Right" 或 "Down" 或 "Left" 这四个特定值中的其中一个。</font>

### **<font style="color:rgb(25, 27, 31);">3.8.2 const 声明的字面量类型</font>**
```plain
typescript
复制代码const size: "small" | "medium" | "large" = "medium";
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用 const 关键字声明了常量 size，并将其类型指定为 "small" | "medium" | "large"。由于使用了 const，size 是一个只读的常量，且初始值为 "medium"。因此，size 的值将永远是 "medium"，不能被重新赋值。</font>

<font style="color:rgb(25, 27, 31);">使用 let 和 const 关键字来声明变量和常量时，可以配合字面量类型提供更具体和可靠的类型约束。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">const 声明的常量在声明时必须被初始化，并且一旦初始化后，其值将不能被修改。而 let 声明的变量可以在后续代码中被重新赋值。</font>**

## **<font style="color:rgb(25, 27, 31);">4. 枚举（Enum）</font>**
<font style="color:rgb(25, 27, 31);">枚举（Enum）是一种用于定义一组命名常量的数据结构。</font>

### **<font style="color:rgb(25, 27, 31);">4.1. 基本枚举</font>**
```plain
typescript复制代码enum Direction {
  Up,
  Down,
  Left,
  Right
}

let dir: Direction = Direction.Up;
console.log(dir); // 输出: 0
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个名为 Direction 的枚举，其中列出了 Up、Down、Left 和 Right 四个枚举成员。默认情况下，枚举成员的值从 0 开始自动递增，因此 Direction.Up 的值为 0。我们可以使用枚举成员来声明变量，并进行比较、打印等操作。</font>

### **<font style="color:rgb(25, 27, 31);">4.2. 数字枚举</font>**
<font style="color:rgb(25, 27, 31);">在默认情况下，数字枚举的成员从 0 开始自动递增。</font>

### **<font style="color:rgb(25, 27, 31);">4.2.1. 默认递增的数字枚举</font>**
```plain
typescript复制代码enum Direction {
  Up,
  Down,
  Left,
  Right
}

console.log(Direction.Up);     // 输出: 0
console.log(Direction.Down);   // 输出: 1
console.log(Direction.Left);   // 输出: 2
console.log(Direction.Right);  // 输出: 3
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个名为 Direction 的枚举，其中列出了 Up、Down、Left 和 Right 四个枚举成员。默认情况下，枚举成员的值从 0 开始自动递增，因此 Direction.Up 的值是 0，Direction.Down 的值是 1，Direction.Left 的值是 2，Direction.Right 的值是 3。</font>

### **<font style="color:rgb(25, 27, 31);">4.2.2. 手动赋值的数字枚举</font>**
<font style="color:rgb(25, 27, 31);">在手动赋值的数字枚举中，可以为每个枚举成员手动指定一个特定的值。手动赋值的数字枚举可以使用任意合法的数字作为成员的值。</font>

```plain
typescript复制代码enum Direction {
  Up = 2,
  Down = 4,
  Left = 6,
  Right = 8
}

console.log(Direction.Up);     // 输出: 2
console.log(Direction.Down);   // 输出: 4
console.log(Direction.Left);   // 输出: 6
console.log(Direction.Right);  // 输出: 8
```

<font style="color:rgb(25, 27, 31);">在上述示例中，Direction.Up 被赋值为 2，Direction.Down 被赋值为 4，Direction.Left 被赋值为 6，Direction.Right 被赋值为 8。</font>

### **<font style="color:rgb(25, 27, 31);">4.2.3. 计算成员的数字枚举</font>**
<font style="color:rgb(25, 27, 31);">在数字枚举中，可以使用计算表达式作为成员的值。</font>

```plain
typescript复制代码enum Calculation {
  Addition = 2 + 3,
  Subtraction = 10 - 5,
  Multiplication = 6 * 2,
  Division = 20 / 4
}

console.log(Calculation.Addition);        // 输出: 5
console.log(Calculation.Subtraction);     // 输出: 5
console.log(Calculation.Multiplication);  // 输出: 12
console.log(Calculation.Division);        // 输出: 5
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用加法、减法、乘法和除法运算符来计算成员的值。在编译时，这些计算表达式会被求值为结果值并成为实际的枚举成员的值。</font>

### **<font style="color:rgb(25, 27, 31);">4.3. 常量枚举</font>**
<font style="color:rgb(25, 27, 31);">常量枚举（const enum）是一种特殊类型的枚举，它在编译时被删除，并且只保留枚举成员的值作为常量。常量枚举提供了一种更轻量级的方式来使用枚举，可以用于在编译期间替换枚举成员的值。</font>

### **<font style="color:rgb(25, 27, 31);">4.3.1. 常量枚举的定义</font>**
<font style="color:rgb(25, 27, 31);">在定义常量枚举时，需要使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">const</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字和</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">enum</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字的组合。</font>**<font style="color:rgb(25, 27, 31);">常量枚举不能有计算成员。</font>**

```plain
typescript复制代码const enum Direction {
  Up,
  Down,
  Left,
  Right
}
```

### **<font style="color:rgb(25, 27, 31);">4.3.2. 常量枚举的使用</font>**
```plain
typescript复制代码const enum Direction {
  Up,
  Down,
  Left,
  Right
}

console.log(Direction.Up);     // 输出: 0
console.log(Direction.Down);   // 输出: 1
console.log(Direction.Left);   // 输出: 2
console.log(Direction.Right);  // 输出: 3
```

### **<font style="color:rgb(25, 27, 31);">4.3.3. 常量枚举会在编译阶段被删除</font>**
<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763905759-43796dd6-3a76-4dd7-88ca-9511e5bb8485.png)

<font style="color:rgb(25, 27, 31);">  
</font>

### **<font style="color:rgb(25, 27, 31);">4.4. 字符串枚举</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，字符串枚举是一种特殊类型的枚举，其中每个成员都用字符串字面量进行初始化。</font>

```plain
typescript复制代码enum Direction {
  Up = "UP",
  Down = "DOWN",
  Left = "LEFT",
  Right = "RIGHT",
}

console.log(Direction.Up)     // 输出 UP
console.log(Direction.Down)   // 输出 DOWN
console.log(Direction.Left)   // 输出 LEFT
console.log(Direction.Right)  // 输出 RIGHT
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个名为 Direction 的字符串枚举。其中的成员 Up 使用字符串字面量 "UP" 进行初始化，成员 Down 使用字符串字面量 "DOWN" 进行初始化，成员 Left 使用字符串字面量 "LEFT" 进行初始化，成员 Right 使用字符串字面量 "RIGHT" 进行初始化。我们可以通过直接访问枚举成员来获得其对应的字符串值。</font>

<font style="color:rgb(25, 27, 31);">字符串枚举的特点：</font>

+ <font style="color:rgb(25, 27, 31);">明确的字符串值：每个字符串枚举成员都具有明确的字符串值，可更好地描述其含义和用途。</font>
+ <font style="color:rgb(25, 27, 31);">代码可读性：由于成员的值直接使用字符串字面量，因此代码更加清晰、易读。</font>
+ <font style="color:rgb(25, 27, 31);">保留字符串字面量：使用字符串枚举可以在编译后保留字符串字面量，而不是转换为数值或其他类型。</font>
+ <font style="color:rgb(25, 27, 31);">可用于反向映射：字符串枚举可以支持从枚举值到枚举名的反向映射。</font>

### **<font style="color:rgb(25, 27, 31);">4.5. 外部枚举</font>**
<font style="color:rgb(25, 27, 31);">外部枚举（ambient enum）是一种定义在外部代码（如声明文件）中的枚举。外部枚举通常用于描述已存在的枚举类型的形状，而不是为了创建一个具体的 JavaScript 对象。</font>

**<font style="color:rgb(25, 27, 31);">外部枚举的定义不会在编译时生成任何实际的 JavaScript 代码，它只用于类型检查。</font>**

```plain
typescript复制代码declare enum HttpStatusCode {
   OK = 200,
   BadRequest = 400,
   Unauthorized,
   NotFound = 404
 }
 
 let code: HttpStatusCode = HttpStatusCode.OK;
 console.log(code);                        // 输出: 200
 console.log(HttpStatusCode.BadRequest);   // 输出: 400
 console.log(HttpStatusCode.Unauthorized); // 输出: 401 (自动递增)
 console.log(HttpStatusCode.NotFound);     // 输出: 404
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用 declare 关键字来定义了一个外部枚举 HttpStatusCode。它描述了一些常见的 HTTP 状态码。其中的成员 OK 和 BadRequest 和 NotFound 指定了具体的数值，分别为 200，400 和 404，成员 Unauthorized 没有显式指定值，它会根据前一个成员的值自动递增，因此值为 401。</font>

<font style="color:rgb(25, 27, 31);">在使用外部枚举时，我们可以像使用普通枚举一样，访问它的成员并获得相应的值。在上述示例中，我们将 HttpStatusCode.OK 赋值给变量 code，然后将变量 code 的值打印出来，得到的结果是 200。</font>

<font style="color:rgb(25, 27, 31);">注意：当使用外部枚举时，我们必须使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">declare</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来声明它，以告诉 TypeScript 编译器这是一个外部定义的枚举。此外，外部枚举的定义通常是在一个声明文件中（以 .d.ts 结尾），以便在与现有 JavaScript 库或框架进行交互时提供类型信息。</font>

<font style="color:rgb(25, 27, 31);">总结起来，外部枚举是 TypeScript 中一种在外部代码中定义的枚举，用于描述已存在的枚举类型的形状。外部枚举的定义通常只用于类型检查，并不会生成实际的 JavaScript 代码。它在与现有 JavaScript 库或框架进行交互时提供类型信息。</font>

### **<font style="color:rgb(25, 27, 31);">4.6. 异构枚举</font>**
<font style="color:rgb(25, 27, 31);">异构枚举（heterogeneous enum）是一种允许枚举成员的值具有不同类型的枚举。</font>

<font style="color:rgb(25, 27, 31);">通常情况下，枚举中的成员的值应该是相同类型的。但是异构枚举允许在同一个枚举中使用不同类型的值，包括字符串、数字和其他类型。</font>

```plain
typescript复制代码enum Status {
   Active = 1,
   Pending,
   Inactive = "inactive",
   OnHold = "on hold"
 }
 
 console.log(Status.Active);   // 输出: 1
 console.log(Status.Pending);  // 输出: 2 (自动递增)
 console.log(Status.Inactive); // 输出: "inactive"
 console.log(Status.OnHold);   // 输出: "on hold"
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个名为 Status 的异构枚举。其中的成员 Active 的值是一个数字，值为 1。成员 Pending 没有显式指定值，它的值会根据前一个成员的值自动递增，因此值为 2。成员 Inactive 的值是一个字符串，值为 "inactive"。成员 OnHold 的值是一个字符串，值为 "on hold"。</font>

<font style="color:rgb(25, 27, 31);">在访问异构枚举的成员时，将得到其对应的值。在上述示例中，我们分别打印了每个异构枚举成员的值，并相应地获得了不同类型的结果。</font>

<font style="color:rgb(25, 27, 31);">异构枚举的优势在于允许在一组相关的枚举中使用不同类型的值。这在某些特定情况下可能很有用，例如需要表示不同种类的状态或类型时。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">在异构枚举中，具有数字字面量值的成员会根据前一个成员的值自动递增，而具有字符串字面量值的成员不会自动递增。同时，在异构枚举中，没有初始化值的成员会根据前一个成员的值自动递增。</font>**

### **<font style="color:rgb(25, 27, 31);">4.7. 反向映射</font>**
<font style="color:rgb(25, 27, 31);">反向映射（reverse mapping）是指</font>**<font style="color:rgb(25, 27, 31);">枚举成员不仅可以通过名称访问值，而且可以通过值访问名称。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">这意味着可以根据枚举的值获取到对应的枚举成员名称。</font>

```plain
typescript复制代码enum Direction {
   Up = 1,
   Down,
   Left,
   Right
 }
 
 let rightValue = Direction.Right;
 let rightName = Direction[rightValue];
 
 console.log(rightValue);  // 输出: 4
 console.log(rightName);   // 输出: Right
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个名为 Direction 的枚举，其中的成员分别使用数字进行初始化。我们将 Direction.Right 的值赋给变量 rightValue，然后使用 Direction[rightValue] 获取到对应的枚举成员名称，将结果赋给变量 rightName。</font>

<font style="color:rgb(25, 27, 31);">在打印出变量 rightValue 和 rightName 的值后，我们得到的结果是 4 和 Right。这就是反向映射的效果，根据枚举的值可以获取到对应的枚举成员名称。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">反向映射只在数字枚举中有效，而不适用于字符串枚举。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">字符串枚举的成员值虽然可以是字符串字面量，但在 JavaScript 中无法实现反向映射。</font>

### **<font style="color:rgb(25, 27, 31);">4.8. 运行时的枚举</font>**
<font style="color:rgb(25, 27, 31);">运行时的枚举（runtime enum）是指在 JavaScript 运行时可访问和操作的枚举。</font>

<font style="color:rgb(25, 27, 31);">TypeScript 编译器在编译过程中，会将枚举类型转换为实际的 JavaScript 对象。这些对象在运行时仍然保留了枚举的结构和值，以便能够通过它们来进行运行时的枚举操作。</font>

```plain
typescript复制代码enum Fruit {
  Apple,
  Orange,
  Banana
}

function getFruitName(fruit: Fruit): string {
  switch (fruit) {
    case Fruit.Apple:
      return "Apple";
    case Fruit.Orange:
      return "Orange";
    case Fruit.Banana:
      return "Banana";
    default:
      throw new Error("Invalid fruit");
  }
}

console.log(getFruitName(Fruit.Apple));  // 输出: Apple
console.log(getFruitName(Fruit.Orange)); // 输出: Orange
console.log(getFruitName(Fruit.Banana)); // 输出: Banana
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个名为 Fruit 的枚举，其中包含了三个成员 Apple、Orange 和 Banana。然后我们定义了一个函数 getFruitName，它接受一个 Fruit 类型的参数，根据传入的枚举值返回对应的水果名称。</font>

<font style="color:rgb(25, 27, 31);">通过运行 getFruitName 函数并传入不同的枚举值，我们可以在控制台上看到输出的结果，它们是根据传入的枚举值返回的相应水果名称。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">当使用运行时枚举时，由于枚举的成员值实际上是数字（默认从 0 开始递增），因此进行比较时需要使用严格相等运算符 ===。</font>**

### **<font style="color:rgb(25, 27, 31);">4.9. 联合枚举</font>**
<font style="color:rgb(25, 27, 31);">联合枚举（union enum）是指一个枚举类型可以包含多个不同的枚举成员的组合。每个成员可以具有不同的值和类型。</font>

```plain
typescript复制代码enum Shape {
  Circle = "circle",
  Rectangle = "rectangle",
  Triangle = "triangle"
}

enum Color {
  Red = "red",
  Green = "green",
  Blue = "blue"
}

type ShapeColor = Shape.Circle | Shape.Rectangle | Shape.Triangle | Color.Red | Color.Green | Color.Blue;

function drawShape(shape: ShapeColor) {
  switch (shape) {
    case Shape.Circle:
      console.log("画一个圆形");
      break;
    case Shape.Rectangle:
      console.log("画一个矩形");
      break;
    case Shape.Triangle:
      console.log("画一个三角形");
      break;
    case Color.Red:
      console.log("颜色为红色");
      break;
    case Color.Green:
      console.log("颜色为绿色");
      break;
    case Color.Blue:
      console.log("颜色为蓝色");
      break;
    default:
      throw new Error("Invalid shape or color");
  }
}

drawShape(Shape.Circle); // 输出: 画一个圆形
drawShape(Color.Blue);   // 输出: 颜色为蓝色
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了两个枚举 Shape 和 Color。Shape 枚举表示不同的形状，Color 枚举表示不同的颜色。然后我们定义了一个类型别名 ShapeColor，它是 Shape 枚举成员和 Color 枚举成员的联合。接着，我们定义了一个函数 drawShape，它接受一个 ShapeColor 类型的参数 shape。根据传入的参数值进行不同的分支逻辑处理，并输出相应的消息。通过调用 drawShape 函数并传入不同的值，我们可以根据传入的参数值来绘制不同的形状或填充不同的颜色。</font>

<font style="color:rgb(25, 27, 31);">联合枚举使得我们能够在一个类型中组合多个不同的枚举成员，以表示更复杂的类型。这可以让 TypeScript 的类型系统提供更精确的类型检查和推断，以确保代码的正确性。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">联合枚举的使用是通过定义类型别名或接口来实现的。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">通过将不同枚举成员组合在一起，可以创建复合类型，提供更灵活的数据表示。</font>

## **<font style="color:rgb(25, 27, 31);">5. any类型</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，any 类型表示一个动态类型，它可以接受任何类型的值。使用 any 类型时，TypeScript 编译器将不会对值进行类型检查，允许你在编译期绕过类型系统的限制。</font>

<font style="color:rgb(25, 27, 31);">如果是一个普通类型，在赋值过程中改变类型是不被允许的。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763904978-4bc6d9eb-d472-4924-83d0-9c6ac86c77d1.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">如果是 any 类型，则允许被赋值为任意类型。</font>

```plain
typescript复制代码let x: any = 26;
x = "Echo";
x = true;
x = undefined
x = null
x = []
x = {}
```

<font style="color:rgb(25, 27, 31);">以下两种情况，隐式具有 any 类型：</font>

+ <font style="color:rgb(25, 27, 31);">声明变量不提供类型也不提供默认值。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763905173-d6a980fb-a016-468c-a143-66d278101f1a.png)

<font style="color:rgb(25, 27, 31);">  
</font>

+ <font style="color:rgb(25, 27, 31);">函数参数不加类型。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763905311-5fcda66b-10c6-4176-9117-529aaa64e68c.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">注意：在开发过程中应尽量避免过度使用 any 类型，以充分利用 TypeScript 的类型系统来提供更好的类型安全性和代码可维护性。</font>

## **<font style="color:rgb(25, 27, 31);">五、接口（interface）</font>**
## **<font style="color:rgb(25, 27, 31);">1. 什么是接口</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，接口（Interface）是一种用来定义对象的结构和行为的类型。通过接口，我们可以定义对象应该有哪些属性、属性的类型以及方法。</font>

<font style="color:rgb(25, 27, 31);">接口提供了一种约束和规范，使得我们可以在代码中定义和使用特定的数据结构。</font>

## **<font style="color:rgb(25, 27, 31);">2. 定义接口</font>**
+ <font style="color:rgb(25, 27, 31);">使用关键字</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">interface</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来定义接口。</font>
+ <font style="color:rgb(25, 27, 31);">声明接口后，直接使用接口名称作为变量的类型。</font>
+ <font style="color:rgb(25, 27, 31);">方法的定义和函数的定义类似，包括参数和返回值类型。</font>
+ <font style="color:rgb(25, 27, 31);">接口一般首字母大写。</font>**<font style="color:rgb(25, 27, 31);">有的编程语言中建议接口的名称加上前缀</font>****<font style="color:rgb(25, 27, 31);">I</font>****<font style="color:rgb(25, 27, 31);">。</font>**

```plain
typescript复制代码interface Person {
  name: string
  age: number
  sayHi(): void
}

let jerry: Person = {
  name: 'John',
  age: 25,
  sayHi() {}
}
```

<font style="color:rgb(25, 27, 31);">上面的代码中，我们定义了一个接口 Person，接着定义了一个变量 jerry，它的类型是 Person。这样，我们就约束了 jerry 的形状必须和接口 Person 一致。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">定义的变量比接口少了一些属性不允许的</font>**<font style="color:rgb(25, 27, 31);">。</font>

<font style="color:rgb(25, 27, 31);">下面是一段错误的代码演示：我们定义了一个接口 Person，里面有name，age2个属性，以及sayHi方法，接着定义了一个变量 jerry，它的类型是 Person，但是我们只给属性name和age赋值，所以会报错。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763905680-52913317-632f-4cb0-8520-f68acc7c635f.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">当然，</font>**<font style="color:rgb(25, 27, 31);">定义的变量比接口多了一些属性也是不允许的。</font>**

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763905865-d0df0fa7-88c4-4f2e-94f7-5e4bff12d49b.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">也就是说，</font>**<font style="color:rgb(25, 27, 31);">在赋值的时候，变量的形状必须和接口的形状保持一致</font>**<font style="color:rgb(25, 27, 31);">。</font>

## **<font style="color:rgb(25, 27, 31);">3. 接口（interface）和类型别名（type）的区别</font>**
1. <font style="color:rgb(25, 27, 31);">相同点：都可以用于定义对象的结构和类型。</font>
2. <font style="color:rgb(25, 27, 31);">不同点：</font>
    1. <font style="color:rgb(25, 27, 31);">接口更适合用于描述真实存在的对象，而类型别名更适合用于定义复杂的类型。</font>
    2. <font style="color:rgb(25, 27, 31);">接口可以被其他对象实现，而类型别名只是给类型起了一个别名。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

```plain
typescript复制代码interface Person {
  name: string
  age: number
  sayHi(): void
}

type IPerson = {
  name: string
  age: number
  sayHi(): void
}
```

## **<font style="color:rgb(25, 27, 31);">4. 接口继承（extends）</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，接口是可以相互继承的，也就是说：</font>**<font style="color:rgb(25, 27, 31);">一个接口可以从另一个接口中继承属性和方法的定义（通过继承实现复用）。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">接口的继承可以通过使用关键字</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">extends</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">实现。</font>

<font style="color:rgb(25, 27, 31);">接口继承的语法格式如下：</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763906529-680cd1f5-ae89-4fd1-8ef4-e6db70c8da93.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">通过继承，子接口可以获得父接口中定义的属性和方法，并可以在自身接口中添加新的属性和方法。</font>

<font style="color:rgb(25, 27, 31);">下面是一个简单的例子，展示了接口继承的用法：</font>

```plain
typescript复制代码interface Shape {
  color: string;
}

interface Circle extends Shape {
  radius: number;
  getArea(): number;
}

const circle: Circle = {
  color: "red",
  radius: 5,
  getArea() {
    return Math.PI * this.radius * this.radius;
  }
}
```

<font style="color:rgb(25, 27, 31);">在上面的例子中，使用 extends 关键字实现了接口 Circle 继承 Shape。继承后，Circle 就有了 Shape 中的 color 属性，以及自身的 radius 属性以及 getArea() 方法。</font>

## **<font style="color:rgb(25, 27, 31);">5. 接口的可选属性</font>**
<font style="color:rgb(25, 27, 31);">带有可选属性的接口与普通的接口定义差不多，只是在可选属性名字定义的后面加一个</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">?</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">符号。</font>

```plain
typescript复制代码interface Person {
  name: string;
  age?: number; // 可选属性
}

const person1: Person = { name: "Alice" };
const person2: Person = { name: "Bob", age: 25 };
```

<font style="color:rgb(25, 27, 31);">上面的例子中，Person 接口中的 age 属性是可选的，我们定义了 person1 和 person2 两个对象，类型都是Person，其中，person1 对象中没有 age 属性，而 person2 对象中包含了 age 属性。</font>

<font style="color:rgb(25, 27, 31);">可选属性的好处有2个：</font>

1. <font style="color:rgb(25, 27, 31);">可以对可能存在的属性进行预定义</font>
2. <font style="color:rgb(25, 27, 31);">可以捕获引用了不存在的属性时的错误</font>

<font style="color:rgb(25, 27, 31);">例如，我们故意将 person2 对象中的 age 属性名写错，就会得到一个错误的提示。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763906467-85bda3cf-57a9-46a1-8b5e-bf614cb27b07.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">6. 接口的只读属性</font>**
<font style="color:rgb(25, 27, 31);">有时候我们希望某些属性在对象创建后不能被修改，可以将这些属性声明为</font>**<font style="color:rgb(25, 27, 31);">只读属性</font>**<font style="color:rgb(25, 27, 31);">。</font>

<font style="color:rgb(25, 27, 31);">通过在属性名称前面加上</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">readonly</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字，就可以将属性设置为只读。</font>

<font style="color:rgb(25, 27, 31);">例如，下面的例子中，声明了一个名称为 Point2D 的接口，接口中的属性 x 和 y 都是只读的，然后创建了一个 point 对象，类型为 Point2D，此时，我们不能再给对象中的 x 和 y 重新赋值，会报错，因为它们都是只读属性。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763906548-d0190199-e9be-46ef-8689-380e3e7cbafc.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">此外 TypeScript 还提供了</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">ReadonlyArray</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">类型，它与</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">Array</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">相似，只是把所有可变方法去掉了，因此可以确保数组创建后再也不能被修改。</font>

```plain
typescript复制代码let a: number[] = [1, 2, 3, 4]
let ro: ReadonlyArray<number> = a
ro[0] = 12      // error!
ro.push(5)      // error!
ro.length = 100 // error!
a = ro          // error!
```

## **<font style="color:rgb(25, 27, 31);">7. 额外的属性检查</font>**
<font style="color:rgb(25, 27, 31);">接口用于定义对象的结构，当我们使用</font>**<font style="color:rgb(25, 27, 31);">对象字面量</font>**<font style="color:rgb(25, 27, 31);">赋值给接口类型时，TypeScript 会自动进行额外的属性检查。这意味着</font>**<font style="color:rgb(25, 27, 31);">赋值的对象不能包含接口中未定义的额外属性，否则会导致编译错误。</font>**

```plain
typescript复制代码interface Rectangle {
  width: number;
  height: number;
}

const rect1: Rectangle = { width: 10, height: 20 }
const rect2: Rectangle = { width: 10, height: 20, color: "red" } // 编译错误，额外的属性检查
```

<font style="color:rgb(25, 27, 31);">在上述例子中，rect2 对象包含了额外的 color 属性，但是接口 Rectangle 中并未定义该属性，所以会导致编译错误。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763907657-b1c065bc-bd9c-415b-8577-8e5ec3cfc1ae.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">如果我们确定对象会包含额外的属性，可以使用类型断言（Type Assertion）来绕过额外属性检查。</font>**

## **<font style="color:rgb(25, 27, 31);">8. 接口的任意属性</font>**
<font style="color:rgb(25, 27, 31);">有时候我们希望一个接口中除了包含必选和可选属性之外，还允许有其他的任意属性，这时我们可以使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">索引签名</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">的形式来满足上述要求。</font>

```plain
typescript复制代码interface Person {
  name: string;
  age?: number;
  [propName: string]: any;
}

let person: Person = {
  name: 'Echo',
  gender: 'male'
}
```

<font style="color:rgb(25, 27, 31);">上述代码中，我们使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">[propName: string]</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">定义了任意属性取</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">string</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">类型的值。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">一旦定义了任意属性，那么必选属性和可选属性的类型都必须是它的类型的子集：</font>**

```plain
typescript复制代码interface Person {
  name: string;
  age?: number;
  [propName: string]: string;
}

let person: Person = {
  name: 'Echo',
  age: 25,
  gender: 'male'
}
```

<font style="color:rgb(25, 27, 31);">上述例子中，任意属性的值允许是 string，但是可选属性 age 的值却是 number，number 不是 string 的子属性，所以报错了。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763907529-cdd9f21b-ac79-4324-8bd9-a74c78c2138c.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">一个接口中只能定义一个任意属性。如果接口中有多个类型的属性，则可以在任意属性中使用联合类型。</font>**

```plain
typescript复制代码interface Person {
  name: string;
  age?: number; // 这里age真实的类型应该为：number | undefined
  [propName: string]: string | number | undefined;
}

let person: Person = {
  name: 'Echo',
  age: 25,
  gender: 'male'
}
```

## **<font style="color:rgb(25, 27, 31);">9. 函数类型</font>**
<font style="color:rgb(25, 27, 31);">接口可以描述函数类型。</font>

<font style="color:rgb(25, 27, 31);">为了使用接口表示函数类型，我们需要给接口定义一个调用签名。 它就像是一个只有参数列表和返回值类型的函数定义，参数列表里的每个参数都需要名字和类型。</font>

```plain
typescript复制代码interface SearchFunc {
  (source: string, subString: string): boolean;
}
```

<font style="color:rgb(25, 27, 31);">在上述例子中，SearchFunc 是一个接口，它表示一个接收两个参数 source 和 subString，参数类型都为 string，并且返回值为 number 类型的函数。</font>

<font style="color:rgb(25, 27, 31);">这样定义后，我们可以像使用其它接口一样使用这个函数类型的接口。</font>

<font style="color:rgb(25, 27, 31);">下面的例子展示了如何创建一个函数类型的变量，并将一个同类型的函数赋值给这个变量。</font>

```plain
typescript复制代码interface SearchFunc {
  (source: string, subString: string): boolean;
}

let mySearch: SearchFunc;
mySearch = function(source: string, subString: string) {
  let result = source.search(subString);
  return result > -1;
}
```

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">对于函数类型的类型检查来说，函数的参数名不需要与接口里定义的名字相匹配。</font>**

<font style="color:rgb(25, 27, 31);">例如，我们使用下面的代码重写上面的例子：</font>

```plain
typescript复制代码interface SearchFunc {
  (source: string, subString: string): boolean;
}

let mySearch: SearchFunc;
mySearch = function(src: string, sub: string): boolean {
  let result = src.search(sub);
  return result > -1;
}
```

<font style="color:rgb(25, 27, 31);">函数的参数会逐个进行检查，要求对应位置上的参数类型是兼容的。</font>

<font style="color:rgb(25, 27, 31);">如果你不想指定类型，TypeScript 的类型系统会推断出参数类型，因为函数直接赋值给了 SearchFunc 类型变量。 函数的返回值类型是通过其返回值推断出来的（此例是 false和true）。</font>

```plain
typescript复制代码interface SearchFunc {
  (source: string, subString: string): boolean;
}

let mySearch: SearchFunc;
mySearch = function(src, sub) {
    let result = src.search(sub);
    return result > -1;
}
```

<font style="color:rgb(25, 27, 31);">如果让这个函数返回数字或字符串，类型检查器会警告我们函数的返回值类型与 SearchFunc 接口中的定义不匹配。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763907617-5006a122-82c8-4801-acd1-f1dbfea648bb.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">10. 可索引类型</font>**
<font style="color:rgb(25, 27, 31);">接口可以描述具有索引签名的对象，这样我们就可以通过索引来访问对象的属性。</font>

```plain
typescript复制代码interface StringArray {
  [index: number]: string;
}

let myArray: StringArray;
myArray = ["Bob", "Fred"];

let myStr: string = myArray[0];
```

<font style="color:rgb(25, 27, 31);">上述的例子中，我们定义了 StringArray 接口，它具有索引签名。这个索引签名表示了当用 number 去索引StringArray 时会得到 string 类型的返回值。</font>

<font style="color:rgb(25, 27, 31);">TypeScript 支持两种索引签名：</font>**<font style="color:rgb(25, 27, 31);">字符串和数字。可以同时使用两种类型的索引，但是</font>**<font style="color:rgb(25, 27, 31);">数字索引的返回值必须是字符串索引返回值类型的子类型。 这是因为当使用 number 来索引时，JavaScript 会将它转换成 string 然后再去索引对象。 也就是说用 100（一个number）去索引等同于使用"100"（一个string）去索引，因此两者需要保持一致。</font>

## **<font style="color:rgb(25, 27, 31);">11. 类类型实现接口</font>**
<font style="color:rgb(25, 27, 31);">接口可以被类实现，称为</font>**<font style="color:rgb(25, 27, 31);">类类型</font>**<font style="color:rgb(25, 27, 31);">。</font>

<font style="color:rgb(25, 27, 31);">类可以通过</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">implements</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字来实现接口，并必须实现接口中定义的所有属性和方法。</font>

```plain
typescript复制代码interface Printable {
  print(): void;
}

class Document implements Printable {
  print() {
    console.log("Printing document...");
  }
}
```

<font style="color:rgb(25, 27, 31);">在上述例子中，Document 类实现了 Printable 接口，并实现了接口中定义的 print 方法。</font>

## **<font style="color:rgb(25, 27, 31);">12. 继承接口</font>**
<font style="color:rgb(25, 27, 31);">和类一样，接口也可以相互继承。 这让我们能够从一个接口里复制成员到另一个接口里，可以更灵活地将接口分割到可重用的模块里。</font>

```plain
typescript复制代码interface Shape {
    color: string;
}

interface Square extends Shape {
    sideLength: number;
}

let square = <Square>{};
square.color = "blue";
square.sideLength = 10;
```

<font style="color:rgb(25, 27, 31);">一个接口可以继承多个接口，创建出多个接口的合成接口。</font>

```plain
typescript复制代码interface Shape {
    color: string;
}

interface PenStroke {
    penWidth: number;
}

interface Square extends Shape, PenStroke {
    sideLength: number;
}

let square = <Square>{};
square.color = "blue";
square.sideLength = 10;
square.penWidth = 5.0;
```

## **<font style="color:rgb(25, 27, 31);">13. 接口继承类</font>**
<font style="color:rgb(25, 27, 31);">当接口继承了一个类类型时，它会继承类的成员但不包括其实现。 就好像接口声明了所有类中存在的成员，但并没有提供具体实现一样。 接口同样会继承到类的 private 和 protected 成员。 这意味着当你创建了一个接口继承了一个拥有私有或受保护的成员的类时，这个接口类型只能被这个类或其子类所实现（implement）。</font>

```plain
typescript复制代码class Animal {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  eat() {
    console.log(this.name + " is eating.");
  }
}

interface CanRun extends Animal {
  run(): void;
  eat(): void;
}

class Dog implements CanRun {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  run() {
    console.log(this.name + " is running.");
  }
  eat() {
    console.log(this.name + " is eating.");
  }
}

const dog: CanRun = new Dog("Buddy");
dog.eat(); // 输出：Buddy is eating.
dog.run(); // 输出：Buddy is running.
```

<font style="color:rgb(25, 27, 31);">在以上示例中，我们定义了一个 Animal 类，它有一个 name 属性和一个 eat 方法。然后，我们定义了一个接口 CanRun，它继承自 Animal 类，并添加了一个 run 和 eat 方法。接着，我们创建了一个 Dog 类来实现 CanRun 接口，并在 Dog 类中实现了 run 和 eat 方法。</font>

<font style="color:rgb(25, 27, 31);">在最后的代码中，我们使用 CanRun 接口来声明一个 dog 对象，并将其实例化为 Dog 类的对象。这样，我们可以通过调用 dog 对象的 eat 和 run 方法来验证接口继承类的实现。</font>

**<font style="color:rgb(25, 27, 31);">接口继承类的主要作用在于类型标注和约束。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">通过接口继承类，我们可以定义更具体的接口类型，使得类和接口之间的关系更加清晰。同时，在使用接口类型的变量或参数时，可以享受到类成员的类型检查和智能提示的功能。这对于代码的可读性、可维护性和可扩展性都有很大的帮助。</font>

## **<font style="color:rgb(25, 27, 31);">六、类型别名</font>**
<font style="color:rgb(25, 27, 31);">作用：</font>

<font style="color:rgb(25, 27, 31);">在 TS 中，类型别名主要用于为已有的类型创建别名，以便在代码中更方便地引用和重用这些类型。</font>

<font style="color:rgb(25, 27, 31);">用法：</font>

1. <font style="color:rgb(25, 27, 31);">使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">type</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字可以为任何类型定义别名，包括基本类型、复杂类型、函数类型等。</font>
2. <font style="color:rgb(25, 27, 31);">创建类型别名后，直接使用该类型别名作为变量的类型注解即可。</font>

<font style="color:rgb(25, 27, 31);">解释：</font>

1. <font style="color:rgb(25, 27, 31);">类型别名是为已有类型提供另一个名称，而不是创建新的类型。</font>
2. <font style="color:rgb(25, 27, 31);">类型别名可以用于简化复杂类型的表达，提高可读性和可维护性。</font>
3. <font style="color:rgb(25, 27, 31);">类型别名可以用于定义联合类型或交叉类型的别名。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>

1. <font style="color:rgb(25, 27, 31);">尽量选择有意义的别名，能够准确描述类型的用途，提高代码的可读性。</font>
2. <font style="color:rgb(25, 27, 31);">避免过度使用类型别名，过多的别名可能导致代码的可维护性变差。</font>
3. <font style="color:rgb(25, 27, 31);">注意避免循环引用的情况，即在类型别名中引用自身，这会导致编译错误。</font>
4. <font style="color:rgb(25, 27, 31);">类型别名并不创建新的类型，所以它无法被继承或实现。</font>

```plain
typescript复制代码// 未使用类型别名
let arr: (number | string)[] = [1, 2, 3]
let arr1: (number | string)[] = ['a', 'b', 'c']

// 使用类型别名
type CustomArray = (number | string)[]
let arr2: CustomArray = [1, 2, 3]
let arr3: CustomArray = ['a', 'b', 'c']
let arr4: CustomArray = [1, 'a', 2, 'b', 3, 'c']
```

## **<font style="color:rgb(25, 27, 31);">七、类型推论</font>**
## **<font style="color:rgb(25, 27, 31);">1. 定义</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，类型推论（Type Inference）是指</font>**<font style="color:rgb(25, 27, 31);">编译器在没有明确指定类型的情况下，根据变量的值推断出该变量的类型。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">通过类型推论，TypeScript 可以在代码中自动推断出变量的类型，而无需显式地将其指定为特定类型。</font>

## **<font style="color:rgb(25, 27, 31);">2. 基本类型推论</font>**
<font style="color:rgb(25, 27, 31);">当声明一个变量时，如果没有显式指定类型，并且在声明的同时进行了赋值操作，TypeScript 将根据赋值的值推断出变量的类型。</font>

```plain
typescript复制代码let age = 26;         // 推断为 number 类型
let str = "Echo";    // 推断为 string 类型
let isActive = true; // 推断为 boolean 类型

// 以上的代码等价于下面的下吗
let age: number = 26;
let str: string = "Echo";
let isActive: boolean = true;
```

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763907685-ef02075a-7442-417f-9f80-8a12b4633f99.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">3. 上下文类型推论</font>**
<font style="color:rgb(25, 27, 31);">当变量的类型与其所处的上下文相关时，TypeScript 可以根据上下文进行类型推断。</font>

```plain
typescript复制代码function add(x: number, y: number) {
  return x + y;
}

let result = add(5, 10); // 推断 result 为 number 类型
```

<font style="color:rgb(25, 27, 31);">在上述示例中，函数 add 接收两个参数，并返回它们的和。当我们调用 add(5, 10) 时，TypeScript 根据函数返回值的类型推断出 result 变量的类型为 number。</font>

## **<font style="color:rgb(25, 27, 31);">4. 最佳通用类型推论</font>**
<font style="color:rgb(25, 27, 31);">当需要推断出数组或对象类型时，TypeScript 会根据元素或属性的类型推断出一个“最佳通用类型”。</font>

```plain
typescript复制代码let numbers = [1, 2, 3]; // 推断为 number[] 类型

let mixed = [26, "Echo", true]; // 推断为 (number | string | boolean)[]
```

<font style="color:rgb(25, 27, 31);">在上述示例中，数组 numbers 中的所有元素都是数字，因此 TypeScript 推断出 numbers 的类型为 number[]。而数组 mixed 中的元素类型不同（数字、字符串和布尔值），所以 TypeScript 推断出 mixed 的类型为 (number | string | boolean)[]，表示该数组可以存储数字、字符串或布尔值类型的元素。</font>

## **<font style="color:rgb(25, 27, 31);">5. 声明变量但没有赋值的情况</font>**
<font style="color:rgb(25, 27, 31);">如果声明变量的时候没有赋值，不管之后有没有赋值，都会被推断成</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">any</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">类型而完全不被类型检查。</font>

```plain
typescript复制代码let str

str = "Echo"

str = 26

str = true
```

<font style="color:rgb(25, 27, 31);">在上述示例中，变量 str 的类型推断为 any 类型，因为它没有明确的初始值。此时我们就可以把任意类型的值赋值给 str。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，虽然 TypeScript 可以根据赋值来推断类型，但如果变量的初始值为 null 或 undefined，类型推论仍然会将其推断为 any 类型。</font>

**<font style="color:rgb(25, 27, 31);">为了避免使用 any 类型，我们可以显式指定变量的类型或为变量提供一个初始值来触发类型推论。</font>**

## **<font style="color:rgb(25, 27, 31);">八、类型断言</font>**
## **<font style="color:rgb(25, 27, 31);">1. 定义</font>**
<font style="color:rgb(25, 27, 31);">类型断言（Type Assertion）是 TypeScript 中的一种表达式，它可以用来告诉编译器一个值的确切类型。通过类型断言，我们可以在一些情况下主动指定变量的类型，以满足特定的需求。</font>

## **<font style="color:rgb(25, 27, 31);">2. 语法</font>**
<font style="color:rgb(25, 27, 31);">类型断言有2种语法形式：</font>

1. **<font style="color:rgb(25, 27, 31);">尖括号语法：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">使用尖括号 <> 将值包裹，并在尖括号内指定目标类型。</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);"><类型>值</font>**

```plain
typescript复制代码let value: any = "Hello";
let len: number = (<string>value).length;

console.log(len); // 输出: 5
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，我们将变量 value 的类型断言为 string 类型，然后使用 .length 属性获取字符串的长度。</font>

1. **<font style="color:rgb(25, 27, 31);">as 语法：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">使用 as 关键字，在值后面跟上目标类型。</font>**<font style="color:rgb(25, 27, 31);">值 as 类型</font>**

```plain
typescript复制代码let value: any = "Hello";
let len: number = (value as string).length;

console.log(len); // 输出: 5
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，我们使用 as 关键字将变量 value 的类型断言为 string 类型，并用 length 属性获取字符串的长度。</font>

<font style="color:rgb(25, 27, 31);">以上两种语法虽说没有太大的区别，但是我们</font>**<font style="color:rgb(25, 27, 31);">更推荐使用 as 语法</font>**<font style="color:rgb(25, 27, 31);">。因为尖括号格式会与 react 中 JSX 产生语法冲突。</font>

## **<font style="color:rgb(25, 27, 31);">3. 任何类型可以断言为 any 类型</font>**
<font style="color:rgb(25, 27, 31);">由于 any 类型可以接收任何值，因此任何类型都可以断言为 any 类型。这样的断言并不提供更多的类型检查，因此在使用类型断言时需要谨慎。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763907338-b63208c9-89f5-41cf-9702-ec895b73c3f5.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">上面的例子中，数字类型的变量 foo 上是没有 length 属性的，故 TypeScript 给出了相应的错误提示。</font>

<font style="color:rgb(25, 27, 31);">这种错误提示显然是非常有用的。</font>

<font style="color:rgb(25, 27, 31);">但有的时候，我们非常确定这段代码不会出错，比如下面这个例子：</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763908093-b7ce89e4-02a6-4644-aa6b-2b29e5825524.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">上面的示例中，我们需要将 window 上添加一个属性 bar，但 TypeScript 编译时会报错，提示我们 window 上不存在 属性 bar。</font>

<font style="color:rgb(25, 27, 31);">此时我们可以使用 as any 临时将 window 断言为 any 类型：</font>

```plain
typescript
复制代码(window as any).bar = 1;
```

## **<font style="color:rgb(25, 27, 31);">4. any 类型可以断言为任何类型</font>**
<font style="color:rgb(25, 27, 31);">与上述情况相反，由于 any 类型可以接收任何值，它可以被断言为任何类型。这样的断言会跳过类型检查，因此潜在的类型错误可能发生。</font>

```plain
typescript复制代码let x: any = "Echo";

let y: number = x as number; // 将 any 类型断言为 number 类型
```

## **<font style="color:rgb(25, 27, 31);">5. 联合类型的类型断言</font>**
<font style="color:rgb(25, 27, 31);">当变量具有联合类型时，我们可以通过类型断言将其断言为其中的一个类型，但是必须确保断言的类型是变量实际上可以具备的类型。</font>

```plain
typescript复制代码let value: string | number = "Echo";
let length: number = (value as string).length; // 类型断言为 string 类型
```

## **<font style="color:rgb(25, 27, 31);">6. 类型断言的限制</font>**
### **<font style="color:rgb(25, 27, 31);">6.1. 类型断言不会改变变量的实际类型</font>**
<font style="color:rgb(25, 27, 31);">类型断言只是告诉编译器将一个值视为特定类型，并不会改变该值的实际类型。在运行时，类型断言不会影响变量的值或行为，它只是在编译时起作用。</font>

### **<font style="color:rgb(25, 27, 31);">6.2. 类型断言不能用于基本类型之间的转换</font>**
<font style="color:rgb(25, 27, 31);">TypeScript 的类型断言不能用于将基本类型（如 number、string、boolean）相互转换。因为基本类型具有明确的类型判断和行为，不能将一个基本类型断言为另一个基本类型。</font>

```plain
typescript复制代码let x: number = 5;
let y: string = x as string; // 错误，不能将 number 类型断言为 string 类型
```

### **<font style="color:rgb(25, 27, 31);">6.3. 类型断言不能覆盖类型检查</font>**
<font style="color:rgb(25, 27, 31);">类型断言可以绕过编译器的类型检查，但并不意味着我们可以随意断言任何类型。如果发生类型断言与变量的实际类型不匹配的情况，可能会导致运行时错误。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763908648-f6ba12bd-cd19-4fb7-b2ee-17d3e1f66aec.png)

<font style="color:rgb(25, 27, 31);">  
</font>

### **<font style="color:rgb(25, 27, 31);">6.4. 类型断言不能将 null 或 undefined 断言为其他类型</font>**
<font style="color:rgb(25, 27, 31);">因为 null 和 undefined 可以被赋值给任何类型，将它们断言为其他类型是没有意义的。</font>

```plain
typescript复制代码let x: null = null;

let y: number = x as number; // 错误，不能将 null 断言为 number 类型
```

### **<font style="color:rgb(25, 27, 31);">6.5. 联合类型的类型断言存在类型互相排斥的限制</font>**
<font style="color:rgb(25, 27, 31);">如果将一个变量断言为联合类型中某个类型，那么它必须是该联合类型中的实际类型之一。</font>

```plain
typescript复制代码let value: string | number = "Echo";

let len: number = (value as string).length; // 正确，因为 value 的实际类型可以为 string

let size: number = (value as number).toFixed(2); // 错误，value 的实际类型不是 number
```

## **<font style="color:rgb(25, 27, 31);">7. 双重断言</font>**
<font style="color:rgb(25, 27, 31);">双重断言（Double Assertion），也被称为双重类型断言或连续类型断言，是一种在 TypeScript 中连续使用类型断言的技术。它是将一个值断言为多个类型的一种尝试，尽管这种用法并不被 TypeScript 官方鼓励使用，因为它可能产生不可预测的结果。</font>

<font style="color:rgb(25, 27, 31);">双重断言的形式是使用连续的类型断言操作符</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">as</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">或尖括号</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);"><></font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来表示：</font>

```plain
typescript复制代码let value: any = "Echo";

let len: number = (value as any as string).length;
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们连续使用了两次类型断言，将值 value 先断言为 any 类型，然后再将其断言为 string 类型，并使用 length 属性获取字符串的长度。但是需要注意的是，尽管代码通过了编译，但是这种双重断言的方法并不安全，因为它可以导致类型错误和运行时错误。</font>

<font style="color:rgb(25, 27, 31);">使用双重断言可能会隐藏类型错误，因为类型断言是编译时的操作，而不是运行时。在运行时，双重断言可能会导致意外的类型转换错误，并且编译器无法为此提供任何保护。</font>

<font style="color:rgb(25, 27, 31);">所以，在实际开发中，应尽量避免使用双重断言。如果需要使用多个类型，而无法使用更安全的方法来表示，可以考虑重构代码，使用更合适的类型来处理多种情况，或者使用类型守卫和类型判断等 TypeScript 提供的更安全的技术来处理复杂的类型转换或条件判断。</font>

## **<font style="color:rgb(25, 27, 31);">8. 类型断言VS类型转换</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，</font>**<font style="color:rgb(25, 27, 31);">类型断言（Type Assertion）</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">是一种在编译时告诉编译器一个值的确切类型的方式，它只是一种类型的声明，不会对变量进行真正的类型转换。</font>

<font style="color:rgb(25, 27, 31);">与类型断言相对的是</font>**<font style="color:rgb(25, 27, 31);">类型转换（Type Casting）</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">，它是将一个值从一种类型转换为另一种类型的实际操作，而不仅仅是告诉编译器某个值的类型。类型转换通常需要在运行时进行，并涉及对值的实际修改。</font>

```plain
typescript复制代码// 类型断言
let value: any = "Echo";
let len: number = (value as string).length;

// 类型转换
let numberValue: any = "26";
let intValue: number = parseInt(numberValue);
```

<font style="color:rgb(25, 27, 31);">在上述示例中，(value as string) 是一种类型断言，告诉编译器将变量 value 视为字符串类型。而 parseInt 是一种类型转换，将字符串类型的 numberValue 转换为整数类型。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，</font>**<font style="color:rgb(25, 27, 31);">类型断言只会在编译时起作用，不会对变量进行实际的类型转换。而类型转换涉及到对变量值的修改，通常发生在运行时。</font>**

<font style="color:rgb(25, 27, 31);">尽管类型断言和类型转换在某种程度上可以实现相似的效果，但它们的机制和目的不同。类型断言是为了辅助编译器进行类型推断和类型检查的工具，而类型转换是为了实际修改变量的类型以满足特定需求。因此，在使用类型转换时，需要注意潜在的类型错误和运行时错误，并谨慎处理类型转换的结果。</font>

## **<font style="color:rgb(25, 27, 31);">9. 类型断言VS类型声明</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，</font>**<font style="color:rgb(25, 27, 31);">类型断言（Type Assertion）</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">是一种在编译时告诉编译器一个值的确切类型的方式，它是开发者主动指定一个变量的类型，并告诉编译器遵循这个类型进行类型检查。通过类型断言，我们可以在某些情况下绕过编译器的类型检查，但这需要开发者对类型的准确性负责，并且存在潜在的类型错误的风险。</font>

```plain
typescript复制代码let value: any = "Echo";
 
 let len: number = (value as string).length;
```

<font style="color:rgb(25, 27, 31);">在上述示例中，(value as string) 是一种类型断言，将变量 value 的类型断言为字符串类型，从而可以安全地访问字符串的 length 属性。</font>

**<font style="color:rgb(25, 27, 31);">类型声明（Type Declaration）</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">是一种为变量、参数、返回值等明确指定类型的语法，它是用来定义变量的类型，并告诉编译器如何对变量进行类型推断和类型检查。类型声明通常出现在变量声明、函数声明、函数参数、函数返回值等地方，例如：</font>

```plain
typescript复制代码let value: string = "Echo";
 
 function greet(name: string): void {
   console.log("Hello, " + name);
 }
```

<font style="color:rgb(25, 27, 31);">在上述示例中，value: string 是对变量 value 进行类型声明，指定其类型为字符串。而 name: string 是对函数参数 name 进行类型声明，指定其类型为字符串。这样可以确保编译器在类型检查时能够发现潜在的类型错误。</font>

<font style="color:rgb(25, 27, 31);">类型声明是 TypeScript 中一种重要的类型系统的特性，它提供了对变量类型的明确说明，使开发者能够编写更加安全和可维护的代码。与类型断言相比，类型声明更加强制，能够更好地帮助开发者在编译时发现类型错误，并提供更好的类型推断和类型检查支持。</font>

## **<font style="color:rgb(25, 27, 31);">10. 类型断言和泛型</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，</font>**<font style="color:rgb(25, 27, 31);">类型断言（Type Assertion）</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">是一种在编译时告诉编译器一个值的确切类型的方式，它是开发者主动指定一个变量的类型，并告诉编译器遵循这个类型进行类型检查。通过类型断言，我们可以在某些情况下绕过编译器的类型检查，但这需要开发者对类型的准确性负责，并且存在潜在的类型错误的风险。</font>

```plain
typescript复制代码let value: any = "Echo";
 
 let len: number = (value as string).length;
```

<font style="color:rgb(25, 27, 31);">在上述示例中，(value as string) 是一种类型断言，将变量 value 的类型断言为字符串类型，以便可以安全地访问字符串的 length 属性。</font>

<font style="color:rgb(25, 27, 31);">泛型是一种在定义函数、类或接口时使用类型参数来表示灵活的类型的方式。通过泛型，我们可以在定义时不指定具体类型，而是在使用时根据上下文传入具体的类型。它可以增加代码的重用性和灵活性。例如：</font>

```plain
typescript复制代码function toArray<T>(value: T): T[] {
  return [value];
}

let array: string[] = toArray("Hello");
```

<font style="color:rgb(25, 27, 31);">在上述示例中，toArray 是一个泛型函数，使用类型参数 T 来表示数组中的元素类型。通过传入具体的类型 "Hello"，我们可以创建一个字符串类型的数组。</font>

<font style="color:rgb(25, 27, 31);">类型断言和泛型实际上可以一起使用。当我们在处理泛型类型时，有时可能需要对类型进行断言以满足特定的需求。例如：</font>

```plain
typescript复制代码function convertToString<T>(value: T): string {
  return value as unknown as string;
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，通过连续使用类型断言，我们将泛型类型 T 先断言为 unknown 类型，然后再断言为字符串类型，将参数 value 转换为字符串类型并返回。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，在使用类型断言和泛型时，我们要确保类型的安全性和正确性，并避免潜在的类型错误。类型断言可以帮助我们处理一些特殊情况，但要谨慎使用，并确保断言的类型与变量的实际类型相符。泛型则是一种更加灵活和通用的方式来处理不特定类型的代码逻辑。</font>

## **<font style="color:rgb(25, 27, 31);">九、类（class）</font>**
## **<font style="color:rgb(25, 27, 31);">1. 类的定义</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，可以使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">class</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字来定义类。类的定义通常包括成员变量、构造函数、方法等。</font>

## **<font style="color:rgb(25, 27, 31);">2. 类的基本使用</font>**
<font style="color:rgb(25, 27, 31);">类的基本使用主要有以下几个步骤：</font>

1. **<font style="color:rgb(25, 27, 31);">定义类及成员变量：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">class</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字定义一个类，并在类中声明成员变量。</font>
2. **<font style="color:rgb(25, 27, 31);">构造函数：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">constructor</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">方法定义构造函数，用于在创建类的实例时初始化对象的属性。</font>
3. **<font style="color:rgb(25, 27, 31);">方法：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">在类中定义方法，可通过类的实例调用。</font>
4. **<font style="color:rgb(25, 27, 31);">创建类的实例：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">new</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字创建类的实例，并传递构造函数所需的参数。</font>
5. **<font style="color:rgb(25, 27, 31);">访问成员变量和调用方法：</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">通过实例对象访问成员变量和调用方法。</font>

```plain
typescript复制代码class Person {
   name: string;
   age: number;
 
   constructor(name: string, age: number) {
     this.name = name;
     this.age = age;
   }
 
   sayHello(): void {
     console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
   }
 }
 
 const p = new Person("Echo", 26);
 console.log(p.name); // 输出：Echo
 console.log(p.age);  // 输出：26
 p.sayHello();        // 输出：Hello, my name is Echo and I'm 26 years old.
```

<font style="color:rgb(25, 27, 31);">在上述示例中：我们使用 class 关键字定义一个名为 Person 的类，并在 Person 类中声明了两个成员变量：name 和 age。接着，我们使用 constructor 方法定义一个构造函数，用于在创建类的实例时初始化对象的属性，构造函数参数 name 和 age 分别用于接收传入的 name 和 age 值，并将其赋给对应的成员变量。然后定义了一个名为 sayHello 的方法，用于打印一个问候语，并使用成员变量 name 和 age。接着，我们使用 new 关键字创建一个 Person 实例 p，然后打印出 name 和 age 的值以及调用 sayHello 方法。</font>

## **<font style="color:rgb(25, 27, 31);">3. 类的构造函数</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 类中，构造函数是一种特殊的方法，用于在创建类的实例时进行初始化操作。构造函数使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">constructor</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字来定义，可以接收参数，并在创建对象时调用。</font>

### **<font style="color:rgb(25, 27, 31);">3.1. 构造函数的基本语法</font>**
```plain
javascript复制代码class ClassName {
   constructor(parameter1: Type1, parameter2: Type2, ...) {
     // 书写构造函数的逻辑
   }
 }
```

<font style="color:rgb(25, 27, 31);">在上面的代码中，ClassName 是类的名称，parameter1、parameter2 等表示构造函数的参数名，Type1、Type2 等表示参数的类型。</font>

### **<font style="color:rgb(25, 27, 31);">3.2. 使用构造函数初始化成员变量</font>**
<font style="color:rgb(25, 27, 31);">构造函数可以用来初始化类中的成员变量，通过接收构造函数的参数，并将其赋给对应的成员变量。成员变量的声明通常放在类的顶部，而初始化则在构造函数中进行。</font>

```plain
typescript复制代码class Person {
  name: string;
  age: number;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，构造函数接收 name 和 age 作为参数，并将参数的值分别赋给类中的 name 和 age 成员变量。</font>

### **<font style="color:rgb(25, 27, 31);">3.3. 创建类的实例并调用构造函数</font>**
<font style="color:rgb(25, 27, 31);">使用 new 关键字创建类的实例时，构造函数会被自动调用，让我们可以在创建实例的同时进行初始化操作。</font>

```plain
ini
复制代码const person = new Person('Echo', 26);
```

<font style="color:rgb(25, 27, 31);">在上述代码中，我们创建了一个 Person 类的实例 person，并传递了 'Echo' 和 26 作为构造函数的参数。构造函数会将这些参数的值分别赋给 person 实例的 name 和age 成员变量。</font>

### **<font style="color:rgb(25, 27, 31);">3.4. 构造函数的可选参数和默认值</font>**
<font style="color:rgb(25, 27, 31);">构造函数的参数可以设置为可选的，并且可以为参数提供默认值。</font>

<font style="color:rgb(25, 27, 31);">可选参数使用问号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">?</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）修饰符进行标记，而默认值则使用等号（</font>**<font style="color:rgb(25, 27, 31);">=</font>**<font style="color:rgb(25, 27, 31);">）进行赋值。</font>

```plain
typescript复制代码class Person {
  name: string;
  age: number;

  constructor(name: string = 'Echo', age?: number) {
    this.name = name;
    this.age = age;
  }
}

// 创建 person 实例，但不传递 name 和 age 参数
const person = new Person();
console.log(person.name); // 输出：Echo
console.log(person.age);  // 输出：undefined

// 创建 person1 实例，只传递 name 参数
const person1 = new Person('Jee');
console.log(person1.name); // 输出：Jee
console.log(person1.age);  // 输出：undefined

// 创建 person2 实例，同时传递 name 和 age 参数
const person2 = new Person('James', 35);
console.log(person2.name); // 输出：James
console.log(person2.age);  // 输出：35
```

<font style="color:rgb(25, 27, 31);">在上述示例中，name 参数具有一个默认值 'Echo'，而 age 参数则是可选的。如果在创建实例时不传 name 和 age 参数，那么 name 会输出默认值 'Echo'，而 age 会被设置为 undefined，如果在创建实例时只传递了 name 参数，而没有传递 age 参数，那么 age 也会被设置为 undefined。</font>

### **<font style="color:rgb(25, 27, 31);">3.5 .调用其他构造函数（构造函数重载）</font>**
<font style="color:rgb(25, 27, 31);">在一个类中，可以定义多个构造函数，并通过不同的参数配置来进行重载。重载的构造函数之间可以相互调用，使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">this</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字来引用当前类的实例。</font>

<font style="color:rgb(25, 27, 31);">构造函数重载需要定义多个具有不同参数类型和数量的构造函数签名。构造函数签名是指构造函数名称和参数列表，通过这些不同的签名来区分不同的构造函数。</font>

```php
php复制代码class ClassName {
  constructor(parameter1: Type1);
  constructor(parameter1: Type1, parameter2: Type2);
  constructor(parameter1: Type1, parameter2: Type2, parameter3: Type3);
  // ...
  constructor(parameter1: Type1, parameter2: Type2, parameter3: Type3, ...) {
    // 书写构造函数实现的逻辑
  }
}
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，我们定义了三个构造函数签名，每个签名有不同的参数类型和数量，以提供不同的构造函数选项。</font>

```plain
typescript复制代码class Person {
  name: string;
  age: number;

  constructor(name: string);
  constructor(name: string, age: number);
  constructor(name: string, age?: number) {
    this.name = name;
    if (age) {
      this.age = age;
    } else {
      this.age = 0;
    }
  }
}

const person1 = new Person('Echo');
const person2 = new Person('Echo', 26);

console.log(person1.name, person1.age); // 输出：Echo 0
console.log(person2.name, person2.age); // 输出：Echo 26
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了两个构造函数签名，第一个构造函数接收一个 name 参数，第二个构造函数接收一个 name 和一个 age 参数。在构造函数的实现中，根据传递的参数情况，决定是否给 age 成员变量赋值。接着，我们创建了两个实例 person1 和 person2，第一次实例化传递了一个 name 参数，调用了第一个构造函数。第二次实例化传递了一个 name 参数和一个 age 参数，调用了第二个构造函数。</font>

<font style="color:rgb(25, 27, 31);">注意：</font>

+ <font style="color:rgb(25, 27, 31);">成员初始化（比如 name: string）后，才可以通过 this.name 来访问实例成员。</font>
+ <font style="color:rgb(25, 27, 31);">需要为构造函数指定类型注解，否则会被隐式推断为 any 类型，构造函数不需要返回值类型。</font>

## **<font style="color:rgb(25, 27, 31);">4. 类的实例方法</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 类中，实例方法是定义在类中的成员方法，用于操作和访问类的实例属性，并执行特定的操作。实例方法可以通过类的实例来调用，用于对特定实例进行特定操作。</font>

### **<font style="color:rgb(25, 27, 31);">4.1. 定义实例方法</font>**
<font style="color:rgb(25, 27, 31);">实例方法是通过在类中定义普通函数来创建的。语法格式如下：</font>

```php
php复制代码class ClassName {
  methodName(parameter1: Type1, parameter2: Type2): ReturnType {
    // 书写方法的实现逻辑
  }
}
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，methodName 是实例方法的名称，parameter1 和 parameter2 是方法的参数，Type1 和 Type2 是参数的类型，ReturnType 是方法的返回类型。</font>

### **<font style="color:rgb(25, 27, 31);">4.2. 访问实例属性</font>**
<font style="color:rgb(25, 27, 31);">实例方法可以通过使用 this 关键字直接访问类的实例属性。</font>

```plain
typescript复制代码class Person {
  name: string;
  age: number;

	constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }

  sayHello(): void {
    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
  }
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，sayHello 是一个实例方法，它访问了 Person 类的 name 和 age 属性，并在控制台打印出相应的消息。</font>

### **<font style="color:rgb(25, 27, 31);">4.3. 调用实例方法</font>**
<font style="color:rgb(25, 27, 31);">实例方法必须通过类的实例来调用。</font>

```plain
ini复制代码const person = new Person("Echo", 26);
person.sayHello(); // 输出：Hello, my name is Echo and I'm 26 years old.
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们首先创建了一个 Person 类的实例 person，然后使用 person 实例来调用 sayHello 方法。</font>

## **<font style="color:rgb(25, 27, 31);">5. 类的继承</font>**
<font style="color:rgb(25, 27, 31);">类的继承有2种方式：</font>

1. <font style="color:rgb(25, 27, 31);">extends（继承父类）</font>
2. <font style="color:rgb(25, 27, 31);">implements（实现接口）</font>

<font style="color:rgb(25, 27, 31);">说明：JS 中只有 extends，而 implements 是 TS 提供的。</font>

### **<font style="color:rgb(25, 27, 31);">5.1. extends（继承父类）</font>**
<font style="color:rgb(25, 27, 31);">当一个类继承另一个类时，它会继承父类的属性和方法，并可以通过重载或添加新的属性和方法来扩展父类。继承使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">extends</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字来建立类之间的关系。</font>

### **<font style="color:rgb(25, 27, 31);">5.1.1. 定义父类和子类</font>**
<font style="color:rgb(25, 27, 31);">父类是被继承的类，子类是继承父类的类。</font>

```scala
scala复制代码class ParentClass {
  // 书写父类的属性和方法
}

class ChildClass extends ParentClass {
  // 书写子类特有的属性和方法
}
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，ParentClass 是父类，ChildClass 是子类，ChildClass 继承了 ParentClass 的属性和方法。</font>

### **<font style="color:rgb(25, 27, 31);">5.1.2. 继承父类的属性和方法</font>**
<font style="color:rgb(25, 27, 31);">使用</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">extends</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字来建立子类对父类的继承关系。子类会继承父类的公共成员（属性和方法）。子类可以直接访问和使用继承来的属性和方法。</font>

```plain
typescript复制代码class Animal {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  move(distance: number): void {
    console.log(`${this.name} moved ${distance} meters.`);
  }
}

class Dog extends Animal {
  bark(): void {
    console.log("Woof! Woof!");
  }
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，Animal 是父类，其中包含了 name 属性和 move 方法。Dog 是子类，使用 extends Animal 建立了继承关系。Dog 继承了 Animal 的属性和方法，并且定义了自己的 bark 方法。</font>

### **<font style="color:rgb(25, 27, 31);">5.1.3. 调用继承的属性和方法</font>**
<font style="color:rgb(25, 27, 31);">子类可以直接调用继承来的父类属性和方法，也可以访问自己定义的属性和方法。</font>

```plain
arduino复制代码const dog = new Dog("Hate");
dog.move(10);   // 调用继承来自父类的方法 输出：Hate moved 10 meters.
dog.bark();     // 调用子类自己定义的方法 输出：Woof! Woof!
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们首先创建了一个 Dog 类的实例 dog。我们可以通过 dog 实例调用继承自父类的 move 方法，也可以调用子类自己定义的 bark 方法。</font>

### **<font style="color:rgb(25, 27, 31);">5.2. implements（实现接口）</font>**
<font style="color:rgb(25, 27, 31);">接口的实现是以类为基础的，类可以通过</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">implements</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字实现一个或多个接口。通过实现接口，类必须提供接口中定义的所有属性和方法的具体实现。</font>

### **<font style="color:rgb(25, 27, 31);">5.2.1. 定义接口</font>**
<font style="color:rgb(25, 27, 31);">接口是一种抽象的类型，定义了一组属性和方法的规范。接口在定义时不包含具体的实现，而是描述了类应具备的特定行为和功能。</font>

```kotlin
kotlin复制代码interface InterfaceName {
  // 书写接口的属性和方法
}
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，InterfaceName 是一个接口，用于定义属性和方法的规范。</font>

### **<font style="color:rgb(25, 27, 31);">5.2.2. 使用 implements 实现接口</font>**
<font style="color:rgb(25, 27, 31);">使用 implements 关键字来实现接口，使得类能够满足接口定义的规范。通过实现接口，类必须提供接口中定义的所有属性和方法的具体实现。</font>

```java
java复制代码class ClassName implements InterfaceName {
  // 书写类的属性和方法的具体实现
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，ClassName 是一个类，通过 implements InterfaceName 实现了接口 InterfaceName，从而满足了接口定义的规范。</font>

### **<font style="color:rgb(25, 27, 31);">5.2.3. 实现接口的属性和方法</font>**
<font style="color:rgb(25, 27, 31);">实现接口的类必须包含接口中定义的所有属性和方法，并提供它们的具体实现。</font>

```plain
typescript复制代码interface Shape {
  color: string;
  getArea(): number;
}

class Circle implements Shape {
  radius: number;
  color: string;

  constructor(radius: number, color: string) {
    this.radius = radius;
    this.color = color;
  }

  getArea(): number {
    return Math.PI * this.radius * this.radius;
  }
}

const circle = new Circle(10, 'blue');
const area = circle.getArea();
console.log(area); // 输出：314.1592653589793
```

<font style="color:rgb(25, 27, 31);">在上面的示例中，Shape 是一个接口，定义了属性 color 和方法 getArea()。Circle 类通过 implements Shape 实现了接口 Shape，并提供了接口中定义的属性和方法的具体实现。</font>

## **<font style="color:rgb(25, 27, 31);">6. 类的修饰符</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 中，类的修饰符用于控制类的成员（属性和方法）的可见性和访问权限。</font>

<font style="color:rgb(25, 27, 31);">类的修饰符包括：</font>

1. <font style="color:rgb(25, 27, 31);">public（公有的），可以在任何地方被访问到，默认所有的属性和方法都是 public 的。</font>
2. <font style="color:rgb(25, 27, 31);">privete（私有的），不能在声明它的类的外部访问。</font>
3. <font style="color:rgb(25, 27, 31);">protected（受保护的），和 private 类似，区别是它在子类中也是允许被访问的。</font>

### **<font style="color:rgb(25, 27, 31);">6.1. public</font>**
<font style="color:rgb(25, 27, 31);">public 关键字是默认的访问修饰符，如果不指定修饰符，默认为 public。公共成员在类的内部和外部都是可见的，并且可以随时访问。</font>

```plain
typescript复制代码class Person {
  public name: string;
  public age: number;

  public constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }

  public sayHello(): void {
    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
  }
}

const person = new Person("Echo", 26);
console.log(person.name); // 输出：ECho
person.sayHello();        // 输出：Hello, my name is Echo and I'm 26 years old.
person.name = "James";
console.log(person.name); // 输出：James
```

<font style="color:rgb(25, 27, 31);">在上述示例中，name、age 和 sayHello() 都是公共成员，可以在类的内部和外部进行访问。</font>

### **<font style="color:rgb(25, 27, 31);">6.2. private</font>**
<font style="color:rgb(25, 27, 31);">private 关键字修饰符限制成员的访问范围仅在类的内部。私有成员在类的外部不可见，只能在类的内部进行访问。</font>

```plain
typescript复制代码class Person {
  private name: string;

  constructor(name: string) {
    this.name = name;
  }

  public sayHello(): void {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

const person = new Person("Echo");
person.sayHello();        // 输出：Hello, my name is Echo.
console.log(person.name); // 报错：属性“name”为私有属性，只能在类“Person”中访问
```

<font style="color:rgb(25, 27, 31);">在上述示例中，成员 name 是私有成员，只能在类的内部进行访问，外部访问会报错。</font>

**<font style="color:rgb(25, 27, 31);">注意：1. 使用 private 修饰的属性或方法，在子类中也是不允许访问的。</font>**

```scala
scala复制代码class Animal {
  private name: string;
  public constructor(name: string) {
    this.name = name;
  }
}

class Dog extends Animal {
  constructor(name: string) {
    super(name);
    console.log(this.name); // 报错：属性“name”为私有属性，只能在类“Animal”中访问
  }
}
```

**<font style="color:rgb(25, 27, 31);">注意：2. 当构造函数修饰为 private 时，该类不允许被继承或者实例化。</font>**

```scala
scala复制代码class Animal {
  public name: string;
  private constructor(name: string) {
    this.name = name;
  }
}
class Dog extends Animal { // 报错：无法扩展类“Animal”，类构造函数标记为私有
  constructor(name: string) {
    super(name);
  }
}

const dog = new Animal('Hate'); // 报错：类“Animal”的构造函数是私有的，仅可在类声明中访问。
```

### **<font style="color:rgb(25, 27, 31);">6.3. protected</font>**
<font style="color:rgb(25, 27, 31);">protected 关键字修饰符限制成员的访问范围在类的内部及其派生类中。受保护成员在类的外部不可见，但可以在类的内部和派生类中进行访问。</font>

```plain
typescript复制代码class Animal {
  protected name: string;
  public constructor(name: string) {
    this.name = name;
  }
}

class Dog extends Animal {
  constructor(name: string) {
    super(name);
    console.log(this.name); // 输出：Hate
  }
}

const dog = new Dog('Hate');
```

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">当构造函数修饰为 protected 时，该类只允许被继承。</font>**

```scala
scala复制代码class Animal {
  public name: string;
  protected constructor(name: string) {
    this.name = name;
  }
}
class Dog extends Animal {
  constructor(name: string) {
    super(name);
  }
}

const dog = new Animal('Hate'); // 报错：类“Animal”的构造函数是受保护的，仅可在类声明中访问
```

### **<font style="color:rgb(25, 27, 31);">6.4. readonly</font>**
<font style="color:rgb(25, 27, 31);">readonly 是一个只读属性关键字，只允许出现在属性声明或索引签名或构造函数中。</font>

```plain
typescript复制代码class Person {
  readonly name: string;
  constructor(name: string) {
    this.name = name;
  }
}

let person = new Person('Echo');
console.log(person.name); // 输出：Echo
person.name = 'James';    // 报错：无法为“name”赋值，因为它是只读属性
```

<font style="color:rgb(25, 27, 31);">注意：</font>**<font style="color:rgb(25, 27, 31);">如果 readonly 和其他访问修饰符同时存在的话，需要写在其后面。</font>**

```plain
typescript复制代码class Person {
  // public readonly name: string;
  public constructor(public readonly name: string) {
    this.name = name;
  }
}
```

<font style="color:rgb(25, 27, 31);">readonly 只读属性特点：</font>

+ <font style="color:rgb(25, 27, 31);">只读属性必须在声明时或索引签名或构造函数内进行初始化赋值。</font>
+ <font style="color:rgb(25, 27, 31);">只读属性不能被重新赋值或修改，否则会报错。</font>
+ **<font style="color:rgb(25, 27, 31);">只能修饰属性，不能修饰方法。</font>**

<font style="color:rgb(25, 27, 31);">只读属性和常量的区别：</font>

+ <font style="color:rgb(25, 27, 31);">只读属性是 TypeScript 提供的一种语法，用于将类的属性标记为只读，并且只有在类的内部可以修改其值。</font>
+ <font style="color:rgb(25, 27, 31);">常量通常是通过 const 关键字声明的，在任何地方都无法修改其值，包括类的内部。</font>

### **<font style="color:rgb(25, 27, 31);">6.5. 参数属性</font>**
<font style="color:rgb(25, 27, 31);">参数属性是一种简化代码的</font>[<font style="color:rgb(9, 64, 142);">语法糖</font>](https://zhida.zhihu.com/search?content_id=234903611&content_type=Article&match_order=1&q=%E8%AF%AD%E6%B3%95%E7%B3%96&zhida_source=entity)<font style="color:rgb(25, 27, 31);">，用于在构造函数中同时声明和初始化类的成员属性。使用参数属性可以在一个地方完成属性的声明和赋值，减少了重复的代码。</font>

```plain
typescript复制代码class Person {
  constructor(public name: string, private age: number, protected sex: string, public readonly height: number) {
    this.name = name;
    this.age = age;
    this.sex = sex;
    this.height = height;
  }
}

const person = new Person('Echo', 26, 'male', 1.7);
console.log(person.name);   // 输出：Echo
console.log(person.age);    // 报错：属性“age”为私有属性，只能在类“Person”中访问
console.log(person.sex);    // 报错：属性“sex”受保护，只能在类“Person”及其子类中访问
console.log(person.height); // 输出：1.7
```

<font style="color:rgb(25, 27, 31);">在上述示例中，定义了一个名为 Person 的类，类里面定义了一个 constructor 构造方法，其中参数 name 是公共属性，可以在类的内部和外部访问；参数 age 是私有属性，只能在类 Person 中访问；参数 sex 是受保护属性，只能在类 Person 及其子类中访问；参数 height 是只读属性，类的外部无法修改其值。</font>

## **<font style="color:rgb(25, 27, 31);">7. 抽象类</font>**
<font style="color:rgb(25, 27, 31);">使用关键字</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">abstract</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">用于定义抽象类和其中的</font>[<font style="color:rgb(9, 64, 142);">抽象方法</font>](https://zhida.zhihu.com/search?content_id=234903611&content_type=Article&match_order=1&q=%E6%8A%BD%E8%B1%A1%E6%96%B9%E6%B3%95&zhida_source=entity)<font style="color:rgb(25, 27, 31);">。</font>

<font style="color:rgb(25, 27, 31);">抽象类是一种不能直接实例化的类，它主要用作其他类的基类。抽象类可以包含抽象方法和具体方法的定义，供子类继承和实现。</font>

### **<font style="color:rgb(25, 27, 31);">7.1. 语法</font>**
```csharp
csharp复制代码abstract class AbstractClass {
  abstract method(): void; // 抽象方法

  concreteMethod(): void {
    console.log("This is a concrete method"); // 具体方法
  }
}
```

<font style="color:rgb(25, 27, 31);">在上述示例中，AbstractClass 是一个抽象类，它包含了一个抽象方法 method() 和一个具体方法 concreteMethod()。</font>

### **<font style="color:rgb(25, 27, 31);">7.2. 抽象方法</font>**
<font style="color:rgb(25, 27, 31);">抽象方法是在抽象类中声明但没有具体实现的方法。它只包含方法的签名，没有方法体，</font>**<font style="color:rgb(25, 27, 31);">子类必须实现抽象方法。</font>**

```scala
scala复制代码abstract class Animal {
  constructor(public name: string) {
    this.name = name;
  }
  abstract sayHi();
}

class Cat extends Animal {
  sayHi() {
    console.log(this.name); // 输出：Tom
  }
}

let cat = new Cat('Tom');
cat.sayHi();
```

<font style="color:rgb(25, 27, 31);">在上述示例中，抽象类 Animal 中的 sayHi() 是一个抽象方法，子类 Cat 继承了 父类 Animal 并实现了抽象方法。</font>

### **<font style="color:rgb(25, 27, 31);">7.3. 抽象类不能被实例化，只能被继承</font>**
<font style="color:rgb(25, 27, 31);">抽象类不能被实例化，只能被继承。</font>

```csharp
csharp复制代码abstract class Animal {
  constructor(public name: string) {
    this.name = name;
  }
  abstract sayHi();
}

let cat = new Animal('Tom'); // 报错：无法创建抽象类的实例
```

### **<font style="color:rgb(25, 27, 31);">7.4. 特点</font>**
+ <font style="color:rgb(25, 27, 31);">抽象类不能被实例化，只能被继承。</font>
+ <font style="color:rgb(25, 27, 31);">抽象类可以包含抽象方法和具体方法的定义。</font>
+ <font style="color:rgb(25, 27, 31);">子类必须实现抽象类中的所有抽象方法，否则子类也必须声明为抽象类。</font>
+ <font style="color:rgb(25, 27, 31);">如果一个类继承了一个抽象类，那么它必须实现抽象类中的抽象方法，除非它自身也声明为抽象类。</font>
+ <font style="color:rgb(25, 27, 31);">抽象类可以作为其他类的基类，用于提供共享的属性和方法定义。</font>

## **<font style="color:rgb(25, 27, 31);">十、类型兼容性</font>**
<font style="color:rgb(25, 27, 31);">类型兼容性是指在 TS 中，如何判断一个类型是否能够赋值给另一个类型。</font>

## **<font style="color:rgb(25, 27, 31);">1. 基本类型的兼容性</font>**
### **<font style="color:rgb(25, 27, 31);">1.1. 相同的基本类型可以互相赋值</font>**
<font style="color:rgb(25, 27, 31);">当你声明一个变量并为其赋予一个特定类型的值时，TypeScript 会根据类型注解进行类型检查和推断。如果变量的类型与给定的值的类型完全匹配，那么它们可以互相赋值。</font>

```plain
ini复制代码let a: number = 10;
let b: number = a;
console.log(a, b); // 输出 10, 10
```

<font style="color:rgb(25, 27, 31);">在上述示例中，变量 a 被声明为 number 类型，并且被赋值为 10。 然后将变量 a 赋值给变量 b，因为 a 和 b 的类型相同，都是 number，所以赋值是允许的。</font>

### **<font style="color:rgb(25, 27, 31);">1.2. 数字字面量类型可以赋值给数值类型</font>**
<font style="color:rgb(25, 27, 31);">当你声明一个变量并为其指定为数字字面量类型时，TypeScript 会将该变量视为一个特定的数字值，而不仅仅是一般的数值类型。</font>

```plain
ini复制代码let a: 10 = 10;
let b: number = a;
console.log(a, b); // 输出 10, 10
```

<font style="color:rgb(25, 27, 31);">在这个示例中，变量 a 被声明为数字字面量类型 10，它只能具有值 10，而不能是其它的值。然后将变量 a 赋值给变量 b，因为 b 的类型是 number，而 a 是数字字面量类型 5，数字字面量类型是数字类型的子类型，所以赋值是允许的。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，只有字面量类型才可以赋值给相应的数值类型，普通数值类型不能赋值给字面量类型，除非两者完全匹配。</font>

### **<font style="color:rgb(25, 27, 31);">1.3. 枚举类型可以赋值给数字类型</font>**
<font style="color:rgb(25, 27, 31);">枚举类型在 TypeScript 中被编译成了一个具有反向映射的对象。默认情况下，枚举类型的成员值是从 0 开始递增的数字。由于枚举成员值是数字类型，所以它们可以被赋值给数字类型。</font>

```css
css复制代码enum Direction {
  Up,
  Right,
  Down,
  Left
}
let direction: Direction = Direction.Right;
let num: number = direction;
console.log(direction, num); // 输出：1, 1
```

<font style="color:rgb(25, 27, 31);">在上述示例中，将 Direction.Right 赋值给了枚举类型的变量 direction，然后又将 direction 赋值给了数字类型的变量 num，此时 num 的值为 1，与 Direction.Right 对应的枚举成员值相同。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，枚举类型不仅可以赋值给数字类型，也可以赋值给字面量类型或其他兼容的类型。这主要是由于 TypeScript 在类型系统中对枚举类型进行了特殊处理，使得枚举成员值可以被当作相应的字面量值使用。</font>

## **<font style="color:rgb(25, 27, 31);">2. 对象类型的兼容性</font>**
<font style="color:rgb(25, 27, 31);">对象类型包括接口（interface）、类（class）、字面量对象等。</font>

<font style="color:rgb(25, 27, 31);">记住这句话：</font>**<font style="color:rgb(25, 27, 31);">成员多的可以赋值给成员少的。</font>**

### **<font style="color:rgb(25, 27, 31);">2.1. 成员个数的兼容性</font>**
<font style="color:rgb(25, 27, 31);">对象类型 T 能够赋值给对象类型 U，需要满足的条件是 T 中的成员个数要大于等于 U 中的成员个数。也就是说，T 可以拥有 U 中的所有成员，但 T 可能还有额外的成员。</font>

```plain
ini复制代码class Pont2D {
  x: number;
  y: number;
}

class Point3D {
  x: number;
  y: number;
  z: number;
}

let p1: Pont2D = { x: 1, y: 2 }
let p2: Point3D = { x: 2, y: 3, z: 4 }
p1 = p2 // 正确，类 Point3D 拥有类 Point2D 中的所有成员
// p2 = p1 // 错误，类型 Point2D 中缺少属性 z，但类型 Point3D 中需要该属性
```

<font style="color:rgb(25, 27, 31);">在上述示例中，类 Point2D 具有 x 和 y 成员，类 Point3D 比类 Point2D 多了一个 z 成员，根据兼容性规则，Point3D 可以赋值给 Point2D，因为类 Point3D 拥有类 Point2D 中的所有成员。</font>

### **<font style="color:rgb(25, 27, 31);">2.2. 成员类型的兼容性</font>**
<font style="color:rgb(25, 27, 31);">对象类型 T 能够赋值给对象类型 U，需要满足的条件是 T 中的每个成员的类型都能够赋值给 U 中对应成员的类型。这个规则适用于成员变量和成员函数。</font>

```plain
ini复制代码interface Animal {
  name: string;
}

interface Dog {
  name: string;
  breed: string;
}

let animal: Animal = { name: "Animal" };
let dog: Dog = { name: "Dog", breed: "Husky" };

animal = dog; // 正确，Dog 的成员类型包含 Animal 的成员类型
// dog = animal; // 错误，类型 Animal 中缺少属性 breed，但类型 Dog 中需要该属性
```

### **<font style="color:rgb(25, 27, 31);">2.3. 可选属性的兼容性</font>**
<font style="color:rgb(25, 27, 31);">对象类型 T 能够赋值给对象类型 U，如果 U 中定义了可选属性，且 T 中没有对应的属性，则仍然可以进行赋值。</font>

```plain
ini复制代码interface Person {
  name: string;
  age?: number; // 可选属性
}

interface Employee {
  name: string;
  employeeId: string;
}

let person: Person = { name: "Echo", age: 26 };
let employee: Employee = { name: "James", employeeId: "123" };

person = employee; // 正确，虽然类型 Employee 中没有 age 属性，但类型 Person 中 age 属性是可选的
// employee = person; // 错误，类型 Person 中缺少属性 employeeId, 但类型 Employee 中需要该属性
```

## **<font style="color:rgb(25, 27, 31);">3. 函数类型兼容性</font>**
<font style="color:rgb(25, 27, 31);">函数之间的兼容性会比较复杂，需要考虑以下几个方面：</font>

+ <font style="color:rgb(25, 27, 31);">参数个数</font>
+ <font style="color:rgb(25, 27, 31);">参数类型</font>
+ <font style="color:rgb(25, 27, 31);">返回值类型</font>

### **<font style="color:rgb(25, 27, 31);">3.1. 参数个数</font>**
<font style="color:rgb(25, 27, 31);">源函数的参数个数要小于等于目标函数的参数个数。也就是说，源函数可以接受更少的参数或与目标函数相同数量的参数。多余的参数是允许的，因为在函数调用时可以忽略它们。</font>

<font style="color:rgb(25, 27, 31);">记住这句话：</font>**<font style="color:rgb(25, 27, 31);">参数少的可以赋值给参数多的。</font>**

```plain
typescript复制代码type Adder = (a: number, b: number) => number;
type Calculator = (a: number, b: number, c: number) => number;

let add: Adder = (a: number, b: number) => a + b;
let calculate: Calculator = (a: number, b: number, c: number) => a + b + c;

calculate = add; // 正确，Adder 的参数个数少于 Calculator 的参数个数
// add = calculate; // 错误，Calculator 的参数个数多于 Adder 的参数个数
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了两个类型 Adder 和 Calculator 分别表示加法函数和计算函数。根据函数兼容性规则，add 可以赋值给 calculate，因为 Adder 的参数个数（2个）少于 Calculator 的参数个数（3个）。但是相反的赋值会导致兼容性错误，因为 Calculator 的参数个数（3个）要多于 Adder 的参数个数（2个）。</font>

### **<font style="color:rgb(25, 27, 31);">3.2. 参数类型</font>**
```plain
ini复制代码let x = (a: number) => 0;
let y = (a: number, b: string) => 0;

y = x; // 正确
// x = y; // 错误
```

<font style="color:rgb(25, 27, 31);">在上述示例中，函数 x 的参数只有一个 a，类型为 number，函数 y 的参数有两个 a 和 b，类型分别为 number 和 string，x 可以赋值给 y，是因为 x 的每个参数都能在 y 里找到对应类型的参数。 注意的是参数的名字相同与否无所谓，只看它们的类型。 而 y 不能赋值给 x，因为 y 有个必需的第二个参数，但是 x 并没有，所以不允许赋值。</font>

### **<font style="color:rgb(25, 27, 31);">3.3. 返回值类型</font>**
<font style="color:rgb(25, 27, 31);">如果返回值类型是普通类型，此时函数的返回值类型要相同。</font>

```plain
typescript复制代码type F1 = () => string
type F2 = () => string

let func1: F1
let func2: F2

func1 = func2 // 正确
func2 = func1 // 正确
```

<font style="color:rgb(25, 27, 31);">如果返回值类型是对象类型，此时</font>**<font style="color:rgb(25, 27, 31);">成员多的可以赋值给成员少的。</font>**

```plain
typescript复制代码type F3 = () => { name: string }
type F4 = () => { name: string; age: number }

let func3: F3
let func4: F4

func3 = func4 // 正确
func4 = func3 // 错误
```

## **<font style="color:rgb(25, 27, 31);">4. 类类型兼容性</font>**
<font style="color:rgb(25, 27, 31);">类与对象字面量和接口差不多，但有一点不同：类有静态部分和实例部分的类型。 比较两个类类型的对象时，只有实例的成员会被比较。 静态成员和构造函数不在比较的范围内。</font>

```plain
typescript复制代码class Person {
  name: string;
  constructor(name: string, age: number) {}
}

class Employee {
  name: string;
  constructor(name: string, age: number, employee: string) {}
}

let person: Person;
let employee: Employee;

employee = person; // 正确
person = employee; // 正确
```

<font style="color:rgb(25, 27, 31);">私有的和受保护的成员必须来自于相同的类或者父类的派生类。</font>

```scala
scala复制代码class Person {
  protected name: string;
}

class Employee extends Person {}

let person: Person;
let employee: Employee;

employee = person; // 正确
person = employee; // 正确

class User {
  protected name: string;
}

let user: User;
person = user; // 错误
user = person; // 错误
```

## **<font style="color:rgb(25, 27, 31);">5. 泛型类型兼容性</font>**
<font style="color:rgb(25, 27, 31);">当泛型类型没有明确指定类型参数时，它被认为是一种特殊的兼容性形式，称为类型参数的默认，即泛型函数或泛型类在没有传递类型参数的情况下，它们的类型参数会被推导为any。此时，泛型类型可以兼容任意类型，也能赋值给其他泛型类型。</font>

```plain
ini复制代码type Box<T> = {
  value: T;
};

let boxA: Box<number>;
let boxB: Box<any>;

boxA = boxB; // 正确，类型参数的默认 any 能兼容任意类型
boxB = boxA; // 正确，boxA 指定的类型参数是 number，也能赋值给类型参数的默认 any
```

<font style="color:rgb(25, 27, 31);">当泛型类型明确指定了类型参数时，要求类型参数具有兼容的类型。这意味着泛型类型在传递不同类型参数时，需要确保它们之间满足兼容性规则。</font>

```plain
ini复制代码type Box<T> = {
  value: T;
};

let boxA: Box<number>;
let boxB: Box<string>;

boxA = boxB; // 报错，不能将类型 string 分配给类型 number
boxB = boxA; // 报错，不能将类型 number 分配给类型 string
```

## **<font style="color:rgb(25, 27, 31);">十一、交叉类型（Intersection Types）</font>**
<font style="color:rgb(25, 27, 31);">交叉类型类似于接口继承，是将多个类型合并为一个类型。 也就是说我们可以把现有的多种类型叠加到一起成为一种类型，它包含了所需的所有类型的特性。</font>

<font style="color:rgb(25, 27, 31);">使用符号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">&</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）来定义交叉类型。</font>

## **<font style="color:rgb(25, 27, 31);">1. 组合对象类型</font>**
```plain
ini复制代码type User = {
  name: string;
  age: number;
};

type Admin = {
  isAdmin: boolean;
};

type UserAdmin = User & Admin;

let userAdmin: UserAdmin = {
  name: "John",
  age: 30,
  isAdmin: true
};
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了 User 和 Admin 两个类型，然后使用交叉类型 & 将 User & Admin 连接起来创建了一个新的类型 UserAdmin，该类型包含了 User 和 Admin 类型的所有成员，接着我们定义了一个变量 userAdmin，该变量同时具有 User 和 Admin 类型的属性和方法。</font>

## **<font style="color:rgb(25, 27, 31);">2. 合并函数类型</font>**
```plain
typescript复制代码type AddFunc = {
  fn: (a: number, b: number) => number;
}
type MultiplyFunc = {
  fn1: (a: number, b: number) => number;
}

type MathOperations = AddFunc & MultiplyFunc;

const mathOps: MathOperations = {
  fn(num1, num2) {
    return num1 + num2;
  },
  fn1(num1, num2) {
    return num1 * num2
  }
};

console.log(mathOps.fn(10, 20));    // 输出：30
console.log(mathOps.fn1(10, 20));   // 输出：200
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了两个函数类型 AddFunc 和 MultiplyFunc，AddFunc 里面定义了 fn 函数，MultiplyFunc 里面定义了 fn1 函数，并使用交叉类型 & 将 AddFunc & MultiplyFunc 连接起来创建了一个新的类型 MathOperations。此时变量 mathOps 同时拥有 fn 和 fn1 两个方法。</font>

## **<font style="color:rgb(25, 27, 31);">3. 交叉类型VS接口继承</font>**
+ <font style="color:rgb(25, 27, 31);">相同点：都可以实现对象类型的组合。</font>
+ <font style="color:rgb(25, 27, 31);">不同点：两种方式实现类型组合时，对于同名属性之间，处理类型冲突的方式不同。</font>

<font style="color:rgb(25, 27, 31);">下面是接口继承的示例，接口B继承接口A，两个接口都定义了 fn 方法，返回值都是 string 类型，但是参数的类型不同，一个 string，一个 number，由于 fn 参数 value 的类型不兼容，所以接口 B 不能继承接口 A。</font>

```php
php复制代码interface A {
  fn: (value: number) => string
}

interface B extends A {
  fn: (value: string) => string
}
```

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763908612-81a1da9f-5b38-4f2c-ad87-c01b70e13c65.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">下面是交叉类型的示例：我们定义了 A 和 B 两个接口，然后使用交叉类型 & 将 A & B 连接起来创建了一个新的类型 ，接着我们定义了一个变量 c，类型为 C，变量 c 调用 fn 方法，此时参数的类型我们可以传数字类型或者字符串类型。</font>

```plain
typescript复制代码interface A {
  fn: (value: number) => string
}

interface B {
  fn: (value: string) => string
}

type C = A & B

let c: C
c.fn(1)       // 正确
c.fn('Echo')  // 正确
```

## **<font style="color:rgb(25, 27, 31);">4. 注意</font>**
**<font style="color:rgb(25, 27, 31);">如果合并的多个接口类型存在同名属性会是什么效果呢？</font>**

```plain
ini复制代码type User = {
  id: number;
  name: string;
}

type Admin = {
  name: number;
  age: number;
}

type UserAdmin = User & Admin

const user: UserAdmin = {
  id: 1,
  // name: "Echo", // 错误：不能将类型“string”分配给类型“never”
  name: 26, // 错误：不能将类型“number”分配给类型“never”
  age: 26
};
```

<font style="color:rgb(25, 27, 31);">在上面示例中，定义了两个类型 User 和 Admin，其中类型 User 中有 id 和 name 属性，类型 Admin 中有 name 和 age 属性，两个类型都有同名的 name 属性，但类型不同，一个是 string，一个是 number，合并后，name 属性的类型就是 string 和 number 两个原子类型的交叉类型，即 never。</font>

<font style="color:rgb(25, 27, 31);">此时，我们如果赋予 user 任意类型的 name 属性值都会提示类型错误。而如果我们不设置 name 属性，又会提示一个缺少必选的 name 属性的错误。在这种情况下，就意味着上述代码中交叉出来的 UserAdmin 类型是一个无用类型。</font>

**<font style="color:rgb(25, 27, 31);">如果同名属性的类型兼容，比如一个是 number，另一个是 number 的子类型、数字字面量类型，合并后 name 属性的类型就是两者中的子类型。</font>**

```plain
ini复制代码type User = {
  id: number;
  name: number;
}

type Admin = {
  name: 2;
  age: number;
}

type UserAdmin = User & Admin

const user: UserAdmin = {
  id: 1,
  // name: 2, // 正确
  name: 22,  // 错误：不能将类型“22”分配给类型“2”
  age: 26
};
```

<font style="color:rgb(25, 27, 31);">在上面示例中，name 属性的类型就是数字字面量类型 2，因此，我们不能把任何非 2 之外的值赋予 name 属性。</font>

**<font style="color:rgb(25, 27, 31);">如果交叉类型中的某个成员是对象类型，那么交叉后的类型将拥有这些对象类型的所有属性</font>**

```css
css复制代码interface A {
  x: {
    isShow: boolean
  }
}

interface B {
  x: {
    name: string
  }
}

interface C {
  x: {
    age: number
  }
}

type ABC = A & B & C;

let abc: ABC = {
  x: {
    isShow: true,
    name: 'Echo',
    age: 26
  }
};

console.log(abc); // 输出：x: { isShow: true, name: 'Echo', age: 26 }
```

## **<font style="color:rgb(25, 27, 31);">十二、泛型（Generics）</font>**
## **<font style="color:rgb(25, 27, 31);">1. 什么是泛型</font>**
<font style="color:rgb(25, 27, 31);">泛型（Generics）是 TypeScript 中一种允许我们在定义函数、类或接口时使用参数化类型的机制。泛型可以看作是类型参数，类似于函数中的参数，但是用于表示类型而不是值。它允许我们在定义函数、类或接口时使用占位符表示类型，并在实际使用时指定具体的类型。</font>

## **<font style="color:rgb(25, 27, 31);">2. 一个简单的例子</font>**
<font style="color:rgb(25, 27, 31);">现在我们有个需求：实现一个函数，传入的函数参数是什么类型的，返回值的类型也要跟函数参数的类型相同，并且函数只能接收一个参数，你会怎么做？</font>

```plain
typescript复制代码const identity: (value: number) => number = (value) => value

console.log(identity(10)); // 输出：10，类型是number
```

<font style="color:rgb(25, 27, 31);">上面的示例中，我们创建了一个 identity 函数，参数值和返回值类型都为 number，调用 identity 函数，传入一个数字，会返回数字本身。但是，该函数只能接收数值类型，如果我调用函数的时候传入字符串或者布尔值类型的值，此时就会报错。</font>

```plain
typescript复制代码const identity: (value: number) => number = (value) => value
console.log(identity('Echo')); // 报错：类型“string”的参数不能赋值给类型“number”的参数
```

<font style="color:rgb(25, 27, 31);">为了让函数能够接收任意类型，可以将参数类型改为any，但是，这样就失去了 TS 的类型保护，类型不安全。</font>

```plain
typescript复制代码const identity: (value: any) => any = (value) => value
console.log(identity('Echo'));    // 输出：Echo
console.log(identity(26));        // 输出：26
console.log(identity(true));      // 输出：true
console.log(identity(null));      // 输出：null
console.log(identity(undefined)); // 输出：undefined
```

<font style="color:rgb(25, 27, 31);">为了解决上面的这些问题，我们</font>**<font style="color:rgb(25, 27, 31);">使用泛型对上面的代码进行重构。</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">泛型在保证类型安全（不丢失类型信息）的同时，可以让函数等于多钟不同的类型一起工作，灵活可复用。</font>

```sql
sql复制代码function identity<T>(value: T): T {
  return value;
}

console.log(identity<string>('Echo'));   // 输出：Echo
console.log(identity<number>(26));       // 输出：26
console.log(identity<boolean>(true));    // 输出：true
```

<font style="color:rgb(25, 27, 31);">上面示例中，我们在函数名 identity 后添加了 ，其中 T 代表 Type，在定义泛型时通常用作第一个类型变量名称。但实际上 T 可以用任何有效名称代替。在调用函数 identity 时，在<>中指定类型 string，此时参数和返回值类型也都为 string。</font>

## **<font style="color:rgb(25, 27, 31);">3. 泛型语法</font>**
+ <font style="color:rgb(25, 27, 31);">在函数名称的后面添加尖括号（</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);"><></font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">）,尖括号中添加类型变量，比如下图中的</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">T。</font>**
+ <font style="color:rgb(25, 27, 31);">其中 T 代表 Type，可以是任意合法的变量名称。</font>
+ <font style="color:rgb(25, 27, 31);">类型变量 T，是一种特殊类型的变量，它用于处理类型而不是值。</font>
+ <font style="color:rgb(25, 27, 31);">该类型变量相当于一个类型容器，能够捕获用户提供的类型（具体是什么类型，由用户调用该函数时指定）。</font>
+ <font style="color:rgb(25, 27, 31);">因为 T 是类型，因此可以将其作为函数参数和返回值的类型，表示参数和返回值具有相同的类型。</font>

```plain
r复制代码function identity<T>(value: T): T {
  return value;
}
```

<font style="color:rgb(25, 27, 31);">在下面的示例中，调用泛型函数 identity，当传入类型 number 后，这个类型就会被函数声明时指定的类型变量 T 捕获到，此时，T 的类型就是 number，所以，函数 identity 的参数和返回值的类型也都是 number。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763908623-3f420aff-4972-4edf-a258-20c882ddc305.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">4. 简化调用泛型函数</font>**
+ <font style="color:rgb(25, 27, 31);">在调用泛型函数时，可以</font>**<font style="color:rgb(25, 27, 31);">省略<类型>来简化泛型函数的调用</font>**<font style="color:rgb(25, 27, 31);">。</font>
+ <font style="color:rgb(25, 27, 31);">此时，TS 内部会采用一种叫做类型参数推断的机制，来根据传入的实参自动推断出类型变量 T 的类型。</font>
+ <font style="color:rgb(25, 27, 31);">当编译器无法推断类型或者推断的类型不准确时，就需要显示地传入类型参数。</font>

<font style="color:rgb(25, 27, 31);">比如，传入实参10，TS 会自动推断出变量 num 的类型 number，并作为 T 的类型。</font>

```plain
r复制代码function identity<T>(value: T): T {
  return value;
}
```

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763909373-b23c5181-3be9-447d-b910-804a3e2eb02b.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">5. 多个类型参数</font>**
<font style="color:rgb(25, 27, 31);">定义泛型的时候，可以一次定义多个类型参数：</font>

```plain
arduino复制代码function swap<T, U>(tuple: [T, U]): [U, T] {
  return [tuple[1], tuple[0]];
}

console.log(swap(['Echo', 26])); // [26, 'Echo]
```

<font style="color:rgb(25, 27, 31);">上述示例中，我们定义了一个 swap 函数，用来交换输入的元组。</font>

## **<font style="color:rgb(25, 27, 31);">6. 泛型类</font>**
<font style="color:rgb(25, 27, 31);">泛型类（Generic Class）是指在定义类时使用泛型类型参数的类。它允许我们在类的属性、方法、构造函数以及实例化时使用泛型。</font>

+ <font style="color:rgb(25, 27, 31);">在 class 名称后面添加</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);"><类型变量></font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">，这个类就变成了泛型类。</font>
+ <font style="color:rgb(25, 27, 31);">在创建 class 实例时，在类名后面通过</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);"><类型></font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">来指定明确的类型。</font>

<font style="color:rgb(25, 27, 31);">下面是一个简单的泛型类的示例：</font>

```kotlin
kotlin复制代码class Container<T> {
  private items: T[] = [];

  addItem(item: T) {
    this.items.push(item);
  }

  getItem(index: number): T {
    return this.items[index];
  }

  getItems(): T[] {
    return this.items;
  }
}

const container = new Container<number>(); // 实例化一个泛型类，指定类型参数为 number
container.addItem(1);
container.addItem(2);
console.log(container.getItems()); // 输出: [1, 2]
```

## **<font style="color:rgb(25, 27, 31);">7. 泛型接口</font>**
+ <font style="color:rgb(25, 27, 31);">在接口名称的后面添加</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);"><类型变量></font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">，那么，这个接口就变成了泛型接口。</font>
+ <font style="color:rgb(25, 27, 31);">接口的类型变量，对接口中所有其它成员可见，也就是</font>**<font style="color:rgb(25, 27, 31);">接口中所有成员都可以使用类型变量。</font>**
+ <font style="color:rgb(25, 27, 31);">使用泛型接口时，需要显示指定具体的类型。</font>

<font style="color:rgb(25, 27, 31);">下面是一个简单的泛型接口的示例：</font>

```plain
vbnet复制代码interface KeyValuePair<K, V> {
  key: K;
  value: V;
}

const pair1: KeyValuePair<number, string> = { key: 1, value: "one" };
const pair2: KeyValuePair<string, boolean> = { key: "isEnabled", value: true };
```

## **<font style="color:rgb(25, 27, 31);">8. 泛型参数的默认类型</font>**
<font style="color:rgb(25, 27, 31);">在 TypeScript 2.3 以后，我们可以为泛型中的类型参数指定默认类型。当使用泛型时没有在代码中直接指定类型参数，从实际值参数中也无法推测出时，这个默认类型就会起作用。</font>

```plain
ini复制代码function createArray<T = string>(length: number, value: T): Array<T> {
  let result: T[] = [];
  for (let i = 0; i < length; i++) {
    result[i] = value;
  }
  return result;
}
```

## **<font style="color:rgb(25, 27, 31);">9. 泛型约束</font>**
<font style="color:rgb(25, 27, 31);">默认情况下，泛型函数的类型参数 T 理论上是可以是任何类型的，不同于 any，你不管使用它的什么属性或者方法都会报错（除非这个属性和方法是所有集合共有的）。</font>

<font style="color:rgb(25, 27, 31);">比如下面的示例中，我想打印出参数的 length 属性，如果不进行泛型约束 TS 是会报错的：类型“T”上不存在属性“length”。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763908676-ea3766a1-4c12-43fb-b09e-4cd4842f0ce9.png)

<font style="color:rgb(25, 27, 31);">  
</font>

<font style="color:rgb(25, 27, 31);">报错的原因很明显，如果要解决这个问题，我们就可以通过给泛型（类型变量）添加约束。</font>

<font style="color:rgb(25, 27, 31);">下面我们通过</font><font style="color:rgb(25, 27, 31);"> </font>**<font style="color:rgb(25, 27, 31);">extends</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字进行类型约束：</font>

```plain
scss复制代码interface ILength {
  length: number;
}

function getLength<T extends ILength>(value: T): T {
  console.log(value.length);
  return value;
}

getLength([1, 2, 3])                    // 正确，因为数组有 length 属性
getLength('Echo') //                    // 正确，因为字符串有 length 属性
getLength({ length: 10, name: 'Echo' }) // 正确，因为传入的参数有 length 舒心
getLength(10)                           // 报错：类型“number”不能赋值给类型“ILength”的参数，因为数字不具有 length 属性
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们定义了一个 ILength 接口，具有 length 属性。在泛型函数 getLength 中，使用 T extends ILength 进行约束，该约束表示：传入的类型必须具有 length 属性。</font>

## **<font style="color:rgb(25, 27, 31);">十三、TS中的关键字</font>**
<font style="color:rgb(25, 27, 31);">TS 内置了一些常用的工具类型，来简化 TS 中一些常见的操作，它们都是基于泛型实现的，并且是内置的，所以可以直接使用。</font>

<font style="color:rgb(25, 27, 31);">在学习工具类型之前，我们先学习一些关键字和基础知识，以便我们可以更好的去学习后面的内置工具类型。</font>

## **<font style="color:rgb(25, 27, 31);">1. keyof</font>**
<font style="color:rgb(25, 27, 31);">在 TS 中，</font>**<font style="color:rgb(25, 27, 31);">keyof</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">操作符主要用途是用于获取类型中所有键的关键字。它用于泛型中，通常与索引类型（index type）结合使用。其</font>**<font style="color:rgb(25, 27, 31);">返回类型是联合类型</font>**<font style="color:rgb(25, 27, 31);">。</font>

<font style="color:rgb(25, 27, 31);">下面示例中，我们定义了一个接口 Person，包含 name、age 和 gender 三个键，然后使用 keyof 来获取 Person 接口的所有键，这样，Keys 类型就是一个由 "name" | "age" | "gender" 构成的联合字面量类型。</font>

```plain
ini复制代码interface Person {
  name: string;
  age: number;
  gender: string;
}

type Keys = keyof Person; // "name" | "age" | "gender"
```

<font style="color:rgb(25, 27, 31);">下面示例中，我们创建一个函数来获取对象中属性的值：</font>

```plain
javascript复制代码function getProp<Type, Key extends keyof Type>(obj: Type, key: Key) {
  return obj[key];
}

const person = {
  name: 'Echo',
  age: 26,
  gender: 'male',
}

console.log(getProp(person, 'name'))   // 输出：Echo
console.log(getProp(person, 'age'))    // 输出：26
console.log(getProp(person, 'gender')) // 输出：male
```

<font style="color:rgb(25, 27, 31);">在 TS 中， 是一种泛型约束方式，用于限制一个泛型类型参数 key 的范围。</font>**<font style="color:rgb(25, 27, 31);">extends</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">关键字表示限制 key 的取值只能是 Type 类型中已有的属性名。可以理解为：Key 只能是 Type 所有键中的任意一个，或者说只能访问对象中存在的属性。</font>

<font style="color:rgb(25, 27, 31);">在上面的例子中，getProp 函数接收两个参数：一个泛型类型参数 Type，代表输入对象的类型；一个泛型类型参数 Key，代表属性名的类型。keyof Type 实际上获取的是 person 对象所有键的联合字面量类型，也就是：'name' | 'age' | 'gender'，当我们调用调用 getProp 函数传入一个不存在的属性名，例如： 'school' 会引发编译错误。</font>

<font style="color:rgb(25, 27, 31);">  
</font>

![](https://cdn.nlark.com/yuque/0/2025/png/27350975/1739763909049-ec076dd8-6a1c-45d0-8f80-b35cecebfa76.png)

<font style="color:rgb(25, 27, 31);">  
</font>

## **<font style="color:rgb(25, 27, 31);">2. typeof</font>**
<font style="color:rgb(25, 27, 31);">在 TS 中，</font>**<font style="color:rgb(25, 27, 31);">typeof</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">操作符的主要用途是在类型上下文中获取变量或者属性的类型。</font>

### **<font style="color:rgb(25, 27, 31);">2.1. typeof获取变量的声明类型</font>**
<font style="color:rgb(25, 27, 31);">在 TS 中，typeof 可以用来返回一个变量的声明类型，如果不存在，则获取该类型的推论类型。</font>

```plain
typescript复制代码let n: number = 26
type N = typeof n // 等同于 typeof N = number

let s: string = 'Echo'
type S = typeof s // 等同于 typeof S = string

let a: Array<number> = []
type A = typeof a // 等同于 typeof A = number[]

let sy: Symbol = Symbol()
type SY = typeof sy // 等同于 typeof SY = Symbol
```

<font style="color:rgb(25, 27, 31);">需要注意的是：</font>

+ **<font style="color:rgb(25, 27, 31);">typeof作为类型操作符后面只能跟变量。</font>**

```plain
ini复制代码let str = 's';
type S = typeof str; // 正确

// type S1 = typeof 'str';  // 错误
```

+ **<font style="color:rgb(25, 27, 31);">如果变量没有声明类型，typeof返回变量的推断类型。</font>**

<font style="color:rgb(25, 27, 31);">如果变量没有明确声明类型，typeof 将返回变量的推断类型。此时，let关键字声明的变量，可以被重新赋值。</font>

```rust
rust复制代码let str = 'Echo'
type S = typeof str // 等同于 type S= string

// 可以被重新赋值
str = 'Steven' // 正确
// str = 26 // 报错：不能将类型“number”分配给类型“string”
```

<font style="color:rgb(25, 27, 31);">有时候，我们希望变量是常量，不允许被重新赋值。const 关键字可以解决这个问题。此时，基于类型推断，返回类型是等号右边的字面量类型。</font>

<font style="color:rgb(25, 27, 31);">例如，下面示例中，typeof str 返回的是字面量类型 'Echo'，不是字符串。</font>

```plain
ini复制代码const str = 'Echo'
type S = typeof str // 等同于：type S = 'Echo'
// str = 'Steven' // 报错：无法分配到“str”，因为它是常数
```

<font style="color:rgb(25, 27, 31);">在 Typescript3.4 中引入了一种新的字面量构造方式，const 断言。在 const 断言作用下，即使是 let 声明也可以限制类型扩展，变量不能被重新赋值。</font>

<font style="color:rgb(25, 27, 31);">例如，下面示例中，typeof str 返回的是字面量类型 'Echo'，不是字符串。</font>

```plain
ini复制代码let str = "Echo" as const
 type S = typeof str // 等同于：type S = "Echo"
 // str = 'Steven' // 报错：无法分配到“"Steven"”分配给类型“"Echo"”
```

<font style="color:rgb(25, 27, 31);">当我们使用 const 断言构造新的字面量表达式时，应注意以下几点：</font>

+ <font style="color:rgb(25, 27, 31);">表达式中的任何字面量类型都不应该被扩展。</font>
+ <font style="color:rgb(25, 27, 31);">对象字面量的属性，将使用 readonly 修饰。</font>
+ <font style="color:rgb(25, 27, 31);">数组字面量将变成 readonly 元组。</font>

```rust
rust复制代码let str = "Echo" as const;
 type S = typeof str; // 等同于：type S = "Echo"
 
 let num = [1, 2, 3] as const;
 type N = typeof num; // 等同于：type N = readonly [1, 2, 3]
 
 let obj = { name: "Echo" } as const;
 type O = typeof obj; // 等同于：type O = { readonly name: "Echo"; }
```

<font style="color:rgb(25, 27, 31);">如果变量明确声明了类型，推断类型不受 const 影响，typeof str 返回 str 的声明类型 string，而不是字面量类型 "Steven"，但是变量依然不能被重新赋值。</font>

```plain
ini复制代码const str: string = "Echo";
 type S = typeof str // 等同于：type S = string
 str = "Steven" // 报错：无法分配到 "str" ，因为它是常数。
```

### **<font style="color:rgb(25, 27, 31);">2.2. typeof与对象结合使用</font>**
<font style="color:rgb(25, 27, 31);">typeof与对象结合使用，可以用来获取对象的结构类型，以及使用该类型来声明新的变量或函数参数等。</font>

1. **<font style="color:rgb(25, 27, 31);">获取对象的类型</font>**

```rust
rust复制代码const person = {
   name: 'Echo',
   age: 26,
 }
 
 type Person = typeof person
 // 相当于
 // type Person = {
 //   name: string;
 //   age: number;
 // }
```

<font style="color:rgb(25, 27, 31);">在上述示例中，typeof person 返回的是对象 person 的类型，即 { name: string; age: number; }。</font>

1. **<font style="color:rgb(25, 27, 31);">声明新变量的类型为对象的类型</font>**

```css
css复制代码const person = {
   name: 'Echo',
   age: 26,
 }
 
 const newPerson: typeof person = {
   name: 'Steven',
   age: 33,
 };
 
 console.log(newPerson);  // 输出：{ name: 'Steven', age: 33 }
```

<font style="color:rgb(25, 27, 31);">在上述示例中，我们使用 typeof person 将 newPerson 的类型声明为 { name: string; age: number; }，并赋予了新的值。</font>

1. **<font style="color:rgb(25, 27, 31);">在函数参数中使用对象的类型</font>**

```plain
javascript复制代码const person = {
  name: 'Echo',
  age: 26,
}

function printObj(obj: typeof person) {
  console.log(obj);
}

printObj(person);  // 输出：{ name: 'Echo', age: 26 }
```

<font style="color:rgb(25, 27, 31);">在上述示例中，函数 printObj 接收一个参数，其类型为 typeof person，即接收与对象 person 相同类型的参数。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，typeof 运算符用于获取对象类型是在静态类型检查阶段进行的，而不是在运行时期执行的。因此，它只提供了类型信息，而不会直接访问对象的值。</font>

### **<font style="color:rgb(25, 27, 31);">2.3. typeof与接口结合使用</font>**
<font style="color:rgb(25, 27, 31);">typeof 与接口结合使用可以用于创建新类型，该类型的属性和方法将与给定对象类型保持一致。</font>

```plain
typescript复制代码interface Person {
   name: string;
   age: number;
 }
 
 const person: Person = {
   name: 'Echo',
   age: 26,
 }
 
 type NewPerson = typeof person
 
 const newPerson: NewPerson = {
   name: 'Steven',
   age: 33,
 }
```

<font style="color:rgb(25, 27, 31);">在上述实例中，定义了一个名为 Person 的接口，然后创建一个对象 person，类型为 Person，接着使用 typeof 来创建一个新的类型 NewPerson，该类型的属性和方法将与 Person 接口中定义的属性和方法保持一致，这样我们就可以基于 NewPerson 来创建新的对象。</font>

<font style="color:rgb(25, 27, 31);">需要注意的是，typeof 运算符与接口结合使用通常适用于已存在的对象，它提取已知对象的类型用于创建新的类型。它不会用于动态创建对象或实例化类。</font>

### **<font style="color:rgb(25, 27, 31);">2.4. typeof与keyof结合使用</font>**
<font style="color:rgb(25, 27, 31);">keyof 主要用于获取类型的所有属性键，可以与 typeof 结合使用，获取某个类型的键集合。</font>

```bash
bash复制代码let person = {
   name: 'Echo',
   age: 28,
   address: 'Guang Zhou',
 }
 
 type Person = keyof typeof person // 等同于：type Person = "name" | "age" | "address"
```

## **<font style="color:rgb(25, 27, 31);">3. in</font>**
<font style="color:rgb(25, 27, 31);">在 TS 中，</font>**<font style="color:rgb(25, 27, 31);">in</font>**<font style="color:rgb(25, 27, 31);"> </font><font style="color:rgb(25, 27, 31);">操作符的主要用于遍历目标类型的属性 key 值。类似 for...in，一般结合 [] 一起使用。</font>

### **<font style="color:rgb(25, 27, 31);">3.1. 遍历枚举类型</font>**
```plain
ini复制代码enum Direction {
   Up,
   Right,
   Down,
   Left
 }
 
 type DirectionType = {
   [value in Direction]: number
 }
 
 /**
 type DirectionType = {
   0: number;
   1: number;
   2: number;
   3: number;
 }
 */
```

### **<font style="color:rgb(25, 27, 31);">3.2. 遍历联合类型</font>**
```plain
ini复制代码type Property = 'name' | 'age' | 'gender' | 'address';
 
 type PropertyMap = {
   [key in Property]: string;
 }
 
 /**
 type PropertyMap = {
   name: string;
   age: string;
   gender: string;
   address: string;
 }
  */
```

## **<font style="color:rgb(25, 27, 31);">4. extends</font>**
### **<font style="color:rgb(25, 27, 31);">4.1. 用于泛型函数</font>**
```plain
typescript复制代码type NT = number | string;
 
 // T 必须是 number 或 string 类型
 function printValue<T extends NT>(value: T) {
   console.log(value);
 }
 
 printValue("Echo"); // 正确
 printValue(26);     // 正确
 // printValue(true); // 错误，布尔类型不符合约束条件
```

### **<font style="color:rgb(25, 27, 31);">4.2. 用于泛型类</font>**
```scala
scala复制代码interface ILength {
   length: number;
 }
 
 // T 必须是具有 length 属性的类型
 class Container<T extends ILength> {
   value: T;
 
   constructor(value: T) {
     this.value = value;
   }
 
   printLength() {
     console.log(this.value.length);
   }
 }
 
 const container1 = new Container("Echo"); // 正确
 container1.printLength(); // 输出: 4
 
 // const container2 = new Container(26); // 错误，数字类型没有 length 属性
```

### **<font style="color:rgb(25, 27, 31);">4.3. 用于类继承</font>**
```plain
typescript复制代码class Animal {
   name: string;
 
   constructor(name: string) {
     this.name = name;
   }
 
   move(distance: number): void {
     console.log(`${this.name} moved ${distance} meters.`);
   }
 }
 
 class Dog extends Animal {
   bark(): void {
     console.log("Woof! Woof!");
   }
 }
 
 const dog = new Dog("Hate");
 dog.move(10);   // 调用继承来自父类的方法 输出：Hate moved 10 meters.
 dog.bark();     // 调用子类自己定义的方法 输出：Woof! Woof!
```

### **<font style="color:rgb(25, 27, 31);">4.4. 用于继承接口</font>**
```plain
ini复制代码interface Shape {
   color: string;
 }
 
 interface Square extends Shape {
   sideLength: number;
 }
 
 let square = <Square>{};
 square.color = "blue";
 square.sideLength = 10;
```

### **<font style="color:rgb(25, 27, 31);">4.5. 用于类型约束</font>**
```plain
scss复制代码interface ILength {
   length: number;
 }
 
 function getLength<T extends ILength>(value: T): T {
   console.log(value.length);
   return value;
 }
 
 getLength([1, 2, 3])                    // 正确，因为数组有 length 属性
 getLength('Echo') //                    // 正确，因为字符串有 length 属性
 getLength({ length: 10, name: 'Echo' }) // 正确，因为传入的参数有 length 舒心
 getLength(10)                           // 报错：类型“number”不能赋值给类型“ILength”的参数，因为数字不具有 length 属性
```

### **<font style="color:rgb(25, 27, 31);">4.6. 用于条件类型</font>**
<font style="color:rgb(25, 27, 31);">TypeScript 2.8引入了条件类型表达式，类似于三元运算符。</font>

```plain
typescript复制代码type NoNullAndUndefined<T> = T extends null | undefined ? never : T;  // 如果泛型参数 T 为 null 或 undefined，那么取 never，否则直接返回 T。
 let k1: NoNullAndUndefined<number>;    // k1 是 number类型，因为 number 不是 null | undefined 的子集
 let k2: NoNullAndUndefined<undefined>; // k2 是 never类型，因为 undefined 是 null | undefined 的子集
```

<font style="color:rgb(25, 27, 31);">条件类型也支持嵌套。</font>

```plain
typescript复制代码type TypeName<T> =
   T extends string ? "string" :
   T extends number ? "number" :
   T extends boolean ? "boolean" :
   T extends undefined ? "undefined" :
   T extends Function ? "function" : "object";
 
 type T0 = TypeName<'Echo'>;      // "string"
 type T1 = TypeName<26>;          // "number"
 type T2 = TypeName<true>;        // "boolean"
 type T3 = TypeName<() => void>;  // "function"
 type T4 = TypeName<string[]>;    // "object"
```

## **<font style="color:rgb(25, 27, 31);">十四、泛型工具类型</font>**
<font style="color:rgb(25, 27, 31);">泛型工具类型这一章节相关的内容我想放到其它文章中来讲，因为这里涉及到的知识点有点多，一时半会写不完，大家可以持续关注我，精力有限，尽量做到每周2-3更！！！</font>

## **<font style="color:rgb(25, 27, 31);">十五、总结</font>**
<font style="color:rgb(25, 27, 31);">如果文章有什么错误，欢迎大家在评论区指正，如果觉得本文对您有帮助的话，欢迎 </font>**<font style="color:rgb(25, 27, 31);">点赞收藏</font>**<font style="color:rgb(25, 27, 31);">哦</font>

