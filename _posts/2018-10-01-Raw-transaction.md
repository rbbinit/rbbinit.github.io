---
title: "Raw transaction"
date: 2019-10-01 10:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

# Raw transaction using bitcoin protocol  

### Step 1 - View all unspent confirmed UTXO in the wallet  
### Step 2 - View Details about a Specific UTXO  
### Step 3 - Create a Raw Transaction  
### Step 4 - Decode the Raw Transaction (to doublecheck it went through correctly)  
### Step 5 - Sign the Raw Transaction  
### Step 6 - Submit the Raw Transaction to the Network  
### Step 7 - Query the TxID of the Transaction we sent  


## Step 1 - listunspent  

### To show all the unspent confirmed output in our wallet.  
### These can be used as inputs in another transaction.  

![image 228](https://user-images.githubusercontent.com/31816456/46276946-a2b2d880-c59c-11e8-940e-d202db8bfc16.png)  

### txid = This shows us that there is a transaction with this id.  
### vout = (At index 0) The transaction has one output.  
### address = Transaction is assigned to this address.  
### account = User defined and made it before.  
### scriptPubkey = The hash of the locking script.  
### amount = Transaction amount in BTC.  
### confirmations = At the time of viewing this Tx, how many confirmation occured.  


## Step 2 - gettxout  

![image 230](https://user-images.githubusercontent.com/31816456/46276948-a2b2d880-c59c-11e8-942d-8ec254f9aefe.png)  

### gettxout "txid" n (include_mempool)  
### n is vout number. 'include_mempool' is boolean( optional & default : true).  


## Step 3 - createrawtransaction  

![image 235](https://user-images.githubusercontent.com/31816456/46279453-16a4af00-c5a4-11e8-9cc1-759a85169194.png)  

### If we have 0.05 and send 0.03 to another, we have to spend whole output from a transaction.  
### Suppose 0.0005 is transaction fee, change back for rest money, 0.0195.  
### Sum(inputs) - sum(outputs) = transaction fee.  
### 0.05 - (0.03+0.0195) = 0.0005.  
### Two outputs are produced = 0.03, 0.0195  
### And these are added to address parameters.  


![image 236](https://user-images.githubusercontent.com/31816456/46279455-16a4af00-c5a4-11e8-8243-c68c7e928990.png)  

### You can see '0.03' and '0.0195' in the picture above.  
### Return value is 'raw hex string'  


# Step 4 - decoderawtransaction  

![image 237](https://user-images.githubusercontent.com/31816456/46279456-16a4af00-c5a4-11e8-8e0d-7a9c62a11536.png)  

### We can confirm everything processed correctly by using this command.  

### 'scriptSig' field is empty now. Why? We have not signed transaction yet to prove that we own the address from  
### which the UTXO were sourced.  
  

# Build Out Command  

![image 238](https://user-images.githubusercontent.com/31816456/46279457-173d4580-c5a4-11e8-9145-20c96a4f49fd.png)  


## signrawtransaction  

### signrawtransaction "hexstring"  


## sendrawtransaction  

### It takes the raw hex string produced by signrawtransaction and returns a transaction hash (txid) as it submits the transaction on the network  


## gettransaction  

### Query the TxID and view details. Similar to online block explorer.  

