---
title: "Frame of blockchains (udacity)"
date: 2019-09-10 08:26:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

@@@  I will commit pictures in all articles for better understanding   @@@

Why is manage transaction important?
= Without transaction, blockchain technology is nothing, but just static entity.

The concept of Blockchain identity is very important. It's like bank account, drivers licenses, club membership and so on.
Also, bitcoin wallet is consisted of private key, public key and wallet address.

Wallet address = unique identifier for your wallet to identify ours and can have transaction with others.
It's address is not secret. It can be shared with others. But trace inside wallet address and try to figuer out what's inside
for example, private key, is not possible.

Public key= It's not secret. It can make private key by using Algorithms. I discuss it below.

Private key= It's secret key. Very very important key and should be hided to others. 
 It is randomly generated number. It is used when you send bitcoin and other coins. 

Hashing is also important things you should know.
It has Three things. =SHA256, ECDSA, RIPEMD 
![image 002](https://user-images.githubusercontent.com/31816456/45399055-a5976900-b681-11e8-87eb-b36d8871b7a7.png)

< Steps of how hashing is used> 
Private keys -> ECDSA (Algorithms) -> Public Keys -> SHA256 -> result of SHA256 -> RIPEMD160 -> (Base58check) -> Wallet Address
![image 010](https://user-images.githubusercontent.com/31816456/45399070-b9db6600-b681-11e8-962d-1336c85499ea.png)
 but reverse is very very very difficult. (So blockchain's security is great)

SHA256 = 256 means it consisted of 256 bits , Ripemd160 = 160 bits also.
Through base58check, wallet address is 58 bits.

All steps above automatically execute because of programming. (That's why I respect programmers)

Next time, I write down type of wallet. 
