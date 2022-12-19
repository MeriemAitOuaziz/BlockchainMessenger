# Blockchain Messenger Decentralized App

A chat DApp built on the Avalanche Blockchain Network as part of an academic project.

Group 6 : Meriem AIT OUAZIZ & Chaimaa NAJIM


## Preview
![Preview](/assets/preview.png)
## Writing the smart contract

The smart contract is written in Solidity. We recommend using the [Remix](https://remix.ethereum.org/) IDE to Deploy it.

The contract defines 5 Data Structures :


| NAME | TYPE | DESCRIPTION |
| ------------- | ------------- | ------------- |
| user  | Structure  | user , has a name and a friend list |
| friend  | Structure  | friend, has a unique identifier(address) , and name |
| message  | Structure  | has address of sender, timestamp of sending time, and content in the form of a String message  |
| userList  | HashTable  | key : address of user, value : user Structure  |
| allMessages  | HashTable  | key : hash of sender's address and receiver's address , value : array of message structure, Hence one entry groups all messages exchanged by 2 users  |

The contract defines  Functions :

| NAME | DESCRIPTION |
| --- | --- |
| checkUserExists | looks up user by address in the userList |
| createAccount | adds given nonempty user name to userList, key being the sender's address |
| getUsername | returns name from userList for the given address |
| addFriend | adds the user identified by the given address to sender's friendList, adds the sender to the user identified by the given address friendList |
| checkAlreadyFriends | checks if users identified by given addresses exist in eachother's frindList |
| getMyFriendList | returns frindList of sender  |
| _getChatCode | returns a hash of the 2 given addresses using Keccak-256 algorithm |
| sendMessage | calculates key for message (=hash(sender,receiver)) and adds message in correct entry of allMessages Table  |
| readMessage | Returns all the chat messages communicated in a channel |

## Steps To Run Project

###### Requirements
1. Node.js
2. [Metamask extension](https://metamask.io/download/) on your browser

###### Clone Project

### `git clone `

## Set Up Metamask

Add Custom Network with following settings :

**Network Name**: Avalanche FUJI C-Chain

**New RPC URL**: https://api.avax-test.network/ext/bc/C/rpc

**ChainID**: use the recommended ChainID

**Symbol**: C-AVAX

**Explorer**: https://cchain.explorer.avax-test.network

Fund your address from the given [faucet](https://faucet.avax.network/).

## Deploy the smart contract with [Remix](https://remix.ethereum.org/)

Compile and run the smart contract in Database.sol and retrieve the ABI and Contract Code.

Place your Contract Code in line 14 of App.jsx.

###### Install dependancies

Go to the "Frontend" folder ...

### `cd Frontend`

And run ...

### `npm install`

###### Run Project

### `npm start`






