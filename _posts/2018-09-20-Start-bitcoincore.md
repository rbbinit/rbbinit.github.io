---
title: "Getting start with Bitcoin-core"
date: 2019-09-20 10:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

### Before I use testnet in bitcoin-core, I want to compare testnet and regnet.  

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
![image 118](https://user-images.githubusercontent.com/31816456/45796541-0c4d0000-bcdc-11e8-9dd6-04a31fef5572.png)  

## Switch to Testnet  
For run the client with a testnet flaog, you need to change a bitcoin configuration file.  
### First, make a file which named 'bitcoin.conf'  
![image 197](https://user-images.githubusercontent.com/31816456/45796726-f55add80-bcdc-11e8-9cff-5b88358349db.png)  
#### If you want to use regnet, just modify textfile's contents to 'regnet = 1'  
And reboot bitcoin-core program. Icon's color has been changed to green.  (Name also contain test-net)  

## Let's start  
You need to make new wallets. 
#### File- receving message - New - Write down in label(anything you want) - Ok  
![image 124](https://user-images.githubusercontent.com/31816456/45796955-12dc7700-bcde-11e8-9bb2-ac5dfc007a94.png)  
Now you get a new address. Copy it  

## Details of your wallets.   
https://live.blockcypher.com/btc-testnet/  
Using the site, choose 'BTC Testnet'(blue icon) and paste your wallet adderss  
You can see ***Recent blocks, Current Fee estimates, latest transactions***  

## Next section, we will use Debug console commands

