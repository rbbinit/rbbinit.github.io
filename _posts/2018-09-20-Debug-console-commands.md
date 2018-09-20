---
title: "Debug-console-commands-with Bitcoin-core"
date: 2019-09-20 11:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

## Debug console  

#### 'help' - 'debug console' - 'console'  
You can see Welcome message.  
Write down 'help' in commands line.  

![image 127](https://user-images.githubusercontent.com/31816456/45797433-68198800-bce0-11e8-9e47-6863154382fd.png)  
### You can always use 'help' commands whenever you need help! It's very important commands.  
https://en.bitcoin.it/wiki/Original_Bitcoin_client/API_calls_list  <- You also see commands in websites.  



### Debug console commands  

There are lots of commands, so before see them in details, I want to introduce a few important commands.  
Also use 'help' in each commands. For example, 'help getblockchaininfo'.  
You can find what you need, for example, parameters, return value, and etc.  


### Blockchain  
#### Commands list = getblockchaininfo, getblockcount, verifychain  

#### Type 'help getblockchaininfo'  

![image 129](https://user-images.githubusercontent.com/31816456/45797644-892ea880-bce1-11e8-9384-ad74c3131be7.png)  

And just type 'getblockchaininfo'  

![image 131](https://user-images.githubusercontent.com/31816456/45797735-0823e100-bce2-11e8-9df6-84b5de4b6758.png)  
It returns various state information about blockchain processing.  

"softforks": [ { "id": "bip34"  
-> We can see version and whether or not it was accepted to the network.  

"reject" : { "status": true"  
-> It means it is never implemented into the protocol. (So, 'false' is correct)  

In "bip9_softforks"  
-> you can find "csv" and "segwit"  
https://github.com/bitcoin/bips <- see more in details  
![image 133](https://user-images.githubusercontent.com/31816456/45797910-c7789780-bce2-11e8-9ef4-198b250ea2d0.png)  



#### Type 'help getblockcount' and 'getblockcount'  

![image 135](https://user-images.githubusercontent.com/31816456/45797970-f2fb8200-bce2-11e8-9f6d-30d1907cbcb8.png)  

As you can see, it returns the number of blocks in the longest blockchain.  
![image 134](https://user-images.githubusercontent.com/31816456/45797969-f262eb80-bce2-11e8-97a1-14c7dc5fc652.png)  


#### Type 'help verifychain' and 'verifychain'  

![image 136](https://user-images.githubusercontent.com/31816456/45798082-70bf8d80-bce3-11e8-8281-ba2a0f9bddd2.png)  

'True' means entire chain is accurate.  


#### Next session, we see other commands 


