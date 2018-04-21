# Blockchain 
### What is Blockchain ?
A blockchain is a decentralized, distributed and public digital ledger that is used to record transactions across many computers so that the record cannot be altered retroactively without the alteration of all subsequent blocks and the collusion of the network.<br />
![Blockchain Structure](https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/Bitcoin_Block_Data.svg/1200px-Bitcoin_Block_Data.svg.png) <br />

BLOCKCHAINS are built from 3 technologies (the Internet, private key cryptography, & protocol governing incentivization) <br />

| 1. Private Key Cryptography | 2. P2P Network         | 3. Program (the blockchain's protocol) |
| --------------------------- | ---------------------- | -------------------------------------- |
| Cash vs. Plastic            | Tree falls in a forest | Tragedy of the commons                 |
| Identity                    | System of Record       | Platform                               |

![Blockchain](https://blockgeeks.com/wp-content/uploads/2016/09/infographics0517-01-1.png) <br />

# Bitcoin
### New Terms in Bitcoin
Node / Full node  : A powerful computer that runs the bitcoin software and helps to keep bitcoin running by participating in the relay of information. A node spread Bitcoin around the network. <br />
Mining            : Process by which transactions are verified & added to the public ledger, known as the blockchain. <br />
> Every 10 minutes or so, mining computers can collect a few hundred pending bitcoin transactions (a “block”) and turn them into a mathematical puzzle. <br />
> If a miner mines a new block, they're given a reward in the form of the block reward (coinbase). This is the main incentive for Bitcoin miners, as the block reward is 12.5 BTC. The block reward is halved every 210,000 blocks, which is approximately every 4 years. <br />

Bitcoin Address   : A long string **of 34 letters & numbers** (also known as __public key__). It's ok to be seen by the whole world. <br />
Private key       : A long string **of 64 letters & numbers**.


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
 5. Divisibility : Smallest unit of a bitcoin is called a satoshi, one hundred millionth of a bitcoin (1 x 10^(-8)).
 > Satoshi can conceivably enavle microtransactions that traditional electronic money can't.
 
 
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
### Additional Information
Each block contains a hash of previous block (i.e. makes it a part of chain & called __BLOCKCHAIN__).
  > In other words, if you change a small part of your previous block , then you also need to change the current block's hash. <br />
  
 ```
 CHANGE IN INPUT of hash function --> CHANGE IN OUTPUT
 ```
Therefore, this is what makes Bitcoin virtually tamper-proof

### How Bitcoin Mining works
Because it's similar to gold mining in that the bitcoins exist in the protocol's design (just as the gold exists underground), but they haven't been brought out into the light yet (just as the gold hasn't yet been dug up). The bitcoin protocol stipulates that 21 million bitcoins will exist at some point. What "miners" do is bring them out into the light, a few at a time. They get to do this as a reward for creating blocks of validated transactions and including them in the blockchain. <br />

Miners group outstanding transactions into blocks and add them to the blockchain. <br />
How do they do this? <br />
  > By solving a complex mathematical puzzle(part of the bitcoin program) & including the answer in the block. The puzzle that needs solving is to find a number that, when combined with the data in the block and passed through a hash function, produces a result that is within a certain range. This is much harder than it sounds.

### How are Bitcoin Mining Pools ?
Question : Do I need to mine solo or join a pool ? <br />

Going solo means that you don't need to share your reward __(your full block reward, 25 XBTC)__. But, your odds of getting a reward are also __decreased__. <br />
Whereas a pool has __a much larger chance__ of solving a block & winning the reward (reward will be splitted between all the pool members). Therefore, joining a pool will create a steady stream of income <br />

### What is Lightning Network?
The idea of Lightning Network is based on a network that sits on top of the bitcoin blockchain and eventually setlles on it. The network is comprised of user-generated channels(send payments back and forth in a secure & trust-less fashion).

###### How it works?
> 2 Parties set up a _multisig wallet_(which requires > 1 signature to enact/menetapkan a transaction). This wallet holds some amount of bitcoin & the wallet address is saved in the bitcoin blockchain.<br />
> 2 Parties can conduct an unlimited number of transactions without ever touching the info stored on the blockchain. <br />
> When the 2 parties finish with the transaction, they close out the channel & the resulting balance is registered on the blockchain. __It is useful to note that it is not necessary to set up a direct channel to transact on lightning - you can send payments to someone via channels with people that you are connected with. The network automatically finds the shortest route.__ <br />

```
Without the security of the blockchain behind it, the lightning network will not be as secure, which implies that it will largely be used for small or even micro transactions which carry a lower risk. Larger transfers that require decentralized security are more likely to be done on the original layer.
```
