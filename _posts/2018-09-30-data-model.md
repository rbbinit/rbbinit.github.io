---
title: "Blockchain Data Model"
date: 2019-09-30 10:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

![image 188](https://user-images.githubusercontent.com/31816456/46267376-7f256900-c56f-11e8-8c7b-3e1dbbb16ac7.png)  

## Block Data model  
#### merkle root is the first hash that represents every transaction included inside the block.  
#### nonce is literally number only used once. It is used in bitcoin mining.
#### Miners are solving for the nonce what when added to a hashed block, and those 2 values are rehashed, will solve the mining puzzle  

### Nuts and bolts of transaction  
![image 190](https://user-images.githubusercontent.com/31816456/46267854-2a372200-c572-11e8-84c5-00b166b2ebc6.png)  

#### When you do transaction, there are 1 input and 2 outputs.  
#### Input is the amount in wallet, Output 1 is money I gave to another address, Output 2 is the change I will get back.  

![image 191](https://user-images.githubusercontent.com/31816456/46267855-2a372200-c572-11e8-81f9-10ec9f38dc0c.png)  

#### All inputs reference back to output. Inputs are the unspent outputs from another transaction.  
#### If someone got bitcoin, it is recorded as unspent outputs. It is called ** UTXO **  
![image 193](https://user-images.githubusercontent.com/31816456/46267857-2a372200-c572-11e8-989c-0299de904e87.png)  

#### So, if you get many bitcoins from other transactions, you get huge UTXOs.  
##### UTXO can not be divided and arbitrary value.  
#### There is no stored balance. It is just records of UTXO tied to a specific owner.  

### Jesscia send '2 bitcoins' to Brandy  
#### 1) Wallet scans blockchain  
#### 2) And see that there are two UTXO associated with 'Jessica' that can be summed up and used for this transaction.  
#### 3) UTXO(1)'s value is 1.25. UTXO(2)'s value is 1.75.  
#### 4) And wallets aggreagates these to UTXOs to total 3 that we use as input of 'Jessica' transaction with 'Brandy'  
#### 5) transaction fee = inputs - outputs  

![image 194](https://user-images.githubusercontent.com/31816456/46267858-2acfb880-c572-11e8-8ebc-1ae7f92be753.png)

