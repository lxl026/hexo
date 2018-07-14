---
title: Linux学习之路0x01——什么是Linux
date: 2018-07-12 14:06:18
tags:
	- Linux
---


*本系列文章主要记录本人学习[《鸟哥的Linux私房菜》](http://linux.vbird.org/)过程中的重点难点。之前也有学习过Linux，但都是半途而废，现在希望有所记录，有所收获，坚持不懈。*

知道Linux很久了，但是稍微一问细些，如RedHat是什么、Debian是什么、Ubuntu和CentOS的区别是什么等等这些问题，都是一头雾水。本文从Unix开始，简单梳理Unix和LInux的历史过程，以及各个Linux相关概念，主要理清Unix、Linux、GNU的关系以及区分Linux kernel与Linux Distributions。

## Unix与Linux的历史

- 1969年以前，Bell、MIT、GE合作开发“Multics”系统
- 1969年，Bell实验室退出合作计划，Bell的Ken Thompson 用汇编语言写出了Unix原型Unics
- 1973年，Ritchie等人用C语言写成第一个正式的Unix核心
- 1977年，BSD诞生：Berkeley大学的Bill Joy在Unix的核心代码上着手修改，命名为Berkeley Software Distribution
- 1979年，Unix的第七版System V可以支持x86架构，Unix版权被AT&T收回
- 1984年，Andrew Tanebaum（谭宁邦）开始开发Minix，1987年发布；Richard Mathew Stallman发起GNU计划
- 1988年前后，Linus Torvalds不满于Minix，开始用GNU计划中的bash工作环境软件和gcc编译器撰写操作系统核心
- 1991年,Linus Torvalds初次释出Linux核心 0.02，参考POSIX规范，相容于Unix
- 1994年，在虚拟团队的共同努力下，Linus发表Linux正式核心1.0
...

## Linux Distributions

从前面的历史中可以看到，Linus基于GNU计划开发出Linux**核心**与核心工具。
而Linux Distribution则是kernel+Softwares+Tools，各个Distribution需遵循Linux Standard Base（LSB）、Filesystem Hierarchy Standard（FHS）等标准规范。
Distributions主要分为两大系统，一种是使用RPM（Red-Hat Package Manager）方式安装软件的系统，另一种是使用DPKG（Debian Packager）方式安装软件的系统

|   | RPM  | DPKG  | others  |
| ------------ | ------------ | ------------ | ------------ |
| 商业公司  | RHEL（Red Hat公司）SusE  | Ubuntu  |   |
| 社群单位  | Fedoras CentOS openSuSE  |  Debian B2D | Gentoo  |

商业公司一般依靠后续支持与维护获得收益。
CentOS：由社群支持的包，旨在100%地与Red Hat Linux企业版兼容，但不包含Red Hat的商业软件。
Ubuntu：知名Linux发行版之一，由Canonical有限公司赞助，基于Debian，使用自己的软件包库，与Debian的有所不同，旨在开发出更加友好的桌面。
Gentoo：这个包采用自己独特的Portage包管理系统，吸引了许多狂热爱好者以及专业人士，由于能自己编译及调整源码依赖等选项，而获得至高的自定义性及优化的软件，在源码包也有相当多新旧版本的选择，是个强调能自由选择的发行版。





