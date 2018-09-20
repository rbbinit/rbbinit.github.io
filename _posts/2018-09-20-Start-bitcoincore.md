---
title: "Getting start with Bitcoin-core"
date: 2019-09-20 10:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

Before I use testnet in bitcoin-core, I want to compare testnet and regnet.  

**Testnet is alternative bitcoin blockchain that provides a test environment for applications**  
**Regnet gives test environment. But there is no network which means local**  

![image 117](https://user-images.githubusercontent.com/31816456/45796116-fdfde480-bcd9-11e8-9cb4-37a1b83aeaa2.png)  

Reg has no peers for networking. It almost instantaneously generate blocks on demand for testing.  
It has no validation and just make any nuumber node.  

# Bitcoin-core software  
![image 121](https://user-images.githubusercontent.com/31816456/45796309-e1ae7780-bcda-11e8-9437-75d32a655c2c.png)  

## You need to download wallet. https://bitcoin.org  
!Warning. You need a lot of space (120 GB for sync nodes)  So I bought extra hard space.  
But don't worry. If you don't have any space for now, you can just use bitcoin core software while not using many nodes.  
(A few commands can't be used without full-downloading nodes(about 120GB) )  

## Pruning  
You can reduce the amount of space taken by bitcoin blockchain.


