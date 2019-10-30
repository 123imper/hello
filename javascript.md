document	对象

查找页面节点的方法

document.getElementById(id名字)；

document.getElementsByTagName(标签的名字)；//指定标签名的标签集合[0]

document.getElementsByClassName(标签的类名)；

js 写在head标签里		 加载事件，页面加载完毕之后执行脚本

数组的索引值从0开始[]

 对象 	document  	

函数 : 可重复利用的代码块.	function 关键字	1.0 定义函数

参数传递
function add(a) { //形参 console.log(a) 100}    2.0 调用函数    add(100)//实参

作用域 function			在控制台输出console

基本的数据类型			 string  number boolean  undefined  null 

变量的声明	 关键字  var  全局变量	局部变量	 隐式变量 

 查找页面节点的方法

\- document.getElementById( id名字 ); //指定id的标签

\- document.getElementsByTagName(标签的名字); //指定标签名的标签集合 []

\- document.getElementsByClassName(标签的类名); //指定类名的标签集合 []

检测数据类型的关键字 typeof

隐式转换  + /- 	parseInt//强制转换number类型 (取整)	parseFloat// 转换number类型(带小数点 , 浮点型)	parseFloat//not a number  是一种特殊的数值

语法

​        // if( 条件 ){ //执行结果 } 

​        // if( 条件 ){ //执行结果1 }else { //执行结果2}

​        // if( 条件1 ){ //执行结果1 }else if(条件2 ){ //执行结果2 }else {//执行结果3}

window 下属性和方法是全局的	在head标签内些脚本 , 不执行window.onload = function(){} ,获取不到页面元素

 事件 ？ 某一种行为   onclick  onmouseover onmouseleave ....

​        // 事件对象  ？ 由某一种行为产生的集合 { key:value }

​        // 给页面绑定点击事件

​        // 页面 document

表达式 = 操作符 + 操作数

debugger 打断点		函数不调用不执行。

对象 = document.createElement('标签')//创建            对象.appendChild(变量)//添加元素

removeChild(变量); //删除指定的元素

类名操作

classList.add()添加类名 	classList.remove()//删除类名	classList.contain()判断是否包含类名

定时器

调用者：window

参数：b1：function(){}  

b2:毫秒值，时间   1000毫秒=1秒

返回值：忽略

功能：执行时间执行函数

1.setInterval(function(){} ,1000) //相隔指定时间执行函数多次   用法	var timer = 

2.clearInterval()	//停止定时器函数（清楚定时器）

3.setTimeout() //延迟函数，在指定时间执行函数（一次）

4.clearTimeout()

​	getComputedStyle()		getComputedStyle(1.dom元素 2.伪类元素/null)[属性名]

调用者：window

参数：dom元素	null

返回值：样式的对象

功能：获取标签的样式

div.getAttribute('class');   //获取div标签的class的值

setAttribute('id','dome')//设置div标签的id的值

.removeAttribute('src');//移除标签src属性

兼容IE浏览器

currentStyle(属性)		dom.style.width = '100px';

1. 定时器 
   a. 调用者： window
   b. 参数 : b1: function(){}  b2:毫秒值 ，时间   1000 毫秒  = 1秒
   c. 返回值： 忽略
   d. 功能 ： 执行时间执行函数

- 相隔指定的时间执行函数(多次)
  var timer = setInterval(  function(){} , 1000 )
- 停止定时器函数 （清除定时器）
  clearInterval(timer);

- 延迟函数，在指定时间执行函数(一次)
  var timer = setTimeout( function(){} , 1000 )
  clearTimeout(timer);

1. 获取页面元素的方法
   // 动态获取元素
   document.getElementById('ID'); //单一元素
   document.getElementsByTagName('标签'); //元素集合
   document.getElementsByClassName('类名'); //元素集合
   //静态获取元素
   document.querySelector('#/./标签');//单一元素
   document.quertSelectorAll('#/./标签'); //元素集合
2. 创建元素的方法
   document.createElement('标签');
3. 添加元素的方法
   父元素.appendChild(元素);
4. 删除元素的方法
   父元素.removeChild(元素)

onfocus =====> 输入框获取焦点事件  function(){}
onblur =====>  输入框失去焦点事件  function(){}

![捕获](C:\Users\Administrator.USER-20190704PG\Desktop\捕获.PNG)

##### DOM 操作 ---- 属性

1. 如何优化前端页面性能 ? 
   a. 代码减少冗余 .
   b. 使用雪碧图(精灵图) , 减少http请求
   c. 减少页面的dom操作
   d. 合理处理数据 data
   ...

##### 定时器

#### object -----> Function / Array / Date 

1.0  对象
var obj = {}
var space = {
	dom:div,
	foo:function(){}
}

2.0 Date 日期对象

Date(); //作为普通函数调用

new Date();//作为构造函数 ,然后创建实例

------

2.1日期对象定义
他就是一个盒子。里面装满了与日期有关的所有信息的盒子。
日期对象一般不独立使用，可以独立获取里面的相关信息。
Wed    Apr    13   2016    10:45:32    GMT+0800 (中国标准时间)
星期		月份	 日期	 年		时分秒	 时区
2.2定义方法
2.2.1常用
var date1 = new Date();

设定制定时间：（兼容最强）
var date2 = new Date("2016/01/27 12:00:00")
2.2.2不常用：
var date3 = new Date('Wed Jan 27 2016 12:00:00 GMT+0800 (中国标准时间)');
var date4 = new Date(2016, 1, 27);
2.2.3日期对象方法使用
获取日期和时间
getDate()                获取日 1-31
getDay ()                获取星期 0-6（0代表周日）
getMonth ()              获取月 0-11（1月从0开始）
getFullYear ()	         获取完整年份（浏览器都支持）
getHours ()	       	   	 获取小时 0-23
getMinutes ()	         获取分钟 0-59
getSeconds ()	         获取秒  0-59
getMilliseconds ()       获取毫秒 （1s = 1000ms）

getTime()	             返回累计毫秒数(从1970/1/1午夜) 至今  时间戳

##### Math  数学对象

Math.floor()// 向下取整 1.2  Math.floor(1.2) // 1 |  Math.floor(99.9) // 99
Math.ceil() // 向上取整 1.2  Math.ceil(1.2) // 2  |  Math.floor(99.9) //100
Math.abs();//取绝对值  Math.abs(-10);// 10
Math.random();//0-1之间随机数   0.4213412341243
Math.random()*10;// 0-10 之间的随机数 
Math.round();//四舍五入

<!-- 计算弧度:  角度 * Math.PI/180 -->
<!-- 三角函数 canvas -->
Math.sin(弧度) ;//正弦  a:临边   b:对边  c:斜边      
Math.cos(弧度);//余弦
Math.tan(弧度);//正切

查找父节点   parentNode;				查找子元素 	children

查找子节点	childNodes		查找当前元素上一个元素  previousElementSibling

查找当前元素下一个元素  nextElementSibling							childNodes;//数组



键盘事件

onkeydown	onkeyup	onkeypress

|| "或"  两个条件  ，其一为ture，结果为ture 

&& '与' 两个条件，其一为false，结果为false

动画原理			 目标值 = 当前值 + 步长

indexof 是否存在这个字符   返回值是该元素的索引值

.push(); 往数组尾部添加元素

.unshift();往数组头部添加元素

.pop();往数组尾部删除元素

.shift();往数组头部删除元素

join()	把数组元素拼接字符串

.concat	合并数组

.splice(x);//原数组保留前x个 ，新数组 获取索引值为x开始的所有元素

//.splice(x,x) 

 //原数组：// 第一个参数：开始元素的索引值 //第2个参数：删除的元素的个数  //第多个参数：在原数组里添加的元素

// 新数组：//第一个参数：开始元素的索引值 // 第二个参数：保留元素的个数 

.slice(x);// 截取索引值为x开始的字符到最后

.slice(x,x) // 参数1：开始的索引值  参数2：结束的索引值 （包括左边不包括右边的字符）备注：开始索引值   <   结束的索引值

.substr(x);//截取索引值为x后面的所有字符

 // event.stopPropagation();//事件对象下的方法  阻止事件的API  冒泡事件  由内往外 

event.stopImmediatePropagation();//阻止事件捕获  由外往内

可以在事件对象的tagget属性

navgator.userAgent;//是个属性 获取对象当前设备信息 字符串

 back.onclick=function(){}

​        back.addEventListener('click',function(){

​            // 返回上一个页面  历史记录   上一个记录

​            // window   对象

​            // history 对象

​            window.history.back();

​        })

​        // 

​        forword.addEventListener('click',function(){

​            // 历史记录  下一个记录  进入下一个页面

​            window.history.forward();

​        })

// BOM提供的四个对象	// history   navgator   screen   location

​    var obj = window.screen;//对象包含用户屏幕的信息

window.location;  设置跳转页面的路径



   console.log(box.offsetLeft);//元素距离浏览器的左边的间距（没有父元素/父元素没有定位）

​        console.log(box.offsetTop);//元素距离浏览器的顶部的间距（没有父元素/父元素没有定位）

​        console.log(box.offsetHeight);//获取元素的宽度：border + padding + content

​        console.log(box.offsetWidth);//获取元素的高度：border + padding + content



 console.log(box.clientHeight)//获取元素的高度 padding + content

​        console.log(box.clientWidth)//获取元素的宽度 padding + content

​        console.log(box.clientLeft)//获取元素left边框的大小

​        console.log(box.clientTop)//获取元素top边框的大小



闭包：

概念：一个外部函数的声明变量，能被内部函数所使用	

封闭的环境，暂存指定的值，不被销毁。一个外部函数的变量，能被内部函数所使用。

function outerFunc(){

var a = 100;

function inner(){

console.log(a)

​		}

return inner;

}

var f = outerFunc()

f();

垃圾回收机制：在浏览器里，有个程序每个一段时间，自动寻找不在被继续使用的值，把这些值销毁掉。（把不需要使用的值给释放掉他们所占用的空间）

内存泄露：已经没有使用的值，还一直存在这个内存中。（不断增加不需要用到的值一直不断增加）

  //递归：函数在自身作用域调用

​    // 函数的自身调用：直接调用和间接调用