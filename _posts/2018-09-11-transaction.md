---
title: "About transaction"
date: 2019-09-11 09:59:28 -0400
layout: post
comments: true
categories: UdacityCourse
tags: UdacityCourse
---

Goal of private keys is security. So how private keys are generated?

Private keys = 256 bit random numbers (1 and 2^256)
         it's format = hex, wif, wix-compressed  (though format is different, it's all same 256bit(hexadecimal)
         32bytes using 64 characters (0~9, A~F)

![image 015](https://user-images.githubusercontent.com/31816456/45399290-6f0e1e00-b682-11e8-99c7-d9a742f38f48.png)
![image 017](https://user-images.githubusercontent.com/31816456/45399262-5aca2100-b682-11e8-830c-8f951d9473e2.png)
       
Using random number generator, private keys can be produced. (It is impossible to trace back(reverse) )

bitaddress.org  <- this site can make private keys.
or https://bitcoin.org/en/choose-your-wallet <- this site introduce many wallets.

I chose this wallet. electrum.
Why? this is piece of bitcoin software, fast and lightweight.

When you first make wallet using electrum, seed are generated. (**Very important and secret information)
Seeds should be stored physically(write down on paper) or in very secure tools.(I just use email)


<Sign a transaction>
When you use wallet, you will use and make transaction. 
So how do we know it's valid? and who owns the transaction? 
  = for these, use digital signature.

Definition of signature = establishes proof of ownership for each transaction. and it is produced by bitcoin wallet address.
Property = ensure transaction, authentication, integrity, non-repudation

wallet address is linked to private key.
transaction message is broadcasted to the chain.

You can have project about how to sign and verify a message ?
Use bitcoin javascript libraries (bitcoinjs-lib and bitcore-message) //you can find in google search.
  *bitcoinjs-message library have a function 'sign()' - takes in private key, message and returns a signature.

![image 021](https://user-images.githubusercontent.com/31816456/45399321-9107a080-b682-11e8-9704-d5cd4d1e12b0.png)

In conclusion, I want to show all steps called Lifecyicle.
 When transaction start,
 verify information and sends transaction. Start transaction signing algorithm which signs transaction using private key)
 This transaction is memory pool and it is broadcasted within network.
 Transaction is accepted by the miners. Miners group this transaction into a block, find the proof of work, assign this block a hash value.
 Finally, this block is now placed onto the blockchain. It gets confirmation.
 
