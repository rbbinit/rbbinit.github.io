---
title: "Inside scripts"
date: 2019-09-30 12:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

## Opcode  

![image 218](https://user-images.githubusercontent.com/31816456/46270472-a5a0cf80-c582-11e8-930b-99538e9e1536.png)  

### Opcodes show how datas in stack interact each other  

### OP_ADD  
#### For example, 3 5 OP_ADD means pop 5, pop 3, sum (5,3) and push 8  

### OP_EQUAL  
#### It checks top two stack items where equal or not. And returns boolean result.  

#### 2 6 OP_ADD 8 OP_EQUAL  
#### Pop 2, pop 6 and sum (2, 6) and push 8  
#### 'OP_EQUAL' compare '8' and result of 'OP_ADD'  
#### If result is true, transaction is valid.  
#### '2' is unlocking script and the others are locking script.  

#### 2 3 OP_ADD 2 OP_MUL 1 OP_ADD 11 OP_EQUAL  
#### true  

## Standard script  

### <sig><pubKey> OP_CHECKMULTISIG  
#### Bracketed values are data to be pushed to the **stack** for example, <sig>  
#### Non-bracked words are **opcodes** for example, OP_CHECKMULTISIG  
#### OP prefic can be omitted  

## Using online block explorer  

### www.blockchain.com  
![image 220](https://user-images.githubusercontent.com/31816456/46271268-c4a16080-c586-11e8-86ca-60fbec18beab.png)  
### You can see input and outputs  
### Checkout this TXID: 56beef8afe5a4b5b41225211e62c3e7bce5747c4c8dcdd982173e8496687794b  

![image 219](https://user-images.githubusercontent.com/31816456/46271267-c4a16080-c586-11e8-9552-4b3791a730ac.png)  

### Input  
#### It is <sig><pubKey>  

### Output  
#### DUP HASH160 PUSHDATA(20)[07628bb59790a53711f3e9caddaa7eed89663935] EQUALVERIFY CHECKSIG  
#### -> OP_DUP OP_HASH160 <pubKeyHASH> OP_EQUALVERIFY OP_CHECKSIG  

## Attributes of Script  

### Not turing completeness  
![image 224](https://user-images.githubusercontent.com/31816456/46271269-c4a16080-c586-11e8-8702-94eff038aec0.png)  

#### No loops or complex flow control  
#### Completely deterministic ->so that we know when and how program will end  
#### Provides simplicity and security  
#### It removes fear of being stuck in an infinite loop  
#### Limited language prevents transaction validation mechanism from being targeted and attacked as a vulnerability  

### Stateless verfication  
![image 225](https://user-images.githubusercontent.com/31816456/46271270-c539f700-c586-11e8-81ae-ba2bd6247145.png)  

#### benefit = same script run anywhere in the system will execute the same way  
