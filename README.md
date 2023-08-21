# EscrowFrontend
# ethavaxmod2
#  create a Auction app frontend and deploy it on the Localhost network
This repository is made for my ethereum intermediate avax mod 2 project which is used to create a Frontend app for Auction and run it on localhost network.

## Problem Statement

create a simple contract frontend  with 2-3 function.
## Description

This program  written in Solidity by using a simple contract, solidity is  a programming language used for developing smart contracts on the Ethereum blockchain. 
This Solidity smart contract is called `EscrowContract` and is designed to facilitate an escrow-like arrangement between a buyer, a seller, and an arbiter in the context of a financial transaction. Here's a breakdown of the key components and functions in the contract:

1. **Contract Variables:**
   - `buyer`, `seller`, and `arbiter`: These variables store the Ethereum addresses of the buyer, seller, and arbiter involved in the transaction.
   - `amount`: This variable stores the amount of Ether that the buyer has deposited into the escrow contract.
   - `releaseApproved` and `refundApproved`: These boolean variables track whether the release of funds to the seller or the refund to the buyer has been approved by the necessary parties.

2. **Events:**
   - `FundsDeposited`: This event is emitted when the buyer deposits funds into the escrow contract.
   - `FundsReleased`: This event is emitted when funds are released to the seller.
   - `FundsRefunded`: This event is emitted when funds are refunded to the buyer.

3. **Constructor:**
   - The constructor takes two parameters: `_seller` and `_arbiter`, representing the addresses of the seller and arbiter. The `msg.sender` at the time of contract deployment is assumed to be the buyer. This information is stored in the respective contract variables.

4. **Function `depositFunds`:**
   - This function allows the buyer to deposit funds into the escrow contract by sending Ether along with the function call.

5. **Function `releaseFunds`:**
   - This function can be called by the seller or the arbiter to release the funds to the seller.
     
6. **Function `refundBuyer`:**
   - This function can be called by the arbiter to refund the funds to the buyer.
   - Similar to `releaseFunds`, it requires certain conditions to be met.

7. **Function `getContractBalance`:**
   - This function allows anyone to query the current balance (amount of Ether) held by the escrow contract.


## Getting Started

### Executing Program
To run this CONTRACT we use VS CODE IDE. 
Install project dependencies by running: npm install
Start the local Ethereum network (Hardhat's built-in node) by running: npx hardhat node
In a new terminal, deploy the contract to the local network by running: npx hardhat run deploy.js --network localhost
Note down the deployed contract address as it will be required in the frontend.
Start the React frontend by running: npm start.It will redirect to our localhost frontend page and then put the auction value and then it will ask confirmation of transaction from metamask wallet.

## Author

SHRESHTHA PAL

## License

This project is licensed under the MIT License - see the LICENSE file for details
