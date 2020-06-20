# 10.Shell Programe

为什么要有Shell编程?
没有一种编程语言是完美的，甚至也没有一种最好的语言；只有一种非常合适或可能非常不合适实际目标的语言。 （Herbert Mayer）
脚本应用知识对于希望相当精通系统管理的任何人来说是必需的，即使他实际上并不想写一个脚本程序。

一般来说一个Linux机器启动后，它会执行在/etc/rc.d 目录下的Shell脚本重建系统环境并且启动各种服务。
理解这些启动脚本的细节对分析系统运作行为并修改它是意义重大的。

编写shell脚本不是很难学，因为脚本内建的功能集（check?）和他们只有相当少的shell的操作符和选项 需要学。
语法非常的简单易懂，就像在命令行上调用和连接软件包一样容易，它仅有一些少量的 "规则" 需要掌握。
大多数短小的脚本第一次就工作的很好，即使是较长的脚本调试也相当的容易。

shell脚本是一个复杂应用原型的"quick and dirty" 方法。
在项目开发中用shell编程实现一个有限的功能性子集常常是有用的开始。
用这种方法去测试应用程序的结构和模块组合，可以在实际地用C,C++,Java或者Perl进行编程之前发现主要的设计缺陷。

Shell编程遵从经典UNIX哲学：
把复杂的问题分解成简单的小问题，然后再把各部分功能组合起来解决复杂问题。
这和用新一代高级的多用途的语言，例如Perl，试图成为所有人处理所有事情的语言，
但是所付出的代价是强迫改变你的思维方法来适应这种工具，大多数人认为这是一个更好的或者至少感觉上更令人能接受的方法。

什么时候不适合使用Shell编程：
资源紧张的项目，特别是那些速度是重要因素的地方（排序，散序，等等）
程序要进行很复杂的数学计算，特别是浮点计算，任意精度的计算，或者是复数计算（应该用C＋＋或是FORTRAN代替）
要求交叉编译平台的可移植性（使用C或者是Java代替）
需要结构化编程的复杂应用（需要变量类型检查和函数原型等等）
对于影响系统全局性的关键任务应用。
安全非常重要。你必须保证系统完整性和抵抗入侵，攻击和恶意破坏。
项目由连串的依赖的各个部分组成。
多种文件操作要求（Bash被限制成文件顺序存取，并且是以相当笨拙，效率低下的逐行的存取方式）
需要良好的多维数组支持。
需要类似链表或树这样的数据结构。
需要产生或操作图象或图形用户界面。
需要直接存取系统硬件。
需要端口号或是socket I/O。
需要使用可重用的函数库或接口。
所有的私有的不开源的应用程序（Shell脚本的源代码是直接可读，能被所有人看到的）

如果你需要有上面的任意一种应用，
请考虑其他的更强大的脚本语言――Perl,Tcl,Python,Ruby，
或者可能是其他更高级的编译型语言，例如C，C＋＋或者是Java。
尽管如此，使用Shell脚本来构造应用原型仍然是一个有用的开发步骤。
