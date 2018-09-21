---
title: "Other-Commands"
date: 2019-09-21 11:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

**We overviewed commands before session, and continues other commands**  



## Signature - signrawtransaction, signmessage  
![image 172](https://user-images.githubusercontent.com/31816456/45869305-18f85380-bdc3-11e8-80aa-77f07fdf7e7d.png)  

**signature establies proof of ownership for each transaction on the blockchain**  
**Every transaction need signatrues**  


### signrawtransaction  

**It signs inputs for a raw transaction**  
**Second, third parameters are optional**  
**It need parameters which are transaction hex string and private key**  

#### To get 'hex string'  
#### 1) Type 'getblockhash 100' to get hash value.  
#### 2) 'getblock <hashvalue>' to get 'tx' value.  
#### 3) 'getrawtransaction <tx>'  
![image 173](https://user-images.githubusercontent.com/31816456/45868746-85725300-bdc1-11e8-84e1-f5294ebdb21e.png)  

#### To get 'privatekey'  
#### You use 'dumpprivkey' command  

## Network - getnetworkinfo, getpeerinfo, getconnectioncount  

**peer to peer network = network of computers that allows information to be shared across users**  
**Its' good for when you want the connection' information or want to configure backend service with multiple nodes**  


### getnetworkinfo  

**It returns information about the state of peer-to-peer network**  
![image 175](https://user-images.githubusercontent.com/31816456/45868748-85725300-bdc1-11e8-9b5d-4e74b0d330a4.png)  

![image 176](https://user-images.githubusercontent.com/31816456/45868749-860ae980-bdc1-11e8-9a81-ebeaf6cb5d22.png)  
#### You can see ipV4, ipv6, reachable and etc  

### getpeerinfo  

**It returns data about each connected network node**  
**You can add or remove peers**  

![image 178](https://user-images.githubusercontent.com/31816456/45868751-860ae980-bdc1-11e8-8512-aa7020904b7b.png)  
![image 179](https://user-images.githubusercontent.com/31816456/45869177-c323ab80-bdc2-11e8-9cac-138f360c6dd4.png)  

### getconnectioncount  
**It returns the number of connections to otheer nodes**  


## Mining - getmininginfo, prioritisetransaction  

![image 182](https://user-images.githubusercontent.com/31816456/45869181-c3bc4200-bdc2-11e8-9d8d-925393ff5500.png)  

**proof of work = consensus algorithm that requires manual processing from the user**  
**bitcoin blockchain currently uses miners and proof of work to achieve consensus**  

### getmininginfo  

![image 184](https://user-images.githubusercontent.com/31816456/45869183-c3bc4200-bdc2-11e8-9508-92cb15b0a0f7.png)  

**getmininginfo returns an object that contains mining-related information**  

### prioritisetransaction  

![image 185](https://user-images.githubusercontent.com/31816456/45869185-c454d880-bdc2-11e8-9b1b-92e4faf908c1.png)  

**prioritisetransaction accepts the transaction into mined blocks at higher or lower priority**  


## In conclusion of commands session, Please always remember, use 'help' commands like a best frined  



