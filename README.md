# New Terms in Bitcoin
Node / Full node  : A powerful computer that runs the bitcoin software and helps to keep bitcoin running by participating in the relay of information. A node spread Bitcoin around the network. <br />
Mining            : Process by which transactions are verified and added to the public ledger, known as the blockchain. <br />
> Every 10 minutes or so, mining computers can collect a few hundred pending bitcoin transactions (a “block”) and turn them into a mathematical puzzle. <br />
> The miner who find the solution will get 25 bitcoins as a reward, but only after another 99 blocks have been added to the ledger. <br />
Bitcoin Address   : A long string **of 34 letters & numbers** (also known as __public key__). It's ok to be seen by the whole world. <br />
Private key       : A long string **of 64 letters & numbers**.


# Bitcoin
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
 
 
 ## How do Bitcoin transactions work?
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
###### Additional Information
Each block contains a hash of previous block (i.e. makes it a part of chain & called __BLOCKCHAIN__).
  > In other words, if you change a small part of your previous block , then you also need to change the current block's hash. <br />
  
 ```
 CHANGE IN INPUT of hash function --> CHANGE IN OUTPUT
 ```
Therefore, this is what makes Bitcoin virtually tamper-proof

###### How Bitcoin Mining works
Because it's similar to gold mining in that the bitcoins exist in the protocol's design (just as the gold exists underground), but they haven't been brought out into the light yet (just as the gold hasn't yet been dug up). The bitcoin protocol stipulates that 21 million bitcoins will exist at some point. What "miners" do is bring them out into the light, a few at a time. They get to do this as a reward for creating blocks of validated transactions and including them in the blockchain. <br />

Miners group outstanding transactions into blocks and add them to the blockchain. <br />
How do they do this? <br />
  > By solving a complex mathematical puzzle(part of the bitcoin program) & including the answer in the block. The puzzle that needs solving is to find a number that, when combined with the data in the block and passed through a hash function, produces a result that is within a certain range. This is much harder than it sounds.

 
