---
layout: post
title: 继续LFS
description: 继续LFS
categories: Old
tags: Old
---
这几日还是忍不住在机子上狂编译LFS了。换了个6.2版，虚拟机的速度还是可以忍受，起码比家里的赛扬366快2倍。。

暑假在家的时候，用这台闪龙2600+已经成功编译了一遍，不过立马就要翻学，so也没继续BLFS。不过BLFS真的挺有趣，希望这次LFS能成功让我继续下去。

这一遍编译也让我对建造一个Linux系统有了更深入的了解。基本上，整个Linux的编译就靠三大件：binutils，glibc，gcc。LFS的工具链（toolchain）里所指的基本工具也就是以上三个，其意念是：首先利用母系统的编译工具编译出临时的编译工具，再用临时的编译工具编译出子系统的编译工具，最后用子系统的编译工具编译出子系统。其间要不断调整系统编译器的指向，最终目的是让子系统完全独立于母系统，能自行编译任何程序。

现在在虚拟机的LFS已进入到自行编译阶段，不过中途出了次胆战心惊的意外，编译gcc的途中去睡了个午觉，起来居然发现死机了，狂晕~~，原因不明。后来重新编译一次了事，没出差错，不过后来的几次make check里出了些令人不安的error，没敢去查，怕承受不了失败，继续编译下去算了，不行再重来吧。明晚继续。

This entry was posted on Friday, September 8th, 2006 at 1:23 am.

---



-EOF-