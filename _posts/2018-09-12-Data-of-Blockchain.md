---
title: "Data of blockchain"
date: 2019-09-11 12:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

Blocks contain two main sections that each hold important data  
 = block header, block transactions  
![image 068](https://user-images.githubusercontent.com/31816456/45429689-c17d2800-b6de-11e8-81ad-578d973844b9.png)

**Block header** contains metadata about block including things like hash(which is connected to the chain)

![image 069](https://user-images.githubusercontent.com/31816456/45474554-09e72500-b775-11e8-8442-6c1dd4c2e131.png)   
You can see 'Number of transactions', 'Height', 'Block reward', 'Timestamp', 'Difficulty', 'Bits' and so on.

![image 072](https://user-images.githubusercontent.com/31816456/45474727-719d7000-b775-11e8-8d41-c69215ed65f8.png)  
**coinbase** means first transaction.  
Also, you can explore through blockchain JSON data.
![image 074](https://user-images.githubusercontent.com/31816456/45474790-998cd380-b775-11e8-95a2-fdf9f7d17525.png)  
You can found 'hash', 'height', 'time', 'previoiusblockhash' and so on.  

In block header, there is txid, hash, vin, vout  
**vin = transaction input **  
**vout = transaction output ** //change = full input - value(sent) - miners reward    
vin = When bitcoin is sent, inputs are collected from the network and combined together to send to the address specified by the sender  

non-human readable is in raw transaction. Data is formatted to heximal system.  
![image 075](https://user-images.githubusercontent.com/31816456/45475100-55e69980-b776-11e8-9518-f9db6ba46d20.png)

Q1) When reviewing Blockchain data, what does the block height mean within the header of a block?  
= block number in the chain (an identifier for reference to the block)  
Q2) When reviewing Blockchain header data, which of the following fields contribute to block immutability?  
= Previous hash, nonce, bits and time stamp (These help assist in block immutability in the chain. If one is modified  
after inclusion into the chain, the block hash would be invalid which would break the chain)  

Explore the bitcoin codebase  
![image 076](https://user-images.githubusercontent.com/31816456/45476535-191ca180-b77a-11e8-9315-5b64baf3d1c7.png)  
https://github.com/bitcoin/bitcoin  
There are lots of things in github. Folder **src** is one of the important things. And closer look to chainparams.cpp  
It sets up the consensus rules for all the blocks  
![image 077](https://user-images.githubusercontent.com/31816456/45476664-7a447500-b77a-11e8-8264-24d45add3aff.png)    

![image 077](https://user-images.githubusercontent.com/31816456/45477198-fbe8d280-b77b-11e8-8842-9f57e5acc4cb.png)
![image 078](https://user-images.githubusercontent.com/31816456/45477200-fd19ff80-b77b-11e8-91ce-f588a26952a4.png)
![image 079](https://user-images.githubusercontent.com/31816456/45477205-fe4b2c80-b77b-11e8-9e70-8c8f30b8a265.png)  

When you see **HalvingInterval**, you can know how miners get rewards. After a certain mount of blocks are mined, reward of  
for all miners is cut is half. Why? for example, halving interval =210,000 means block is halved after every 210,000 blocks  
![image 081](https://user-images.githubusercontent.com/31816456/45477314-48341280-b77c-11e8-9897-a42d0fdb99ee.png)  

nPowTargetTimespan sets how often the proof of work puzzle adjusts its difficulty level. //two weeks
nPowTargetSpacing = determines when the network should expect a new block //10 * 60 = 10 minutes.  
