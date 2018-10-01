---
title: "Inside of transactions"
date: 2019-09-30 11:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

## Raw transcation  
#### On a blockchain, transactions are stored in a double hashed form.( through SHA-256 twice)  
#### Raw data is hexadecimal format and it's not JSON object format.  
#### It is organized well. You can see how protocol layer stores our transaction information.  

![image 198](https://user-images.githubusercontent.com/31816456/46268636-8439e680-c576-11e8-91a4-e681c0783d25.png)  

#### Version = which rules this transaction follows  
#### Input count = how many inputs are used.  
#### Input info = Where are inputs coming from?  
#### Output count = How many count was produced  
#### Output info = How much BTC outputted? Conditions for future spending.  
#### Locktime = earliest time or block a Tx can be added to the blockchain.  
##### It has two options.  
##### locktime  < 500 million -> block height.  
##### > 500 million -> unix timestamp  

## Locking script, Unlocking script  
![image 199](https://user-images.githubusercontent.com/31816456/46268637-84d27d00-c576-11e8-8381-47ab8575ec12.png)  

##### Unloking script, literally, unlock the conditions of locking script  
##### Through scripts, you can see how transactions are executed onto the blockchain  

![image 203](https://user-images.githubusercontent.com/31816456/46268641-856b1380-c576-11e8-9f88-7cbbe60506ea.png)  


## Script  
### A list of instructions recorded in each transacction that when executed determines if transaction is valid and bitcoinds can be spent.  
#### Simple, lightweight language  

![image 204](https://user-images.githubusercontent.com/31816456/46268642-856b1380-c576-11e8-99e2-3b6902373b30.png)  

![image 206](https://user-images.githubusercontent.com/31816456/46270234-8d7c8080-c581-11e8-9636-df31ecbec730.png)  
#### It's like puzzle. Puzzle should be matched before bitcoin is spent.  

![image 207](https://user-images.githubusercontent.com/31816456/46270235-8e151700-c581-11e8-8431-98807896b630.png)  
![image 208](https://user-images.githubusercontent.com/31816456/46270236-8e151700-c581-11e8-9a8f-9c9da4aefe1d.png)  

#### Unlocking script of input solve puzzle, that is UTXO's locking script in previous transaction.  

![image 210](https://user-images.githubusercontent.com/31816456/46270238-8e151700-c581-11e8-952d-4e6b493ed549.png)
![image 211](https://user-images.githubusercontent.com/31816456/46270239-8eadad80-c581-11e8-9d58-a7416c2aa994.png)  


### Details  
![image 213](https://user-images.githubusercontent.com/31816456/46270469-a5a0cf80-c582-11e8-8c67-965ce0b9c3f3.png)  

