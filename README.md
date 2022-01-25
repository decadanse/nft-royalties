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
Ganache CLI v6.12.2 (ganache-core: 2.13.2)

#### Available Accounts
==================
(0) 0x3A0E53F18d134bA6106094b24D38224C022a2bE4 (100 ETH)
(1) 0x055FA23A64af9C62b6525A568bed377137e67c73 (100 ETH)
(2) 0x878C480A2B9c30815bCe0aa8d984f3F84a092afe (100 ETH)
(3) 0xD50beD6E47A06A39B634E4634565346B1DF82Ac5 (100 ETH)
(4) 0x93e40F831C84009908570337760A3718FEb9Bf88 (100 ETH)
(5) 0xcE26e5977339596a1547178aFf42afb575A1452A (100 ETH)
(6) 0x89c4b4360c1D78964F9050b69A58022DD3994a8E (100 ETH)
(7) 0x15b506203707d8f6AddfcB66E7B0573aD9187B65 (100 ETH)
(8) 0x5E66c4B0837f3712f4e16d748B628D2E455AAdE6 (100 ETH)
(9) 0xFF1EC69A918fDcEdA554350FBf8CD9671d965c2a (100 ETH)

## In the second terminal

decadanse@decadanse:~/smart-contracts/nft_royalties$ truffle migrate --reset

#### Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



#### Starting migrations...
======================
> Network name:    'development'
> Network id:      1643110148528
> Block gas limit: 6721975 (0x6691b7)


#### 1_initial_migration.js
======================

   #### Deploying 'Migrations'
   ----------------------
   > transaction hash:    0x518af7c4b53ab05d450ca8006126bdc7ae4183032aeb9c3fa16a4d7d2c5585b1
   > Blocks: 0            Seconds: 0
   > contract address:    0xd16EE11bF8A819e3fa43916a2b41d83715853836
   > block number:        1
   > block timestamp:     1643110173
   > account:             0x93F2c03442718A17824E1D3c774a87e1A556Ce24
   > balance:             99.99502292
   > gas used:            248854 (0x3cc16)
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00497708 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00497708 ETH


#### 2_deploy_contracts.js
=====================

   #### Deploying 'NFT'
   ---------------
   > transaction hash:    0x5b1652715f0eddb35acdb204c5f352ae34300ade4b243c3bed5aaee77dba2cea
   > Blocks: 0            Seconds: 0
   > contract address:    0xC79Ff4e5Ff985dFA8f070b786A3c74798FB730C7
   > block number:        3
   > block timestamp:     1643110174
   > account:             0x93F2c03442718A17824E1D3c774a87e1A556Ce24
   > balance:             99.91855012
   > gas used:            3781127 (0x39b207)
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.07562254 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.07562254 ETH


#### Summary
=======
> Total deployments:   2
> Final cost:          0.08059962 ETH


decadanse@decadanse:~/smart-contracts/nft_royalties$ truffle test
Using network 'development'.


#### Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



  Contract: NFT
    deployment
      ✓ returns the deployer (38ms)
      ✓ returns the artist (41ms)
      ✓ returns the royality fee
      ✓ sets the royality fee (148ms)
    royalities
      ✓ initially belongs to owner1 (41ms)
      ✓ successfully transfers to owner2 (494ms)
      ✓ updates ether balances (388ms)


  7 passing (5s)


decadanse@decadanse:~/smart-contracts/nft-royalties$ truffle exec scripts/perform_sale.js 
Using network 'development'.

NFT Collection Fetched

Initial balance of deployer | 99.91799986
Initial balance of artist   | 100
Initial balance of owner1   | 100
Initial balance of owner2   | 100

Minting NFT for owner1...

NFT has been minted!

Balance of deployer | 100.66799986
Balance of artist   | 100.25
Balance of owner1   | 98.9969116
Balance of owner2   | 100

Performing transfer sale to owner2...

Transfer complete!

Balance of deployer | 100.66799986
Balance of artist   | 102.75
Balance of owner1   | 106.4959647
Balance of owner2   | 89.99845402
