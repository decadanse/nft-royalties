# NFT Royalties 

## Technology Stack & Tools

- Solidity (Writing Smart Contract)
- Javascript (React & Testing)
- [Web3](https://web3js.readthedocs.io/en/v1.5.2/) (Blockchain Interaction)
- [Truffle](https://www.trufflesuite.com/docs/truffle/overview) (Development Framework)
- [Ganache](https://www.trufflesuite.com/ganache) (For Local Blockchain)

## Requirements For Initial Setup
- Install [NodeJS](https://nodejs.org/en/), should work with any node version below 16.5.0
- Install [Truffle](https://www.trufflesuite.com/docs/truffle/overview), In your terminal, you can check to see if you have truffle by running `truffle version`. To install truffle run `npm i -g truffle`. Ideal to have truffle version 5.4 to avoid dependency issues.
- Install [Ganache](https://www.trufflesuite.com/ganache).

## Setting Up
### 1. Clone/Download the Repository

### 2. Install Dependencies:
```
$ cd nft_royalties
$ npm install 
```

### 3. Start Ganache

### 4. Migrate Smart Contracts
`$ truffle migrate --reset`

### 5. Run Tests
`$ truffle test`

### 6. Run Sale Script
`$ truffle exec ./scripts/perform_sale.js`




# How it works

## In the first terminal

decadanse@decadanse:~/smart-contracts/nft_royalties$ ganache-cli
![pic0](https://user-images.githubusercontent.com/87744721/150973061-cedca42f-305b-454a-8ab8-27bfa015d6c1.png)

## In the second terminal

decadanse@decadanse:~/smart-contracts/nft_royalties$ truffle migrate --reset
![pic1](https://user-images.githubusercontent.com/87744721/150973221-cfc73db7-05b0-4cee-8ed6-e02480f930b7.png)
![pic2](https://user-images.githubusercontent.com/87744721/150973229-6116701d-e59b-4921-be76-98d59d29c1bd.png)
![pic3](https://user-images.githubusercontent.com/87744721/150973278-378e92a9-1db6-4b52-ab10-218e5c5725b0.png)

decadanse@decadanse:~/smart-contracts/nft_royalties$ truffle test
![pic6](https://user-images.githubusercontent.com/87744721/150973421-256064b7-4103-4264-8b53-f79b34554f38.png)

danse@decadanse:~/smart-contracts/nft-royalties$ truffle exec scripts/perform_sale.js 
deca![pic4](https://user-images.githubusercontent.com/87744721/150973117-cf8e02da-ab01-4db8-93c4-fc2c3ba9e340.png)
