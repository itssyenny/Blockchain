# Blockchain 
### What is Blockchain ?
A blockchain is a decentralized, distributed and public digital ledger that is used to record transactions across many computers so that the record cannot be altered retroactively without the alteration of all subsequent blocks and the collusion of the network, by using cryptography and a computer network to : <br />
 * track assets;
 * secure the ledger from tampering (4D). <br />
 > 4D : **D**uplication, **D**ouble Spending, **D**ilution, **D**ata Lost. <br />
![Blockchain Structure](https://blockgeeks.com/wp-content/uploads/2017/08/image4.png)

BLOCKCHAINS are built from 3 technologies (the Internet, private key cryptography, & protocol governing incentivization) <br />

| 1. Private Key Cryptography | 2. P2P Network         | 3. Program (the blockchain's protocol) |
| --------------------------- | ---------------------- | -------------------------------------- |
| Cash vs. Plastic            | Tree falls in a forest | Tragedy of the commons                 |
| Identity                    | System of Record       | Platform                               |

![Blockchain](https://blockgeeks.com/wp-content/uploads/2016/09/infographics0517-01-1.png) <br />
<br />

### Blockchain Ecosystem : Virtuous Cycle !
![Blockchain Ecosystem](https://github.com/itssyenny/Blockchain/blob/master/blockchain_ecosystem.png)
<br />
# Bitcoin
### New Terms in Bitcoin
Node / Full node  : A powerful computer that runs the bitcoin software and helps to keep bitcoin running by participating in the relay of information. A node spread Bitcoin around the network. <br />
Mining            : Process by which transactions are verified & added to the public ledger, known as the blockchain. <br />
> Every 10 minutes or so, mining computers can collect a few hundred pending bitcoin transactions (a “block”) and turn them into a mathematical puzzle. Unspent transaction outputs (**UTXO**) are important because fully validating **nodes use them to figure out whether or not transactions are valid**– all inputs to a transaction must be in the UTXO database for it to be valid.<br />
![utxo image](https://github.com/itssyenny/Blockchain/blob/master/utxo.png)<br />
![satoshis & utxo image](https://github.com/itssyenny/Blockchain/blob/master/satoshis%2Butxo.png) <br />

```
If a miner mines a new block, they're given a reward in the form of the block reward (coinbase). This is the main incentive for Bitcoin miners, as the block reward is 12.5 BTC. The block reward is halved every 210,000 blocks, which is approximately every 4 years. <br />
```

Bitcoin Address     : A long string **of 34 letters & numbers** (also known as __public key__). It's ok to be seen by the whole world. <br />
Private key         : A long string **of 64 letters & numbers**. <br />
Nonce               : In cryptography, a nonce is an **arbitrary number that can only be used once**. <br />
                    The _nonce_ in a **bitcoin block** is a 32-bit (4-byte) field whose value is set so that the hash of the block will contain a run of leading zeros  <br />
Proof-of-Work (PoW) system : The most popular algorithm being used by currencies such as Bitcoin and Ethereum, each one with its own differences.

```
Example:
keccak256("hello") = 1c8aff950685c2ed4bc3174f3472287b56d9517b9c948127319a09a7a36deac8
keccak256("hello1") = 57c65f1718e8297f4048beff2419e134656b7a856872b27ad77846e395f13ffe
```
In Proof of Work, in order for an actor to be elected as a leader and choose the next block to be added to the blockchain they have to find a solution to a particular mathematical problem. <br />
Whenever a new block is mined, that miner gets rewarded with some currency (block reward, transaction fees) and thus are incentivized to keep mining. In Proof of Work, other nodes verify the validity of the block by checking that the hash of the data of the block is less than a preset number. <br />

<br/>

### What is Bitcoin?
 In what ways is it different from traditional currencies ? <br />
 Bitcoin can be used electronically and traded digitally. <br />
 The difference between Bitcoin and fiat digital currencies : <br />
 1. Decentralization : No single institution controls the bitcoin network,but maintained by a group of volunteer coders and run by an open network of dedicated computers spread around the world.
 > Solve the __"double spending problem"__ (i.e. digital assets can easily be copied & re-used) through an ingenious/talented combination of cryptography and economic incentives.
 2. Limited supply : In Bitcoin, the supply is tightly controlled by the underlying algorithm. A small number of new bitcoin trickle out every hour until __maximum of 21 million has been reached__.
 > In theory, if the demand grows and the supply remains the same, the value will increase
 3. Pseudonymity : users in Bitcoin operate in semi-anonymity (no need to identify themselves when sending bitcoin to another user/the system doesn't need to know identity of the sender).
 > In practice, each user is identified by the address of one's wallet.
 > The network is transparant, so the progress of a particular transaction is visible to all.
 4. Immutability : Bitcoin transactions can't be reversed(return money)
 > If a transaction is recoreded on the network & if more than an hour has passed, it is impossible to modify.
 5. Divisibility : **Smallest unit of a bitcoin is called a Satoshi, one hundred millionth of a bitcoin (1 x 10^(-8)).
 > Satoshi can conceivably enavle microtransactions that traditional electronic money can't**.
 
 <br />
 
 
 ### How do Bitcoin transactions work?
 ###### Simple Version 
 1. I want to send some of my Bitcoin to you. <br />
 2. I publish my intention & the nodes scan the entire bitcoin network to validate : <br />
    * I have the amount of Bitcoin I want to send
    * I haven't sent it to someone else
 3. Once the info has been confirmed, my transaction will get included in a "block" which gets attached to the previous block.
  > The term called __BLOCKCHAIN__
 4. Transactions can't be undone because it would mean re-doing all the blocks that came after.
 
 ###### Complicated Version
Bitcoin wallet doesn't actually hold bitcoin, but it holds the __BITCOIN ADDRESS__ (in which keeps a record of all of my transactions & my balance) 
 ```
  Any transaction I issue from my bitcoin address needs to be "signed" with my private key. To do that, I put both my private   key and the transaction details (how many bitcoins I want to send, and to whom) into the bitcoin software on my computer or smartphone. < br />
  The network then confirms that I haven't previously spent the bitcoin __by running through my address history__, which it can do because it knows my bitcoin address (= my public key), & because all transactions are public on the bitcoin ledger (blockchain). <br />
 ```
 
 <br />
 
### Additional Information
Each block contains a hash of previous block (i.e. makes it a part of chain & called __BLOCKCHAIN__).
  > In other words, if you change a small part of your previous block , then you also need to change the current block's hash. <br />
  
 ```
 CHANGE IN INPUT of hash function --> CHANGE IN OUTPUT
 ```
Therefore, this is what makes Bitcoin virtually tamper-proof

<br />


### How Bitcoin Mining works
Because it's similar to gold mining in that the bitcoins exist in the protocol's design (just as the gold exists underground), but they haven't been brought out into the light yet (just as the gold hasn't yet been dug up). The bitcoin protocol stipulates that 21 million bitcoins will exist at some point. What "miners" do is bring them out into the light, a few at a time. They get to do this as a reward for creating blocks of validated transactions and including them in the blockchain. <br />

Miners group outstanding transactions into blocks and add them to the blockchain. <br />
How do they do this? <br />
  > By solving a complex mathematical puzzle(part of the bitcoin program) & including the answer in the block. The puzzle that needs solving is to find a number that, when combined with the data in the block and passed through a hash function, produces a result that is within a certain range. This is much harder than it sounds.

<br />


### How are Bitcoin Mining Pools ?
Question : Do I need to mine solo or join a pool ? <br />

Going solo means that you don't need to share your reward __(your full block reward, 25 XBTC)__. But, your odds of getting a reward are also __decreased__. <br />
Whereas a pool has __a much larger chance__ of solving a block & winning the reward (reward will be splitted between all the pool members). Therefore, joining a pool will create a steady stream of income <br />


<br />

### What is Lightning Network?
The idea of Lightning Network is based on a network that sits on top of the bitcoin blockchain and eventually setlles on it. The network is comprised of user-generated channels(send payments back and forth in a secure & trust-less fashion).

###### How it works?
> 2 Parties set up a _multisig wallet_(which requires > 1 signature to enact/menetapkan a transaction). This wallet holds some amount of bitcoin & the wallet address is saved in the bitcoin blockchain.<br />
> 2 Parties can conduct an unlimited number of transactions without ever touching the info stored on the blockchain. <br />
> When the 2 parties finish with the transaction, they close out the channel & the resulting balance is registered on the blockchain. __It is useful to note that it is not necessary to set up a direct channel to transact on lightning - you can send payments to someone via channels with people that you are connected with. The network automatically finds the shortest route.__ <br />

```
Without the security of the blockchain behind it, the lightning network will not be as secure, which implies that it will largely be used for small or even micro transactions which carry a lower risk. Larger transfers that require decentralized security are more likely to be done on the original layer.
```

<br />

### What is Ethereum ?
### A blockchain application platform & 'world computer'
Our personal data, passwords, & financial info are all stored on other people's computers(such as in clouds & servers owned by companies like Amazon, Facebook, or Google). This setup has a number of conveniences, as these companies deploy teams of specialists to help store & secure this data, and remove the costs that come with hosting and uptime. <br />

However,there is also a __VULNERABILITY__. A hacker/ a government can gain unwelcome access to your files without your knowledge, by influencing/ attacking a third-party service - meaning they can steal, leak, or change important info. <br />

While Bitcoin aims to disrupt Paypal & online banking , __Ethereum__ has the goal of using a blockchain to replace internet third parties -- those that store datas, transfer mortgages, & keep track of complex financial instruments. <br />

In short, ethereum wants to be a 'World Computer' that would decentralize. With Ethereum, servers and clouds are replaced by thousands of so-called "nodes" run by volunteers from across the globe (thus forming a "world computer"). <br />
The idea is that one entity will no longer have control over your notes and that no one could suddenly ban the app itself, temporarily taking all of your notebooks offline. Only the user can make changes, not any other entity. <br />

In theory, it combines the control that people had over their information in the past with the easy-to-access information that we're used to in the digital age. Each time you save edits, or add or delete notes, every node on the network makes the change. <br />

So, in conclusion, Ethereum app is like if you have debt with your mom & due on April 25. Unfortunately, today is already April 25 and you forget to pay your mom. Then, your mom remembers & she request $100 on Ethereum app which on the agreement before, your mom can access your __Ethereum Virtual Machine (EVM, which can execute scripts using an international network of public nodes)__ to pay her $100.
![Ethereum App](https://media.coindesk.com/uploads/2017/03/Screen-Shot-2017-03-28-at-4.56.00-PM.png)

<br />

### The DAO
The best-known attempt at creating such an organization was called _The DAO_.<br />
The plan was for participants to receive DAO tokens, then vote for which projects to fund. For selecting projects to invest in, it relied on the "wisdom of crowds."

There are a few ways that The DAO intended to improve on the governance of today's organizations:
 * Anyone with internet access could hold DAO tokens or buy them
 * DAO creators could set whatever rules they voted on. <br />
In abstract, DAOs function similarly. They rely on smart contracts, or pre-programmed rules that describe what can happen in the system. <br />
Essentially, they see it as a way to cryptographically guarantee democracy, where stakeholders can vote on adding new rules, changing the rules, or ousting a member, to name a few examples. <br />

<br />

### What is ICO ?
### Refers to distribution of digital tokens
ICO stands for _Initial Coin Offering_ & refers to the creation and sale of digital tokens. In an ICO, a project creates a certain amount of a digital token and sells it to the public, usually in exchange for other cryptocurrencies such as bitcoin or ether.

###### Additional info
Cryptocurrency token offerings is a new fundraising method that allows companies to raise millions of dollars in mere minutes. <br />


### The difference between Blockchain and Cryptocurrency
| Blockchain | Cryptocurrency |
| ---------- | -------------- |
|signed,P2P,distributed ledger databases | digital asset that can be an exchange medium (these days, ~ tends to be implemented using a blockchain | 

Most of crytocurrency systems use a proof-of-work scheme to create a new block or Bitcoin. Bitcoin uses a proof-of-work schemes that are based on SHA-256. <br />


