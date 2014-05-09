---
layout: post
title: "Linus vs. Tanenbaum译稿(3)"
category: computer related
tagline: Linux过时了
category: 软件设计
tags: [os, debated]
---

发信人: comm121@unixg.ubc.ca (Louie)<br/>
主题: 回复：Linux过时了<br/>
日期: 30 Jan 92 02:55:22 GMT<br/>
组织机构: University of British Columbia, Vancouver, B.C., Canada

　　在文章12595@star.cs.vu.nl中ast@cs.vu.nl (Andy Tanenbaum) 说:

>　　但凭心而论，对于那些想要一个够现代够免费的OS的人们，我真心建议他们找一个基于微内核的可移植的OS，比如像GNU或者其他类似的。

　　对于像我一样想要一个”自由”操作系统的人来说，除了Linux好像真的没什么选择了。考虑到绝大多数人用的都是386，可移植性也基本不是什么大事啦。如果我有一台Sparc计算机，我会用Solaris。

　　值得一提的是，我不费吹灰之力装了linux，还在上面装了gcc，emacs 18.57，kermit和其他的GNU工具包。我就按着安装步骤一步步来的，也没有打任何补丁。如果不是Linux，我想我不管在哪儿不可能以如此低的成本搞到这么像样的一个OS来做我计算机科学的作业了。并且它似乎还支持网络，X-Window很快也会移植到Linux上，这一点又要比Minix捷足先登了。Linux真是实用。在我看来，标准UNIX软件的可移植性也很重要。

　　我也知道宏内核的设计不如微内核好。但是如果就看这一个学期(我知道这个学期我也只能用386了)的话，Linux完全适合我。

Philip Wu<br/>
pwu@unixg.ubc.ca

----------
发信人: dgraham@bmers30.bnr.ca (Douglas Graham)<br/>
主题: 回复：Linux过时了<br/>
日期: 1 Feb 92 00:26:30 GMT<br/>
组织机构: Bell-Northern Research, Ottawa, Canada

　　在文章12595@star.cs.vu.nl中ast@cs.vu.nl (Andy Tanenbaum) 说道:

>　　如果要争论这两种设计的优缺点，我可以花很多篇幅来讲。但是如果让那些真正设计过操作系统的人来说，这场争论毫无异议已经结束。微内核赢了。

　　你可以推荐一些(无偏见的)分析这两种设计优缺点的文献么？我知道肯定有一些讲微内核的文章，但是我怀疑的是Minix究竟和其他用微内核的系统有几分相像？不错，Minix用了不少的任务和消息，但是微内核的架构肯定不止这么些东西。我怀疑minix的代码在任务区分上是不是最优的。

>　　微内核赢了。宏内核现今唯一拿的出手的只剩下了性能。——可惜现在有足够多的证据表明微内核也能和宏内核跑的一样快(如 Rick Rashid 已经发表的关于对比Mach 3.0和宏内核性能的论文)。所以，一切争论已经结束，剩下的都是瞎嚷嚷了。

　　我对Minix最想抱怨的地方不是性能，而是要给它添加新的特性是不是会让人苦不堪言——按理来说这对微内核架构应该要容易些。

>　　MINIX是微内核系统。

　　这么说大家都同意么？

>　　Linux是宏内核的.这完全是倒退到了20世纪70年代。这好比用Basic来重写一个已经出色工作的C语言程序一样。对我而言，在1991年写一个宏内核系统真是一个糟糕的主意。

　　这样的断言真是不错，但还是想听听你是怎么分析的。我琢磨Linux顶多也就12000行代码。我看不出怎样把它们分到不同的任务里然后再加一堆破破烂烂的消息才能对Linux有所提升。

>　　别误会我，我不是对Linux不满意。这会使得那些想从Minix换到BSD UNIX的人对我唠叨个不停。但凭心而论，对于那些想要一个够现代够免费的OS的人们，我真心建议他们找一个基于微内核的可移植的OS，比如像GNU或者其他类似的。

　　好吧，最近我没注意到有什么别的选择了。但是如果GNU OS出现了，它可能还是很有吸引力的。我总觉得你对Linux多少有点不太满意(这也多少让我有些吃惊)。我只好猜想这是因为有这么多的人都投向它的怀抱，毕竟它提供了更多的特性。面对人们对新特性的诉求，你的处理方式已经渐渐让大家觉得他们再也得不到那些特性了。我的结论就是人们成批的转向Linux证明你错了。

　　免责申明: 我和Linux开发没任何关系的。我只是发现它是一个比Minix更易懂的系统。

Doug Graham<br/>
dgraham@bnr.ca<br/>
观点全来自个人

----------------------
发信人: hedrick@klinzhai.rutgers.edu (Charles Hedrick)<br/>
主题: 回复：Linux过时了<br/>
日期: 1 Feb 92 00:27:04 GMT<br/>
组织机构: Rutgers Univ., New Brunswick, N.J.

　　软件的历史告诉我们可用性每次都能完胜优秀的技术。这是Linux最大的优势。它基于386，系统极为精巧，和通用UNIX兼容的非常好，而且还是自由开放的。几年前我就舍弃了Minix社区，因为那个时候以下几点已经变得很明显了：

　　(1)Minix在未来几年一点都没有要利用比8086更高级的特性的意思。

　　(2)许可证——尽管还是及其友好的——但仍旧很难让对其有兴趣的人们开发一个386的版本。有好几个人明显已经在386上做出了相当出色的工作了，但他们只能用diff给源代码发布补丁。这让新手想装一个386的系统变得不切实际，事实上我也不太确定我是不是愿意这么搞。

　　如果最近几年发生了新的动向，我在此致歉。如果现在有希望以某种形式搞到一个386版本拿来就能跑，而且社区也已经开发出一种共享Minix源代码的方式，而且在期间跑常规的UNIX程序变得容易了的话，我还是愿意重新考虑一下Minix的。我真心喜欢这个架构。

　　Linux也不是没有可能不会被GNU或者是BSD取代。但是如果GNU的操作系统也像其他的GNU软件一样的话，那么它至少也得需要128M的内存和1G的硬盘。再放一个小点的系统还是有空间的。我理想中的OS其实是4.4BSD。但是4.4向来喜欢长时间延期发布。一想到他们大部分成员都搬到了BSDI(Berkely Software Design Inc，伯克利软件设计公司)，我就打死都不会相信这一点会有所改善。就我个人使用经验来看，BSDI的系统可能会比较给力。但是他们那些”诱人”的价格也极有可能对我们大部分学生都高的吓人。就算用户能从他们那儿拿到源代码，但是软件的所有权却再次意味着你没有权利把修改后的代码发布到FTP上。无论如何，现在有Linux了，让剩下的那些选择们吹他们的大牛去吧。

----------
发信人: tytso@athena.mit.edu (Theodore Y. Ts'o)<br/>
主题: 回复：Linux过时了<br/>
日期: 31 Jan 92 21:40:23 GMT<br/>
组织机构: Massachusetts Institute of Technology

　　ast@cs.vu.nl (Andy Tanenbaum)说：

>　　我认为为一个特定的系统结构设计一款内核显然是个错误，因为这样的内核必然不能走远。

　　认为Linux紧密依附于80386，这不是你的错，因为这么多的Linux拥护者(包括Linus自己)都是这么声称的。然而，Linux里与386相关的代码量比Minix的实现里大概也多不了多少，并且和4.3BSD里与VAX相关的代码量比起来，它的量明显要少得多。

　　但是，向其他体系结构的移植还没有开始呢。但如果让我在新的体系结构下面做一个类UNIX系统，我宁愿用Linux也不用Minix，很简单，至少在我的系统完成了之后我还是想对我的系统有点儿控制力的。不错，我肯定得为设备驱动和虚拟内存重写大量的代码——但是换哪个系统不是这样呢？或许和Minix比起来把Linux移植到新的体系结构上要难上那么一点点；但这仅仅适用于我们要移植的第一个新体系结构。

>　　如果要争论这两种设计的优缺点，我可以花很多篇幅来讲。但是如果让那些真正设计过操作系统的人来说，这场争论毫无异议已经结束。微内核赢了。宏内核现今唯一拿的出手的只剩下了性能。——可惜现在有足够多的证据表明微内核也能和宏内核跑的一样快(如 Rick Rashid 已经发表的关于对比Mach 3.0和宏内核性能的论文)。所以，一切争论已经结束，剩下的都是瞎嚷嚷了。

　　这根本不是这么回事么。我想你肯定在现实基础上添油加醋了不少。我推荐你看点其他类的论文，比如Brent Welsh(welch@parc.xerox.com)的”文件系统应该包含在内核内部”。在这篇论文里它论述了文件系统作为一个成熟的抽象层，它应当包含在内核中，而不应该像微内核的设计那样在内核之外。

　　也有一些人在把OSF/1的Mach和宏内核系统做了对比后研究过它的性能；尤其是在管理网络通信时其所需的上下文切换的次数，举个更特殊的情况如网络文件系统。

　　我对微内核实现上有哪些优势还是一清二楚的。但是事实就是这样：Linux已经能用了，而GNU内核还不知道在哪里——并且人们在Hurd上面花的时间要比Linus在Linux上花的时间多多了。

　　我觉得在微内核还是宏内核的权衡上完全取决于你到底想干什么。如果你的兴趣是做研究，那么在微内核里删除替换一些模块那是容易的多，并且也就搞研究的家伙们发发OS的论文，照这个事实微内核肯定是正道。但是，我的确也认识很多别的人，他们不是研究人员，但他们是实实在在的内核程序员，他们更关心的是在微内核里内存复制的开销和上下文切换上的开销。

　　顺带说一句，你说你在单用户系统里用不着多线程的文件系统，我一点都不买你这个账。一旦你启动了一个窗口系统，并且一个窗口里运行了一个编译器，另一个窗口里运行了一个新闻组阅读器，并且UUCP(UNIX-to-UNIX Copy, 另外一个协议，在Intenet流行之前用的很多)新闻源源不断的从后台涌出，到这个时候你就想要一个性能好点的文件系统了，就算你跑的是单用户。也许对于一个理论家，这只是一个没用的优化，也只是一个”性能上的技巧”(盗用你的词)，但我感兴趣的是真正的操作系统——不是拿来做研究的玩具。

Theodore Y. Ts'o

----------
发信人: joe@jshark.rn.com<br/>
主题: 回复：Linux过时了<br/>
日期: 31 Jan 92 13:21:44 GMT<br/>
组织机构: a blip of entropy

　　在文章12595@star.cs.vu.nl中ast@cs.vu.nl (Andy Tanenbaum) 说到:

>　　MINIX在移植性上的设计较为合理。并且已经从英特尔的处理器移植到了68000,SPARC,和NS32061的芯片上。

　　如果你在相信作者之前看看源代码，你就能知道这根本就是在吹牛。

　　他把’fubyte’替换成了一个函数，函数里还显式的使用了一个段寄存器。——但那明明很容易就能改掉。

　　类似的，一些地方假定使用了386的MMU，其他地方用几个宏把真正的页面大小隐藏起来也让移植变得非常琐碎。用386的TSS能让代码简单一些，而且VAX和WE32000里也有类似的结构啊。

　　他自己也承认过：再多花点时间设计，系统代码可能会更整洁些，但放点386汇编也不算为过啊。

　　其实恕我直言：

　　——全书(译者注：指Tanenbaum写的《操作系统，设计与实现》一书，在书中他用Minix作为示例讲解操作系统的实现)压根就没有提过可移植性的话题(除了一些“#ifdef M8088”的宏)

　　——在minix发布的时候，它已经依赖了很多8086的特性，这让68000的用户们颇为不满。

joe

----------
发信人: entropy@wintermute.WPI.EDU (Lawrence C. Foard)<br/>
主题: 回复：Linux过时了<br/>
日期: 5 Feb 92 14:56:30 GMT<br/>
组织机构: Worcester Polytechnic Institute

　　在文章12595@star.cs.vu.nl中ast@cs.vu.nl (Andy Tanenbaum) 说到：

>　　别误会我，我不是对Linux不满意。这会使得那些想从Minix换到BSD UNIX的人对我唠叨个不停。但凭心而论，对于那些想要一个够现代够免费的OS的人们，我真心建议他们找一个基于微内核的可移植的OS，比如像GNU或者其他类似的。

　　我相信你讲这话的时候肯定是有事实依据的，尽管我还不太确信微内核到底是不是更好一点。如果能把这二者有所结合的话兴许还更合理些。我最近在给Linux写进程间通信，我准备添加一些代码让文件系统和设备驱动在用户进程中运行。这将明显会降低性能，我也相信把所有东西都放到内核外是不明智的(TCP/IP肯定会在内核里面的)。

　　其实我对OS理论家们的主要问题是他们是不是从来不测试他们的想法的。这些主意看上去没一个靠谱的(Mach可能部分算得上一个意外)。32位的家庭电脑都流行了10多年了，但写一个能用的操作系统让大家省得花100000美元向AT&T买，Linus是第一人。一个手头能用的软件要比一堆不切实际的破烂有价值的多，OS理论家们指责起一个系统来倒是轻轻巧巧，但他们从来都不愿意提供一个选择给大家。

　　如果一个微内核上面从来都没跑过一个实际的应用程序，那么”微内核是发展趋势”这种论断就必然狗屁不通。

　　Linux的发布给了我一个机会让我尝试一些我好几年前就想试验的点子，之前我还没有过任何机会给一个运作良好的操作系统维护源代码。

--------
发信人: ast@cs.vu.nl (Andy Tanenbaum)<br/>
主题: 回复：Linux过时了<br/>
日期: 5 Feb 92 23:33:23 GMT<br/>
组织机构: Fac. Wiskunde & Informatica, Vrije Universiteit, Amsterdam

　　在文章1992Feb5.145630.759@wpi.WPI.EDU中entropy@wintermute.WPI.EDU (Lawrence C. Foard)说:

>　　其实我对OS理论家们的主要问题是他们是不是从来不测试他们的想法的。

　　这简直是奇耻大辱。我不是什么理论家。不信去问问昨天在我们系开会的人们(开玩笑啦)。

　　事实上，这些想法已经在实践中做了很好的测试。OSF把它们整个商业业务的宝都押在一个微内核上(Mach3.0)。USL则押在另一个上(Chous)。这两个系统上都跑了大量的软件，并且他们也都和宏内核的系统做了广泛的对比。Amoeba有完整的实现，也用大量的软件做了测试。QNX是一个基于微内核的操作系统，有些人告诉我其安装量达20 0000。微内核不是白日做梦。事实证明它们代表了技术。

　　研究Mach的人们写了一篇名为”让UNIX作为一个应用程序”的论文。是Golub等人写的，发表在1990年夏天的USENIX会议上。Chorus的研究者们也有一篇关于微内核性能的技术报告，在这个话题上我也和别人合写过另一篇文章，昨天我刚提过(1991年12月发表在Computing Systems上)。你可以看一下。

Andy Tanenbaum (ast@cs.vu.nl)

---------
发信人: peter@ferranti.com (peter da silva)<br/>
主题: 回复：Linux过时了<br/>
组织机构: Xenix Support, FICC<br/>
日期: Thu, 6 Feb 1992 16:02:47 GMT

　　在文章12747@star.cs.vu.nl中ast@cs.vu.nl (Andy Tanenbaum) 说到:

>　　QNX是一个基于微内核的操作系统，有些人告诉我其安装量达20 0000。

　　好吧好吧，既然我扯进这个话题了….Amigas还超过三百万呢，这意味着它要比任何一个UNIX发行商卖出的量都多，或许比所有的UNIX系统加起来都多。

-----------
发信人: peter@ferranti.com (peter da silva)<br/>
主题: 回复：Linux过时了<br/>
组织机构: Xenix Support, FICC<br/>
日期: Thu, 6 Feb 1992 16:00:22 GMT

　　在文章1992Feb5.145630.759@wpi.WPI.EDU中entropy@wintermute.WPI.EDU (Lawrence C. Foard) 说到:

>　　其实我对OS理论家们的主要问题是他们是不是从来不测试他们的想法的。

　　恕我略有微词...有那么多的微内核操作系统呢，从8088（QNX）到大型的研究性系统，它们有各种产品。

>　　这些主意看上去没一个靠谱的(Mach可能部分算得上一个意外)。32位的家庭电脑都流行了10多年了，写一个能用的操作系统让大家省得花100000美元向AT&T买，Linus是第一人。

　　这些年我肯定生活在AmigaOS的幻觉里。对于这个我意淫出来的系统，我已经用了6年了。

　　AmigaOS作为一个微内核系统，其设计理念是消息传递，其响应时间和性能都强过现在任何一个能用的操作系统：包括minix，OS/2，Windows，MacOS，Linux，UNIX，当然还有MS-DOS。

　　事实证明微内核设计是无价之宝。像新型文件系统之类的东西，本来你只能从发行商那里得到，而在Amiga上总会有内核爱好者帮你实现出来。设备驱动要么就是共享库，要么就是入口地址和消息端口都固定的任务。像这样的模块还有文件系统，窗口系统，不一而足。它的设计简直棒极了，也证实了人们对微内核的一切预期。不错，要让他们顺畅运行，比起一个像UNIX一样基于宏内核的多任务系统来说，得多花点时间，但考虑到其完善性，这是件一劳永逸的事。

　　我真心希望Andy能吸取之前发布版的经验教训再做一个新的MINIX。MINUX做的有点太不负责了，但是它的基本理念还是相当不错的。

>　　如果一个微内核上面从来都没跑过一个实际的应用程序，那么”微内核是发展趋势”这种论断就必然狗屁不通。

　　我又开始产生幻觉了。我深信Deluxe Paint, Sculpt 3d, Photon Paint, Manx C, Manx SDB, Perfect Sound, Videoscape 3d还有其他我为我Amiga买的软件是”真实存在”的。我估计得把这些该死的东西退回去了。

　　Linux自由好用是相当不错。它的存在很让我高兴。我也知道它能够如此迅疾得以实现的一个原因是它采用了宏内核的架构，这也是采用宏内核一个很正当的缘由。但是，这并不意味着微内核天生就很慢，或者仅仅只是一个用来研究的玩具。