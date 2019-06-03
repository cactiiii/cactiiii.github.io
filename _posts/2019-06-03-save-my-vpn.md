---
layout: my_post
categories: [other]
---

vultr上搭建的vpn最近被完全墙掉了，到达了它生命周期（流畅-时断时续-完全不能用）的尽头。

是时候做些改变了，网上整理的一些应对方法有：

* 使用obfsproxy对shadowsocks流量进行混淆，应该对防止DPI检测有一些作用
* vpn服务器端口使用443，假装是https流量，作用应该不大
* 使用cisdo anyconnect协议，因为很多跨国企业内部vpn使用的就是这个协议，所以*有可能*降低被墙概率

### cisco anyconnect

新买了kvmla香港的vps，每个月打完折64人民币，先从安装兼容anyconnect的ocserv（openconnect server)开始。[代码](https://gitlab.com/openconnect/ocserv/tree/master)，[主页](http://ocserv.gitlab.io/www/manual.html)。

centos安装epel源的方法：
1 Download latest epel-release rpm from http://download-ib01.fedoraproject.org/pub/epel/7/x86_64/
2 Install epel-release rpm: # rpm -Uvh epel-release*rpm

