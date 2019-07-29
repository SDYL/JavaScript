# 1.JavaScript前世今生,HelloWorld与开发环境

## JavaScript历史

大概在1992年,一家称作Nombas的公司开始开发一种叫做C--(C-minus-minus,简称Cmm)的嵌入式脚本语言。Cmm背后的理念很简单：一个足够强大可以替代宏操作（macro）的脚本语言，同时保持与C（和C++）中够的相似性，以便开发人员能很快学会。这个脚本语言捆绑在一个叫做CEnvi的共享软件产品中，它首次向开发人员展示了这种语言的威力。Nombas最终把Cmm的名字改成了ScripEase。原因是后面的部分（mm）听起来过于“消极”，同时字母C“令人害怕”。现在ScriptEase已经成为了Nombas产品背后的主要驱动力。当Netscape Navigator崭露头角时，Nombas开发了个可以嵌入网页中的CEnvi的版本。这些早期的试验称为Espresso Page（浓咖啡般的页面），它们代表了每个在万维网上使用的客户端脚本语言。而Nombas丝毫没有料到它的理念将会成为因特网的一块重要基石。  

当网上冲浪越来越流行时，对于开发客户端脚本的需求也逐渐增大。此时，大部分因特网用户还仅仅通过28.8kbit/s的调制解调器来连接到网络，即便这时网页已经不断地变得更大和更复杂。而更加加剧用户痛苦的是，仅仅为了简单的表单有效性验证，就要与服务器端进行多次的往返交互。设想一下，用户填完一个表单，点击提交按钮，等待了30秒钟的处理后，看到的却是一条告诉你忘记填写一个必要的字段。那时正处于技术革新最前沿的Netscape，开始认真考虑一种开发客户端脚本语言来解决简单的处理问题。  

当时工作于Netscape的Brendan Eich，开始着手为即将在1995年发行的Netscape Navigator 2.0开发一个称之为LiveScript的脚本语言，当时的目的是同时在浏览器和服务器（本来要叫它LiveWire的）端使用它。Netscape与Sun公司联手及时完成LiveScript实现。就在Netscape Navigator 2.0即将正式发布前，Netscape将其更名为JavaScript，目的是为了利用Java这个因特网时髦词汇。Netspace的赌注最终得到回报，JavaScript从此变成了因特网的必备组件。  

因为JavaScript 1.0如此成功，Netscape在Netscape Navigator 3.0中发布了1.1版。恰巧那个时候，微软决定进军浏览器，发布了IE 3.0 并搭载了一个JavaScript的克隆版，叫做JScript（这样命名是为了避免与Netscape潜在的许可纠纷）。微软步入Web浏览器领域的这重要一步虽然令其声名狼藉，但也成为JavaScript语言发展过程中的重要一步。

在微软进入后，有3种不同的JavaScript版本同时存在：Netscape Navigator 3.0中的JavaScript、IE中的JScript以及CEnvi中的ScriptEase。与C和其他编程语言不同的是，JavaScript并没有一个标准来统一其语法或特性，而这3种不同的版本恰恰突出了这个问题。随着业界担心的增加，这个语言标准化显然已经势在必行。   

1997年，JavaScript 1.1作为一个草案提交给欧洲计算机制造商协会（ECMA）。第39技术委员会（TC39）被委派来“标准化一个通用、跨平台、中立于厂商的脚本语言的语法和语义”（http://www.ecma-international.org/memento/TC39.htm）
由来自Netscape、Sun、微软、Borland和其他一些对脚本编程感兴趣的公司的程序员组成的TC39锤炼出了ECMA-262，该标准定义了叫做ECMAScript的全新脚本语言。

在接下来的几年里，国际标准化组织及国际电工委员会（ISO/IEC）也采纳ECMAScript作为标准（ISO/IEC-16262）。从此，Web浏览器就开始努力（虽然有着不同程度的成功和失败）将ECMAScript作为JavaScript实现的基础。 

尽管ECMAScript是一个重要的标准，但它并不是JavaScript唯一的部分，当然，也不是唯一被标准化的部分。实际上，一个完整的JavaScript实现是由以下3个不同部分组成的
<ul>
	<li>核心（ECMAScript）——JavaScript的核心ECMAScript描述了该语言的语法和基本对象</li>
	<li>文档对象模型（DOM）——DOM描述了处理网页内容的方法和接口</li>
	<li>浏览器对象模型（BOM）——BOM描述了与浏览器进行交互的方法和接口</li>
</ul>

ECMAScript、DOM、BOM将是我们之后课程的主要内容。


## JavaScript与Java

尽管名字中有Java，但是JavaScript和Java几乎没有什么共同点。Java是一种全功能的编程语言，是由Sun公司开发和推广的。Java是C和C++编程语言之后的又一种主流语言，程序员可以使用它创建完整的应用程序和控制消费电子设备。与其他语言不同，Java宣称具有跨平台兼容性；也就是说，程序员应该能够编写出可以在所有种类的机器上运行的Java程序，无论机器运行的是Windows、Mac OS X还是任何风格的UNIX。但实际上，Java不总是能够实现这个梦想，因为Sun和微软公司在这种语言的发展方向方面有很大的分歧。微软公司首先试图以自己的方式将Java集成到Windows中（Sun认为，这种方式使Java在Windows上以一种方式工作，而在其他机器上以另一种方式工作，从而破坏了Java的跨平台兼容性）；随后，微软公司从Windows中完全去除了Sun的Java，而创建了自己的类Java语言：C#。经过两公司之间的一轮诉讼之后，Sun占据了上风，现在可以在Windows（或Linux）上安装Sun的最新Java版 http://www.java.com/getjava  Mac OS X操作系统在安装时会附带Java。

## JavaScript可以做什么

用JavaScript可以做许多事情，使网页更具交互性，给站点的用户提供更好、更令人兴奋的体验。JavaScript使你可以创建活跃的用户界面，当用户在页面间导航时向他们提供反馈。例如，你可能在一些站点上见过在鼠标指针停留时突出显示的按钮。这是用JavaScript实现的，使用了一种称为翻转器（rollover）的技术
可以使用JavaScript确保用户在表单中输入有效的信息，这可以节省你的业务时间和开支。如果表单需要进行计算，那么可以在用户机器上的JavaScript中完成，而不需要任何服务器端处理。你应该知道一种区分程序的方式：在用户机器上运行的程序称为客户端（client-side）程序；在服务器上运行的程序（包括后面要讨论的CGI）称为服务器端（server-side）程序。
可以使用JavaScript根据用户的操作即时创建定制的HTML页面。假设你正在运行一个旅行指南站点，用户点击夏威夷作为旅游目的地。你可以在一个新窗口中显示最新的夏威夷旅游指南。JavaScript可以控制浏览器，所以你可以打开新窗口、显示警告框以及在浏览器窗口的状态栏中显示定制的消息。JavaScript有一套日期和时间特性，可以生成时钟、日历和时间戳文档。
JavaScript还可以处理表单、设置cookie、即时构建HTML页面以及创建基于Web的应用程序。  

	
## JavaScript不能做什么

JavaScript是一种客户端（client-side）语言；也就是说，设计它的目的是在用户的机器上执行任务，而不是在服务器上。因此，JavaScript有一些固有的限制，这些限制主要出于安全原因：

<li>1.JavaScript不允许读写客户机器上的文件。这是有好处的，因为你肯定不希望网页能够读取自己硬盘上的文件，或者能够将病毒写入硬盘，或者能够操作你计算机上的文件。唯一的例外是，JavaScript可以写到浏览器的cookie文件，但是也有一些限制</li>
<li>2.JavaScript不允许写服务器机器上的文件。尽管写服务器上的文件在许多方面是很方便的（比如存储页面点击数或用户填写的表单数据），但是JavaScript不允许这么做。相反，需要用服务器上的一个程序处理和存储这些数据。这个程序可以是用Perl或PHP等语言编写的CGI或Java程序。</li>
<li>3.JavaScript不能关闭不是由它自己打开的窗口。这是为了避免一个站点关闭其他任何站点的窗口，从而独占浏览器。</li>
<li>4.JavaScript不能从来自另一个服务器的已经打开的网页中读取信息。换句话说，网页不能读取已经打开的其他窗口中的信息，因此无法探察访问这个站点的冲浪者还在访问哪些其他站点。</li>

	


我们的第一个脚本：最经典的HelloWorld程序!
```javascript
<script type="text/javascript">
	document.write("<h2>Hello,JavaScriptWorld!</h2>");
</script>
```

## 开发环境
**选择一个你喜欢的纯文本编辑器或IDE**  
NotePad++  
VIM  
UltraEdit  
EditPlus  
gEdit(Unix)  
Emacs(Mac/Unix)  
其它  

**至少一个符合W3C标准的浏览器（推荐火狐浏览器），和一些市场上流行的浏览器（IE）**  
FireFox 3.0+  
Internet Explorer 6.0+ （由于IE具有多种不同的版本，还推荐安装IETester）  
Google Chrome 1.0+  
Opera 9.0+  
Safari 3.0+  


**调试工具**  
FireFox下的FireBug,Venkman等
IE下的IE DeveloperToolbar,MS Script Debugger等(强烈不推荐MS Script Debugger,安装之后问题多)
Google Chrome 的JS控制台已经很强大了，Opera的错误控制台也可以，Opera蜻蜓和FireBug一样强大，Safari具有和Chrome一样的控制台
