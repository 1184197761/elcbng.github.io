---
layout: note
title: 网络基础知识
author: hanhansun233
category: 2020暑假第一周
date: 2020-07-19
---

## 网络基础知识

### 局域网

局域网（英文名字Local Area Network，缩写为LAN），是指在某一区域内由多台计算机互联成的计算机组。覆盖范围小，自己花钱购买设备， 带宽固定10M 100M 1000M，自己维护。以太网和Wi-Fi(无线网络连接)是现今局域网中最常用的两项技术。比如家庭网络就是一个小型的局域网，一般包含一个运营商免费送的光猫，由于光猫无线信号不好，用户会光猫的LAN口接上一个无线路由器，于是就有了小型的家庭局域网。

代表：家庭Wifi 网吧CS

### 广域网

英语名为Wide Area Network，缩写为 WAN，又称广域网、外网、公网。是连接不同地区局域网或城域网计算机通信的远程网。如果需要长距离的传输，比如某大型企业，总部在北京，分公司在长沙，局域网是无法架设的，这时需要通信有三个解决方案。

第一，通过因特网，只需要办一根宽带，就实现了通信，非常方便，现在的宽带价格也比较便宜。但是会存在数据泄露的风险，所以大型企业、金融单位、各级政府单位，是不放心使用因特网来传输数据的。

第二，通过广域网专线。所以为了数据安全，不能连接因特网，需要用一条自己的专用线路来传输数据，这条线路上只有自己人，不会有其他人接入，且距离很远，这个网络就叫 “广域网”。

第三，通过VPN。VPN是虚拟专用网，是在普通的便宜的因特网上，通过数据加密，完整性验证，身份验证等多种技术手段构建的安全传输网络，实现类似专线的安全功能。

### 互联网

互联网就是由无数个局域网，通过WAN线路汇聚到运营商，然后运营商之间互联起来，就形成了互联网。互联网开放、互联，如果一个公司、机构的局域网没有连接到互联网，那这个局域网就不属于互联网。（即互联网是广域网的一种，但广域网不一定是互联网，如电力调度网络、大型跨地区企业的内部网络，这些网络往往不会和Internet连接，或者是不直接连接。）

### IP地址

IP地址（Internet Protocol Address）是指互联网协议地址，又译为网际协议地址，是IP协议提供的一种统一的地址格式，它为互联网上的每一个网络和每一台主机分配一个逻辑地址，以此来屏蔽物理地址的差异。

**公有地址**

公有地址（Public address）由Inter NIC（Internet Network Information Center因特网信息中心）负责。这些IP地址分配给注册并向Inter NIC提出申请的组织机构。通过它直接访问因特网。

**私有地址**

私有地址（Private address）属于非注册地址，专门为组织机构内部使用，*私有 IP 不能直接上网。*

*局域网和公网是怎么交互呢？*

假设有两台主机A和B，他们分别处于不同的局域网下，他们的局域网IP都是相同的。在同一个时刻，他们都访问百度服务器，那作为百度服务器是怎么分别回复这两台主机的呢？或者是服务器怎么区分A和B呢？

而我们平时通过运营商（主要是电信、移动、联通宽带等）上网，通过家用路由器之后，就会变成私有IP。通俗的讲，运营商有公有IP，但是IPV4下IP资源有限，所以这些IP不能每个人分配单独分配一个IP，所以需要动态给上网的用户。当用户有上网需求时，需经过运营商，运营商那边会做相应的端口映射（而且是动态端口映射），将子网 IP转化为公网 IP，通过这个公网 IP 去访问百度服务器。

### MAC地址

MAC地址（英语：Media Access Control Address），直译为媒体存取控制位址，也称为物理地址（Physical Address），它是一个用来确认网络设备位置的位址。MAC地址用于在网络中唯一标示一个网卡，一台设备若有一或多个网卡，则每个网卡都需要并会有一个唯一的MAC地址。

按照原理性可将计算机网络分为5层
1. 物理层
2. 数据链路层
3. 网络层
4. 传输层
5. 应用层

### 物理层

物理层考虑是如何将采集的信号转化为二进制数据，用什么介质传输信号等等。

数据单元：数据位（bit）binary digit 二进制数据的缩写

### 数据链路层

数据链路层工作在物理层之上，负责给这些二进制信息制定传送的规则，然后另一方再按照相应的规则来进行解读。

数据单元：数据帧 （Frame）

以太网协议规定，一组电信号构成一个数据包，把这个数据包称之为“桢”。每一个桢由标头(Head)和数据(Data)两部分组成。