Web技术的三层蛋糕标准 

- [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML)是一种标记语言，用来结构化我们的网页内容和赋予内容含义，例如定义段落、标题、和数据表,或在页面中嵌入图片和视频。
- [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) 是一种样式规则语言，我们将样式应用于我们的 HTML 内容， 例如设置背景颜色和字体，在多个列种布局我们的内容。
- [JavaScript](https://developer.mozilla.org/en-US/docs/Glossary/JavaScript) 是一种编程语言，允许你创建动态更新的内容，控制多媒体，图像动画，和一些其他的东西。好吧，虽然不是一切，但是它的神奇之处是你能够用几行JavaScript代码就能实现。



在 JavaScript 代码里，被称为**应用程序编程接口 [Application Programming Interfaces** (**APIs)]** 的功能会提供额外的超能力给你使用。

APIs 是已经建立好的一套代码组件，目的是让开发者可以实现除此之外很难甚至不可能实现的程序





#### 对事件冒泡和捕捉的解释

当一个事件发生在具有父元素的元素上(例如，在我们的例子中是`<video>`元素)时，现代浏览器运行两个不同的阶段 - 捕获阶段和冒泡阶段。 在捕获阶段：

- 浏览器检查元素的最外层祖先`<html>`，是否在捕获阶段中注册了一个`onclick`事件处理程序，如果是，则运行它。
- 然后，它移动到`<html>`中的下一个元素，并执行相同的操作，然后是下一个元素，依此类推，直到到达实际点击的元素。

在冒泡阶段，恰恰相反:

- 浏览器检查实际点击的元素是否在冒泡阶段中注册了一个`onclick`事件处理程序，如果是，则运行它
- 然后它移动到下一个直接的祖先元素，并做同样的事情，然后是下一个，等等，直到它到达`<html>`元素。



# 变量

## JavaScript 拥有动态类型

JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：

### 实例

```
var x                // x 为 undefined
var x = 6;           // x 为数字
var x = "Bill";      // x 为字符串
```

http://www.w3school.com.cn/js/js_datatypes.asp

## JavaScript 数组

下面的代码创建名为 cars 的数组：

```
var cars=new Array();
cars[0]="Audi";
cars[1]="BMW";
cars[2]="Volvo";
```

或者 (condensed array):

```
var cars=new Array("Audi","BMW","Volvo");
```

或者 (literal array):

### 实例

```
var cars=["Audi","BMW","Volvo"];
```

## JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

```
var person={firstname:"Bill", lastname:"Gates", id:5566};
```

上面例子中的对象 (person) 有三个属性：firstname、lastname 以及 id。

空格和折行无关紧要。声明可横跨多行：

```
var person={
firstname : "Bill",
lastname  : "Gates",
id        :  5566
};
```

对象属性有两种寻址方式：

### 实例

```
name=person.lastname;
name=person["lastname"];
```

# JavaScript toSource() 方法

[JavaScript Math 对象](http://www.w3school.com.cn/jsref/jsref_obj_math.asp)

## 定义和用法

toSource() 方法返回表示对象源代码的字符串。

### 语法

```
object.toSource()
```

## 提示和注释

注释：该方法在 Internet Explorer 中无效。

## 实例

下面的例子向您展示 toSource() 方法的用法：

```
<script type="text/javascript">

function employee(name,job,born)
{
this.name=name;
this.job=job;
this.born=born;
}

var bill=new employee("Bill Gates","Engineer",1985);

document.write(bill.toSource());

</script>
```

输出：

```
({name:"Bill Gates", job:"Engineer", born:1985}) 
```





# JavaScript isNaN() 函数

[JavaScript 全局对象](http://www.w3school.com.cn/jsref/jsref_obj_global.asp)

## 定义和用法

isNaN() 函数用于检查其参数是否是非数字值。

### 语法

```
isNaN(x)
```

# JavaScript Math 对象

## Math 对象

[Math](http://www.w3school.com.cn/jsref/jsref_obj_math.asp) 对象用于执行数学任务。

### 使用 Math 的属性和方法的语法：

```
var pi_value=Math.PI;
var sqrt_value=Math.sqrt(15);
```

注释：Math 对象并不像 Date 和 String 那样是对象的类，因此没有构造函数 Math()，像 Math.sin() 这样的函数只是函数，不是某个对象的方法。您无需创建它，通过把 Math 作为对象使用就可以调用其所有属性和方法。



## "this"的含义

关键字"this"指向了当前代码运行时的对象