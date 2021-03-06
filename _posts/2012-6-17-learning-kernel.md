---
layout: post
title: 我为何放弃 Linux 内核学习
---

来信:

<blockquote>
    我在国内的技术类网站/博客上, 时常会看到分析linux内核代码的文章.
    图书馆/书店也有国内作者写的 linux 内核书籍.
    经常看到网友在讨论编译内核的事情.
    经过一段时间的 linux 学习, 至今还没发现有学内核的必要.
    我不明白会什么要看 linux 内核代码.
    难道学习 linux, 一定要懂内核吗?
</blockquote>

简短回答：

在一次采访中 Linus 说：如果你在编程中没有涉及到内核的内容，那就不用考虑研究内核，直到有一天你用到了一个让你不太满意的内核接口，你对自己说:" Hey, I can do better... "。 我本人的建议是：水深，危险！用到了最好也别碰。就普通的 Linux 程序员这个人群而言，我是相对花在对 Linux 本身上的时间比较多的，从技术层面讲，使用 Linux，并不意味者你需要去看内核代码，如果真的用到内核相关的东西，也是读一些别人总结好的文档。

下面是完整回答:

我本人的情况是这样，2006开始学习 Linux，因为要做嵌入式项目，直接上手就是内核，06年到08年基本上都像一头猪冲进了原始森林，到处乱撞，受伤很多，收获很少。我目前的主攻方向是 Linux 系统管理和 web app 开发，距离内核方面的知识很远啊，对我来说当初学习内核是个严重错误，所以把我的故事分享在这里，供大家参考。
第一个结论:

### 初学者是不该碰内核的
如果你 C 语言还不太熟练，那抓紧学 C 吧，北京这边我去面试的 Unix 类的公司，基本上笔试都有大量的 C 的内容。当然针对考试而学习是愚蠢的，我这里的意思只是说如果你学了两年多的内核，到最后在面试的时候人家发现你 C 都不过关，那内核的事就基本上不用问了，像我那时就是这样，空中造楼，学了很多内核的知识，最终是一场空。

所以说，我当时倒不如把 C 学好，这样以后不管是向上发展做应用，或是向下做系统编程做内核，知识结构上都是一个更为合理的基础。
然后如果真的想做内核的话，还要有bash脚本的基本功，比较强的各种编程工具的使用技巧。退而言之，内核是世界上最大的软件项目之一，如果你连一个小项目都还没做过的话，着手内核也是明显不合理的。

不过幸运的是我的英文水平还好，同时又会一些 [Qt][qt]，所以毕业以后有幸到 Asianux 工作，维护系统的 updater（就是 apt-get 和 yum 一类的东西），也是从那时开始我才意识到 Linux 真正的魅力在于它是 Internet 的支撑，互联网才是属于我的舞台。所以我最终放弃学习内核倒不是因为困难和挫折，主要还是因为个人的兴趣和价值取向。学编程就跟学音乐学美术一样，作用是表达我们自己的思想，最终目的是能够服务人群。我是那种技术平庸的人，但是我喜欢做东西，同时喜欢像别人炫耀东西，比较人文情怀的一个手工艺人（推荐你看一下 [Hackers and Painters][hp] ），所以我觉得还是做 app 更加的舒畅，因为

### 内核编程是面向硬件的，应用编程是面向人的。

Linus Torvalds 总是说:" My interest has always been how to get hardware to
work ", 由于 Linus 
本人的强大魅力，所以忽悠很多连什么是 software 什么是 hardware 都分不清的年轻人，奋不顾身的投入到内核编程的大军，我本人当初就是这样，不过经过几年我发现其实硬件编程的时代早已经过去了。早期的制造硬件的 Steve
Wozniak，后来赋予人民群众驱动硬件能力的 Linus，都是时代的英雄，而现在这些砖块基石都已经具备，重造车轮没什么意义。所以2000年以来，世界一流的程序员都在关注使用这些砖块表达某种思维，RubyOnRails,
google, facebook...

扯得有点远了，我有一个井底之蛙的结论：国内的情况是搞硬件不太好找工作，找到了也是薪水很低，而且企业文化很差的地方。说的可能有些偏颇，但是记住我本人就是从单片机焊板子过来的，所以这算是一个老青蛙的见解。
我每次见到各个高校电子设计协会的人都会很耐心的劝他们早点放弃硬件投身互联网，赶紧学习 html+css，虽然每次都会遭到鄙视。
搞kernel的人，我见到的发展也不太理想。我在的一个同事，一直负责公司的 kernel 部门，前一段跳槽到 Oracle，不再搞 kernel 了。一个同学以前在 AMD 工作，往 Linus 的 Tree 里打过几个 Patch，现在跳槽到 Intel，做 Andriod，离 kernel 也有十万八千里。

最后，给 Linux 新手的建议是

### 从简单的出发，边做边学

如果上天给我机会重来一次，我会从最简单的开始学，不但不会碰内核代码，语言也会先学一门简单语言例如 Python 或是 Ruby。然后动手做一些简单有趣的网络应用，就像类似于 Facebook 的这种" html + javascript
thing "，然后随着项目作大，可能某些部件需要用 C
 重写才能满足要求，我才会去学 C。好像有人说过，用 C 编程好像穿着旱冰鞋打乒乓球，只有超级聪明的人才能做到。不管是做 C, 还是做 kernel，我的感觉都是 

- NO.1 要有十年左右的计算机软硬件背景，
  半路出家的人最好不要去搞 C。C 编程是很需要计算机科学功底的，像我这种研一才下决心搞编程的人，希望靠毅力解决这个问题，其实是愚蠢的，因为你根本再也抽不出10年的时间补基础。
  所以 python, ruby, java这些东西才是首选。

- NO.2 足够锋利的技术敏锐度。
  如果做了几年，你发现你不是个技术控，这也没准是好事。IT 是个行业，技术水平恐怕对于一个 IT 人是否成功所起的作用还不足5%，更重要的是综合的创造力。
   
我还是坚信由粗到细是计算机教学的正确途径，而不是目前国内大学的这种由细到粗的愚蠢过程。
例证一下我的观点：

- [MIT 的CS教学入门语言是Python][mit]
- [UCB 的RubyOnRails 课][ucb]
 
天气热，大脑工作不太正常，本文跑题可能比较严重，多多原谅。


[hp]:http://www.paulgraham.com/hp.html
[qt]:http://qt.nokia.com
[mit]:http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-00sc-introduction-to-computer-science-and-programming-spring-2011/software/
[ucb]:https://www.coursera.org/course/saas
