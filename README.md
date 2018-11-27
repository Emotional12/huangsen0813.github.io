【重大漏洞预警】Struts 2 远程代码执行漏洞(s2-045s2-046) (含PoC)
背景介绍


近日，安全研究人员发现著名J2EE框架——Struts2存在远程代码执行的漏洞，Struts2官方已经确认该漏洞（S2-045,S2-046），并定级为高危漏洞。

Struts2 的使用范围及其广泛，国内外均有大量厂商使用该框架。

Struts2是一个基于MVC设计模式的Web应用框架，它本质上相当于一个servlet，在MVC设计模式中，Struts2作为控制器(Controller)来建立模型与视图的数据交互。Struts 2是Struts的下一代产品，是在 struts 1和WebWork的技术基础上进行了合并的全新的Struts 2框架。

漏洞描述

使用Jakarta插件处理文件上传操作时可能导致远程代码执行漏洞。

http://p9.qhimg.com/t0180d967ced28d63f5.png

S2-045漏洞影响

攻击者可以通过构造HTTP请求头中的Content-Type值可能造成远程代码执行。
