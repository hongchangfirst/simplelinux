<a name="top"></a>

<h1 align="center"><b>朴素linux</b></h1>

　　大学里我坚持的最久的一项任务就是自学 linux 内核，
虽然以后可能也没机会从事 linux 内核方面的工作，
但是至少提升了自己的编程水平。

　　linux 最新内核的源代码已经没有进行全面研究的可能了，
我看的是 linux0.01 的内核源码。
没有指导直接看源代码是不太容易看懂的，
因为其中涉及到不少硬件操作的规范，
《linux内核完全注释2.01》——赵炯 著 
对早期linux内核的分析是最详细的，真的达到了完全注释的地步，
虽然书里分析的是 linux0.11 的源代码，
但相对于 0.01 的改动不多。

　　而最新的内核由于巨大的代码量，
要达到源代码的完全注释应该是不可能的了，
但是从大粒度上进行的分析也是很有价值的。
《Linux内核设计与实现》英文名为 
*Linux kernerl Development* ，
是 *Robert Love* 所著，陈莉君、康华、张波 翻译的，
我从这本书中了解了最新内核的进程调度思想。

　　还有一本书，书名是《LINUX内核源代码情景分析》 
毛德操 胡希明 著，这本书对于 PCI 
总线操作规范的介绍可谓完全注释。为什么我会看 PCI 
总线的操作？因为现在的电脑都是用 PCI 而非早期的 ISA 
总线了，linux0.01 对硬盘的操作使用 ISA 规定的固定端口，
而 PCI 总线中的硬盘的端口是动态设定的，
与 ISA 时的端口不一致了，所以如果想用 linux0.01 
读写我本机的硬盘的话就得加入 PCI 的功能，
所以我才看关于最新内核的书，我是被逼的。

　　就快要毕业去工作了，想着写几篇文章同大家分享一下 
linux 和 C 语言方面的底层知识。那些既想了解底层
又不愿意系统地看源代码或操作系统方面书籍的同学可以来看看，
就当是看一部小说吧。
这个系列的名字叫<b>朴素linux</b>。

　　以下是目录，目录随着进度变更，
还有可能被重新分类整理，请见谅。

<a name="content"></a>

* 解剖C语言
	1. [照妖镜和火眼金睛](https://github.com/1184893257/simplelinux/blob/master/gcc.md#top) \[2012/11/8更新](3)
	2. [局部变量](https://github.com/1184893257/simplelinux/blob/master/localvar.md#top) \[2012/11/7上线](4)
	3. [全局变量](https://github.com/1184893257/simplelinux/blob/master/globalvar.md#top) \[2012/11/8上线](5)
	4. [函数调用](https://github.com/1184893257/simplelinux/blob/master/call.md#top) \[2012/11/9上线](6)
	5. [值传递](https://github.com/1184893257/simplelinux/blob/master/byval.md#top) \[2012/11/11上线](7)
	6. 数组与指针 \[预计2012/11/13上线](8)
	7. 字符串 \[预计2012/11/15上线](9)
	8. 结构体 \[预计2012/11/17上线](10)
	9. 奇怪的宏 \[预计2012/11/19上线](11)
* 内核小知识
	1. [linux0.01进程时间片的消耗和再生](https://github.com/1184893257/simplelinux/blob/master/process0.01.md#top) \[2012/11/7更新](1)
	2. [linux2.6.XX进程切换和时间片再生](https://github.com/1184893257/simplelinux/blob/master/process2.6.md#top) \[2012/11/7上线](2)
