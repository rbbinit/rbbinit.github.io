---
title: "Variety of Commands"
date: 2019-09-21 10:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

## Hash commands - getblockhash, getnetworkhashups, getbestblockhash  
![image 137](https://user-images.githubusercontent.com/31816456/45864646-9d43da00-bdb5-11e8-802f-93e9e286b93a.png)  

### getblockhash  
It returns hash of a block at the block number provided.  
For example, getblockhash 9  

![image 138](https://user-images.githubusercontent.com/31816456/45864679-bf3d5c80-bdb5-11e8-87e2-346ac592dff5.png)  

![image 139](https://user-images.githubusercontent.com/31816456/45864680-bfd5f300-bdb5-11e8-8e4a-fb4ae9ba3be1.png)  

### getnetworkhashups  

![image 140](https://user-images.githubusercontent.com/31816456/45864681-bfd5f300-bdb5-11e8-8993-2b041864e274.png)  

#### It returns estimated network hashes per second based on specified number of recent blocks.  
#### Network is creating hash values as quickly as possible and this is broken down into hashes per second using this command.  
#### Each hash is happening at a different rate.  
![image 142](https://user-images.githubusercontent.com/31816456/45864685-c06e8980-bdb5-11e8-8fb5-e399436522a0.png)  

### getbestblockhash  

![image 143](https://user-images.githubusercontent.com/31816456/45864686-c06e8980-bdb5-11e8-96d3-104da76e9d14.png)  

#### It returns the hash of the best block.
 ***best block is most recent block that you've synced to with your local copy of the blockchain***  
 ***hash value means digital fingerprint for information.***  
 
![image 144](https://user-images.githubusercontent.com/31816456/45864687-c06e8980-bdb5-11e8-8421-e7f4d2a71098.png)  

## Blocks commands - getblock, getblockheader, generate  
![image 145](https://user-images.githubusercontent.com/31816456/45864950-db8dc900-bdb6-11e8-9abc-933dcdf02205.png)  

### getblock  
*** It returns details of block information.***  
#### It can use like this. 'getblock <hashvalue>'  
#### So we need to type 'getblockhash 100', which returns hash value. And then use it and get detail information.  

![image 147](https://user-images.githubusercontent.com/31816456/45864945-da5c9c00-bdb6-11e8-9ad8-b87a95ba6dab.png)  

### getblockheader  
*** It returns information about the block header ***  
#### It also need 'hash value' parameters. So again, use 'getblockhash 100' (Number '100' is just for example.)  

![image 149](https://user-images.githubusercontent.com/31816456/45864948-daf53280-bdb6-11e8-8525-20ab38794bd8.png)  

### generate  
*** It is for regent environment***  
*** It immediately mines the specified number of blocks to an address in the wallet***.  
*** This is good when you want to test applications with having more powerful controls over your environment***.  

## Wallet - getwalletinfo, listwallets, walletpassphrasechange  
*** wallet = software that stores private keys that give access to a bitcoin balance ***  

### getwalletinfo  
*** It returns an object containing various info about a wallet’s state ***  
![image 154](https://user-images.githubusercontent.com/31816456/45865727-640d6900-bdb9-11e8-8053-d5c522a07f17.png)  

### listwallets  
*** It returns a list of currently loaded wallets ***  
*** There is 'wallet.data' file in the folder. And debug console read it. ***  
![image 155](https://user-images.githubusercontent.com/31816456/45865728-640d6900-bdb9-11e8-803b-b4cc735d568f.png)  

![image 157](https://user-images.githubusercontent.com/31816456/45865731-64a5ff80-bdb9-11e8-804e-0c7efe4bf688.png)  

### walletpassphrasechange  
*** It changes the wallet passphrase from an old passphrase to a new passphrase ***  
*** When you make wallet first, 12 word phrases are maded ***  
![image 158](https://user-images.githubusercontent.com/31816456/45865732-64a5ff80-bdb9-11e8-8f8f-a3f618d18c25.png)  

## Mempool - getmempoolinfo, getrawmempool, getmempoolentry  

*** mempool = waiting place for all unconfirmed transactions before they are added to the blockchain ***  
*** So you can explore the current state of transactions within mempool ***  

![image 159](https://user-images.githubusercontent.com/31816456/45865733-64a5ff80-bdb9-11e8-8ae9-2fc6d808d31d.png)  

### getmempoolinfo  
*** It returns details of the active state of the transaction memory pool***  

![image 161](https://user-images.githubusercontent.com/31816456/45866225-0da12a00-bdbb-11e8-9d66-1d106ce04776.png)  

### getrawmempool  
*** It returns all transaction ids in memory pool ***  

![image 162](https://user-images.githubusercontent.com/31816456/45866226-0e39c080-bdbb-11e8-998e-7c9a9985415a.png)  

## Transaction - getchaintxstats, getrawtransaction, listtransactions  
*** It is very important commands of that I am writing down.  ***  
*** Because transaction is core of everything that happens on the blockchain. ***  

### getchaintxstats  

*** It computes statistics about the total number and rate of transactions in the chain timestamp of final block ***  
*** txrate = many transactoins made per second ***  

![image 168](https://user-images.githubusercontent.com/31816456/45866936-24e11700-bdbd-11e8-8645-e2db93509e4c.png)  

### getrawtransaction  

*** It returns new transaction data ***  
#### To use it, you need to get hash value.  
#### 'getrawtransaction <hashvalue> true'  

![image 170](https://user-images.githubusercontent.com/31816456/45866938-24e11700-bdbd-11e8-9f5e-669685d43e60.png)  

### listtransactions  

*** It returns list of transaction for a given account ***  

### Next session, get more other commands  
