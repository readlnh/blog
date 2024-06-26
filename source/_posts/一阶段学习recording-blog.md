---
title: 一阶段学习recording blog
date: 2024-04-28 23:38:44
categories:
    - 2024春夏季开源操作系统训练营
tags:
    - author:<superwyq>
---

## why？

去年秋冬季已经参加过一次训练营了，今年第二次参加，感觉和去年相比，今年的整体流程更加完善了，相应的训练题目也更加合理了。
本身是非科班出身的，一直以来有一个愿望就是弄清计算机是如何运行的，如何从一个个逻辑门到我们所看到的PC，尤其是在软硬件接口处，OS是软件中距离软硬件接口最近的部分，更像是软件领域的“大管家”，如果说编程是创造的过程，那OS就是编程世界的上帝，上帝为程序员准备好了一切支持，程序员才可以进行创造，所以，OS is charming！每个程序员都应该在创造的基础上更进一步，做自己的god。

## Rust

没有最好的编程语言，也没有最好的编程模型，只有最适合的。编程语言的设计需要平衡两件事情：运行速度与抽象程度。越抽象的，越贴近人类思想的，运行速度大概率就越慢，极端情况就是脚本语言。越贴近计算机思想的，运行速度就越快，但是编写起来就越麻烦，极端情况就是二进制指令。
在编程的时候，我们不仅要考虑业务逻辑的实现，还要为自己所写的代码的稳定性和安全性负责，其中最常见的问题就是内存泄漏和并发问题，为了更加贴近人类思想，有些语言会加入GC垃圾处理机制，这种机制可以帮我们实现内存安全，但是代价就是速度，为了并发安全，Python中直接使用了GLI锁，代价也是速度。

C++是什么都没加，是够快，但是代价就是，程序员要负责一切，只有一些基础的安全保障。
Rust的目的就是，在尽量不影响速度的前提下，实现内存安全和并发安全。
但是实际上，有一些算法或者业务逻辑的实现，是不可能在Rust所定义的安全情况下完成的，针对这种情况，Rust提供了unsafe模块，在unsafe包裹的代码中，程序员有更大的自由度，但也不是绝对自由的。

所以，归根结底，想要做到写出的代码具有稳定性以及安全性，Rust只是为我们提供了一个更加完善的支持，但是我们还是要心中对于内存安全和并发安全有相关的概念，才能做到真正安全，GAMES101的闫令琪老师在课上说，API和知识是两码事，学习API不能替代学习知识，对于Rust我想也是这样的，学习Rust的各种语法设置以及安全设置这很重要，但是他们为什么这么设计，为什么这样能实现内存安全和并发安全，这才是更重要的。对于不得不自己实现unsafe代码的这种情景，我不知道是否符合抽象泄漏的定义，但是我想这种不得不亲自上手的感觉是差不多的。Rust就像是我们雇的一个大厨，跟着大厨做饭肯定色香味俱全，但是大厨不可能在任何时间任何地点都陪在我们身边，这种情况就要检验我们自己做饭的水平了。

That is all.

