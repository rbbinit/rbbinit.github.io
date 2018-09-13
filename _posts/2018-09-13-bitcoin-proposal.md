---
title: "Bitcoin-proposal"
date: 2019-09-13 10:26:28 -0400
layout: post
categories: Development of blockchain
---

•	Who is working on building this?  
•	How are decisions made about any changes in the software?  
•	Is there anyway for me to get involved in the project?  

Bitcoin, open source software, everyone including you, can contribute this project.  
![image 084](https://user-images.githubusercontent.com/31816456/45477772-3ef77580-b77d-11e8-84dc-cb8148916863.png)

Bitcoin improvement proposal = technical documents used to issue changes to the bitcoin core client.  
github.com/bitcoin/bips  
![image 085](https://user-images.githubusercontent.com/31816456/45477831-723a0480-b77d-11e8-830b-46aa91bed8c3.png)  

When someone propose something, it is voted to miners. And if it got majority, it can be implemented  
**What if miners only interested in their gains?**  
![image 087](https://user-images.githubusercontent.com/31816456/45477835-736b3180-b77d-11e8-8f43-127d4a003ba3.png)  
So there is a solution! It's impossible to satisfy ALL members in groups. They are seperated by groups.  
It's called **Forks**  

Types of forks are 'hardforks', 'softforks', 'source code forks'  
**Bitcoin improvement proposal**  

![image 090](https://user-images.githubusercontent.com/31816456/45478302-8df1da80-b77e-11e8-97b3-df79fd445ae6.png)
Hardforks changes bitcoin protocol a lot! It creates entirely seperate network. So users need to decide which protocol is fitted to them.  
When hardforks are implemented, developers copy original version and make alternative version. When changes occured, both are changed.  
I mean, when transaction occurs, both chains are affected. There is interesting pictures.  
![image 091](https://user-images.githubusercontent.com/31816456/45478308-921df800-b77e-11e8-9512-20329374b3d4.png)  
**Bitcoin cash** is a famous example of Hardfork. And as you can see in the picture, quantity of coin is doubled.  

Softforks differs from hardfork. What **diffrence**? Changes are not compatible.  
![image 093](https://user-images.githubusercontent.com/31816456/45478735-8f6fd280-b77f-11e8-9acd-f6810876c309.png)  
When you do softfork, you copy the original version. And then original version is temporarily maintained to only propagate throught the network.  
![image 094](https://user-images.githubusercontent.com/31816456/45478736-8f6fd280-b77f-11e8-8522-37f6d8fa728c.png)  

**Segwit** is good for upgrade block chain. It get rid of some informations from the block and expand the space for transactions.  
![image 096](https://user-images.githubusercontent.com/31816456/45479648-08702980-b782-11e8-9a8f-89b4818fc132.png)  
But **problem** it can open the door for possible way to **attack** the network.  

Finally, I want to introduce **Source code fork**.  
It is copy of blockchain code base with no resulting connection to the original blockchain.  
Famous example is **Litecoin**  
It is similar to Hardfork and Softfork. It copies original blockchain, but there is no connection between new version and original's.  
![image 097](https://user-images.githubusercontent.com/31816456/45479649-08702980-b782-11e8-9c93-f62a270bb127.png)  
Make new version by original's and cut the link between them.  
![image 099](https://user-images.githubusercontent.com/31816456/45479650-0908c000-b782-11e8-8dca-d8e8cd7c9e60.png)  

Here is the **scenarios** for better understanding  
Q1) Blocks Violating the New Rule are made stale by the upgraded mining majority  
= Hardfork  
Q2) Non-upgraded Node Rejects the new Rule resulting in a Diverging Chain  
= Softfork  
*Q3) Which type of forking doesn’t require any nodes to upgrade to maintain consensus since all blocks with the new forked in rules also follow the old rules, therefore old clients accept them. Also, this type of forking cannot be reversed.  
= Softfork  
Q4) Litecoin is considered to be which type of forking?  
= Source code fork  

