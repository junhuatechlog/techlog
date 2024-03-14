---
layout: post
title: "TCPIP Volume 1"
date: 2017-04-21
category: "TCPIP" 
tags: [TCPIP]
---


TCP/IP起源于60年代末美国政府资助的一个分组交换网络研究项目，到90年代已发展成为计算机之间最常应用的组网形式。
TCP/IP协议族是一组不同的协议组合在一起构成的协议族。尽管通称称该协议族为TCP/IP，但TCP和IP只是其中的2种协议而已
(该协议族另一个名字是Internet协议族(Internet Protocol Suite)).
### TCPIP Protocol Layers
TCP/IP通常被认为是一个四层协议系统， 每一层负责不通的功能：

链路层(Link Layer, ARP(地址解析协议) 和 RARP(逆地址解析协议)):
有时也称为数据链路层or网络接口层，通称包括OS中的设备驱动程序和对应的网络接口卡。他们一起处理与电缆（或其他任何传输媒介）的物理接口细节。

ARP 和
RARP是某些网络接口（如以太网和令牌环）使用的特殊协议，用来转换IP层和网络接口层使用的地址。

网络层(IP, ICMP, IGMP):
处理分组在网络中的活动，如分组的选路。- Router.

传输层(Transport Layer):
为2台主机上的应用程序提供端到端的通信。TCP & UDP

应用层:
负责处理特定的应用程序细节。 Telnet, FTP, SMTP, SNMP

应用程序通常是一个用户进程，而下三层则一般在(OS)内核中执行。
应用层关系的是应用程序的细节，而不是数据再网络中的传输活动。下三层对应用程序一无所知，但他们要处理所有的通信细节。

以太网协议是链路层的一种协议。链路层（网络接口层）处理有关通信媒介的细节（以太网，令牌环等），
应用层处理某个特定的用户应用程序(FTP, Telnet etc).

路由器(也称IP Router) 工作在IP层，为不同类型的物理网络提供连接:
以太网，令牌环网，点对点连接和FDDI（光纤分布式数据接口)

网桥是在链路层上对网络进行互联，而路由器则是在网络层上对网络进行互联。交换机也工作在链路层. 

应用层和传输层使用端到端(End-to-end)协议. 网络层提供逐跳(Hop-by-hop)协议，2个端系统和每个中间系统都要使用它.

**互联网的目的之一是在应用程序中隐藏所有的物理细节**

在TCP/IP领域中，域名系统(DNS)是一个分布式数据库，由它来提供IP地址和主机名之间的映射信息。


TCP和UDP采用16
bit的端口号来识别应用程序，服务器端一般通过知名端口号来识别。任何TCP/IP实现所提供的服务都用知名的1
- 1023之间的端口号，这些知名的端口号由Internet号分配机构(Internet Assigned
    Numbers Authority, IANA)来管理.


环回接口(Loopback Interface),
允许运行在同一台主机上的client和server通过TCP/IP进行通信。A类网络号129就是为环回接口预留的。一个传给环回接口的IP数据报不能在任何网络上出现。
当环回数据回到上层的协议栈中时，它已经过传输层和IP层完整的处理过程。

TCP/IP成功的原因之一是它几乎能在任何数据链路技术上运行！

在TCP/IP协议族中，链路层主要有3个目的：
    为IP模块发送和接收IP数据报；
    为ARP模块发送ARP请求和接收ARP应答；
    为RARP发送RARP请求和接收RARP应答。



