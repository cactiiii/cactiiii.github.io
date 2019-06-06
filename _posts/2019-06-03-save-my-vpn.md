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

新买了kvmla香港的vps，每个月打完折64人民币，先从安装兼容anyconnect的ocserv（openconnect server)开始。

centos安装epel源的方法：
1. Download latest epel-release rpm from http://download-ib01.fedoraproject.org/pub/epel/7/x86_64/
2. Install epel-release rpm: # rpm -Uvh epel-release*rpm

安装过程参考：
* 代码：[https://gitlab.com/openconnect/ocserv/tree/master](https://gitlab.com/openconnect/ocserv/tree/master)
* 项目主页：[http://ocserv.gitlab.io/www/manual.html](http://ocserv.gitlab.io/www/manual.html)
* 博客：[https://blog.csdn.net/tty521/article/details/81005213](https://blog.csdn.net/tty521/article/details/81005213)
* iptables详解：[http://www.zsythink.net/archives/1199/](http://www.zsythink.net/archives/1199/)

### obfs4proxy

目前还没有搭建obfs4proxy，下面是收集的一些资料，供后续使用。

* 项目地址：[https://github.com/Yawning/obfs4](https://github.com/Yawning/obfs4)
* 配置方式参考：[https://www-dc1-n1.sparklabs.com/support/kb/article/setting-up-an-obfuscation-server-with-obfsproxy-and-viscosity/](https://www-dc1-n1.sparklabs.com/support/kb/article/setting-up-an-obfuscation-server-with-obfsproxy-and-viscosity/)。
* windows下的obfs4proxy.exe可以从下载的Tor Browser目录中找到
* 如何配置systemd/serive：[http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-part-two.html](http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-part-two.html) 
* 两个启动obfs4proxy的工具：[ptproxy](https://github.com/gumblex/ptproxy)和[ptadapter](https://twisteroidambassador.github.io/ptadapter-docs/index.html)。
* 使用obfs4proxy + ptproxy的一篇博客：[https://typeblog.net/obfourscating-shadowsocks-with-obfs4/](https://typeblog.net/obfourscating-shadowsocks-with-obfs4/)

