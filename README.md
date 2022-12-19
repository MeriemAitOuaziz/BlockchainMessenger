# Blockchain Messenger Decentralized App

A chat DApp built on the Avalanche Blockchain Network

## Preview

## Writing the smart contract

The smart contract is written in Solidity. We recommend using the [Remix](https://remix.ethereum.org/) IDE to Deploy it.

The contract defines 5 Data Structures :


| NAME | TYPE | DESCRIPTION |
| ------------- | ------------- | ------------- |
| user  | Structure  | user , has a name and a friend list |
| friend  | Structure  | friend, has a unique identifier(address) , and name |
| message  | Structure  | has address of sender, timestamp of sending time, and content in the form of a String message  |
| userList  | HashTable  | key : address of user, value : user Structure  |
| allMessages  | HashTable  | key : hash of sender's address and receiver's address , value : array of message structure  |

The contract defines  Functions :


## Steps To Run Project

###### Requirements
1. Node.js
2. [Metamask extension](https://metamask.io/download/) on your browser

###### Clone Project

### `git clone `

###### Deploy Contract

Deploy the contract in Database.sol file and retrive the Contract Code

Replace the line 14 of App.jsx with your Contract Code

###### Install dependancies

Go to the "Frontend" folder ...

### `cd Frontend`

And run ...

### `npm install`

###### Run Project

### `npm start`



