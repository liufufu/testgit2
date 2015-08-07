## 这是我的第一次作业（HTML+CSS） ##

**MarkdownPad** is a full-featured Markdown editor for Windows.

## Markdown的9种基本语法 ##
1. 标题设置（让字体变大，和word的标题意思一样）
 在Markdown当中设置标题，有两种方式：
 第一种：通过在文字下方添加“=”和“-”，他们分别表示一级标题和二级标题。
 第二种：在文字开头加上 “#”，通过“#”数量表示几级标题。（一共只有1~6级标题，1级标题字体最大）
2. 块注释（blockquote）：通过在文字开头添加“>”表示块注释。（当>和文字之间添加五个blank时，块注释的文字会有变化。）
3. 斜体：将需要设置为斜体的文字两端使用1个“*”或者“_”夹起来
4. 粗体：将需要设置为斜体的文字两端使用2个“*”或者“_”夹起来
5. 无序列表：在文字开头添加(*, +, and -)实现无序列表。但是要注意在(*, +, and -)和文字之间需要添加空格。（建议：一个文档中只是用一种无序列表的表示方式）
6. 有序列表：使用数字后面跟上句号。（还要有空格）
7. 链接（Links）
Markdown中有两种方式，实现链接，分别为内联方式和引用方式。
内联方式：This is an [example link](http://example.com/).
引用方式：
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].  
[1]: http://google.com/        "Google" 
[2]: http://search.yahoo.com/  "Yahoo Search" 
[3]: http://search.msn.com/    "MSN Search"
8. 图片（Images）
 图片的处理方式和链接的处理方式，非常的类似。
 内联方式：![alt text](/path/to/img.jpg "Title")
引用方式：![alt text][id] [id]: /path/to/img.jpg "Title"
9. 下划线：在空白行下方添加三条“-”横线。（前面讲过在文字下方添加“-”，实现的2级标题）

##首先是对天哥早上布置任务的解决 ##

*HTTP状态码
*HTTP Method

下面是对这些问题的解答:
### HTTP状态码 ###
- HTTP状态码（HTTP Status Code）是用以表示网页服务器HTTP响应状态的3位数字代码。它由 RFC 2616 规范定义的，并得到RFC 2518、RFC 2817、RFC 2295、RFC 2774、RFC 4918等规范扩展。
- 所有状态码的第一个数字代表了响应的五种状态之一
- 其中以1字头开始的表示这是一个消息状态码，代表请求已被接受，需要继续处理，如100 Continue,101 Switching Protocols,102 Processing等。
- 以2开头的状态码一般都代表请求已成功被服务器接收、理解、并接受，如200 OK，201 Created,202 Accepted,203 No-Authoriative Information等等。
- 以3开头的这类状态码代表需要客户端采取进一步的操作才能完成请求。通常，这些状态码用来重定向，后续的请求地址（重定向目标）在本次响应的 Location 域中指明。如300  Multiple Choices,301 Moved Permanently,302 Move temporarily等。
- 以4开头的状态码代表了客户端看起来可能发生了错误，妨碍了服务器的处理，除非响应的是一个 HEAD 请求，否则服务器就应该返回一个解释当前错误状况的实体，以及这是临时的还是永久性的状况。这些状态码适用于任何请求方法。浏览器应当向用户显示任何包含在此类错误响应中的实体内容。如400 Bad Request，401 Unauthorized，402 Payment Required，403 Forbidden，404 Not Found等。
- 以5开头的状态码代表了服务器在处理请求的过程中有错误或者异常状态发生，也有可能是服务器意识到以当前的软硬件资源无法完成对请求的处理。除非这是一个HEAD 请求，否则服务器应当包含一个解释当前错误状态以及这个状况是临时的还是永久的解释信息实体。浏览器应当向用户展示任何在当前响应中被包含的实体。如500 Internal Server Error，501 Not Implemented，502 Bad Gateway，503 Service Unavailable等。
### HTTP Method ###
- get Method：从指定的url上获取信息
- post mdthod：提交body中的内容给服务器中指定的url中，属于非幂等的(non-idempotent)请求
- head Method:从指定的url上获取header内容(类似Get方式)
- The different of get and post：除了大小不同，前者能保存书签，后者不是幂等性的，表单默认是GET方式提交除非指定method=post

### margin and padding ###
- 在CSS中margin是指从自身边框到另一个容器边框之间的距离，就是容器外距离。在CSS中padding是指自身边框到自身内部另一个容器边框之间的距离，就是容器内距离。
- padding

1、语法结构

（1）padding-left:10px; 左内边距

（2）padding-right:10px; 右内边距

（3）padding-top:10px; 上内边距

（4）padding-bottom:10px; 下内边距

（5）padding：10px; 四边统一内边距

（6）padding:10px 20px; 上下、左右内边距

（7）padding:10px 20px 30px; 上、左右、下内边距

（8）padding:10px 20px 30px 40px; 上、右、下、左内边距

2、可能取的值

（1）length  规定具体单位记的内边距长度

（2）%       基于父元素的宽度的内边距的长度

（3）auto    浏览器计算内边距

（4）inherit 规定应该从父元素继承内边距


- margin:和padding的用法相同
- [示例图](http://blog.sina.com.cn/s/blog_5f738d3d0100kxmm.html)

### 浮动 ###

- Float常跟属性值left、right、none  
  Float:none 不使用浮动  
  Float:left 靠左浮动  
  Float:right 靠右浮动
- 默认情况下，float值为none
- 浮动元素的边距不会合并
- 非替换元素需要设置宽
### border ###
- 我们常用的border一般为四个边框属性相同的那种，例如  
p
  {
  border:5px solid red;
  } 指的就是边框的4边宽度为5px,边框类型为实边，颜色为红色。
- 当边框的4边属性不相同时我们可以这样设置<br>border-left 设置左边框，一般单独设置左边框样式使用  <br>border-right 设置右边框，一般单独设置右边框样式使用<br>border-top 设置上边框，一般单独设置上边框样式使用<br>border-bottom 设置下边框，一般单独设置下边框样式使用,有时可将下边框样式作为css下划线效果应用。
- border的默认值为none，即没有边框
- 边框没设置颜色时使用的是前景色，即color
- 边框并不影响行高，会遮挡住上下文内容，左右边框产生填充，不会遮挡内容
- 内边距能填充背景并产生覆盖
- [详情请咨询百度](http://www.baidu.com)
### 定位 ###
- 在CSS中关于定位的内容是：position:relative | absolute | static | fixed  <br>
static 没有特别的设定，遵循基本的定位规定，不能通过z-index进行层次分级。<br>
relative 不脱离文档流，参考自身静态位置通top,bottom,left,right 定位，并且可以通过z-index进行层次分级。<br>
absolute 脱离文档流，通过 top,bottom,left,right 定位。选取其最近的父级定位元素，当父级 position 为 static 时，absolute元素将以body坐标原点进行定位，可以通过z-index进行层次分级。<br>
fixed 固定定位，这里他所固定的对像是可视窗口而并非是body或是父级元素。可通过z-index进行层次分级。<br>
CSS中定位的层叠分级：z-index: auto | namber;<br>
auto 遵从其父对象的定位<br>
namber  无单位的整数值。可为负数
- 个人对相对定位和绝对定位的理解:<br>(1)相对定位只可以在文本流中进行位置的上下左右的移动，同样存在一定的局限性，虽然他的表现区脱离了文本流，但是在文本流却依然为其保留了一席之地，这就好比一个打工的人他到了外地，但是在老家依然有一个专属于他的位置，这个位置不随他的移动而改变。<br>(2)绝对定位不光脱离了文本流，而且在文本流中也不会给这个绝对定位元素留下专属空位。这就好比是一个工厂里的职位，如果有一个工人走了自然会要有别的工人来填充这个位置。而移动出去的部分自然也就成为了自由体。绝对定位将可以通过TRBL来设置元素，使之处在任何一个位置。在父层position属性为默认值时，TRBL的坐标原点以body的坐标原点为起始
- 绝对定位偏移值设为auto时，位置和static定位相同
- 绝对定位会覆盖文本流，相对定位不会
- 对于定位的那些上下左右移动还是不太了解，感觉有点萌萌的！


# 这是我的第二次作业（javaScript） #
### 由于时间紧迫赶下面就列举一些今天上课记录的笔记吧 ###
- JS 中的return、ture、continues关键字如果忘记加结束符的话，机器能自动加上结束符；
- JS中数值都是双精度浮点型，用二进制表示，尽量少使用小数点形式，例如*0.9-0.8！=0.2-0.1*
- 对于==运算符，只要等号两端数值相同即可
- 对于恒等运算符===必须是类型和数值都相同
- 对于Sting类型的必须是完全相等才成立，即是对应字母等不能有偏差，而且存储位置也要相同
- var生成的对象不能被delete
- javaScript数据类型有：number,Boolean,String,null,underfine,object
- 原始值是不能改变的，例如对String对象执行replace操作，只能复制该对象的地址，而不能改变该对象的值
- Nan表示非数字，与任何值都不相等
- \r表示回车符
- 用var声明全局变量
- JS 中没有块作用域
- 属性三特性：可写，可枚举，可配置
- 创建对象的方式：直接创建对象，通过new关键字，object.create
- 函数RegExp,Error,underfine不可序列化和还原
- 插入元素到数组中的方式：push*向数组末尾添加一个或多个元素，且返回新的长度，插入多个元素时保持原来的相对位置*，unshift*向数组开头添加一个或多个元素，且返回新的长度，插入多个元素时保持原来的相对位置*
- 删除数组元素的方法：delete*不改变数组的长度*，pop和shift*能减少数组的长度*
- foreach函数用于读取数组中的所有元素
- 函数表达式必须声明后才可以调用，可以在任何地方声明
- 函数的length属性是指形参的数量

- **AngularJS和Ember.js是前端开发的两大核心技术**