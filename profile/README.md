# SolarFund

make fundraising more fun and efficient thanks to decentralized incetives

Repos:
- solar-dapp: Dapp hosted at, [app.solarfund.wtf](https://app.solarfund.wtf])
- contracts: deployed on:
  - goerli testnet:
       - CHARITY_CONTRACT=0xe2884f42eE507c52aBFaDe5302b4152dd1794b7a
       - TREASURE_CONTRACT=0x45388922BaeCD944F2F1300fF20Bbb6eB1A85174 
  -  mantle testnet:
       - CHARITY_CONTRACT=0x7EbE2404A940e52e5E02fAB17C78583FfA3D1f04
       - TREASURE_CONTRACT=0xefe86329296Bf2f2fB3C4fF5545Dca8736fB2e71  
  -  mumbai testnet:
       - CHARITY_CONTRACT=0xcdb55249320aAC9600AFCca9706f61EF52115164
       - TREASURE_CONTRACT=0x9bd688AE2491C44C10C97efCB4dF15DC66FEfa01 
  -  sepolia testnet:
      -  CHARITY_CONTRACT=0x2cA10927e79Bf9c0a2566E6ccC6e8cEebFE66167
      -  TREASURE_CONTRACT=0x6B7a85AaeF8D09813890c1F4c58f2973c22eB142
  -  ZKSync testnet:
      -  CHARITY_CONTRACT=0x2cA10927e79Bf9c0a2566E6ccC6e8cEebFE66167
      -  TREASURE_CONTRACT=0x6B7a85AaeF8D09813890c1F4c58f2973c22eB142
      -  PAYMASTER_ADDRESS=0xd33D38c6580C3Fcd29023fb96A722852100C4a47
      -  TOKEN_ADDRESS=0xE10EFd0e5dD3b83E160D5F4AeA1e7953EB5B73EC
  -  
- homepage: The hompage: solarfund.wtf

SolarFund is a platform developed for the EthPrague hackathon. It aims to facilitate crowdfunding for charity projects using Ethereum smart contracts and Graph subgraphs. The project consists of three main components: the frontend dApp, the smart contracts, and the Graph subgraphs.

Table of Contents
Overview
Features
Installation
Usage
Smart Contracts
Graph Subgraphs
Contributing
License
Overview

SolarFund enables users to create and contribute to crowdfunding campaigns for charities using incentives with Treasure Hunt games. The dApp provides a user-friendly interface for project creation, browsing active campaigns, and making contributions. The smart contracts handle the logic and storage of campaign data, while the Graph subgraphs index and expose relevant data for querying.

# Features
- Create crowdfunding campaigns for charities.
- Browse and search active campaigns.
- Contribute to campaigns using native cryptocurrencies e.g. ether or matic.
- Track the progress and status of campaigns.
- Access detailed information about each campaign, including the funding goal, current balance, and contributors.
- Efficient indexing and querying of campaign data using Graph subgraphs.
- Creation of Treasure Hunt Clues and Verification of Secret submitted by the user.

# Installation
To set up the SolarFund dApp locally, follow these steps:

- Clone the repository:

`
bash
Copy code
git clone https://github.com/your-username/solarfund.git
cd solarfund
`

- Install the dependencies:

`
npm install
`

- Build the dApp:

`
npm run build
`

- Start the dApp:

`
npm start
`

The dApp will be accessible at http://localhost:3000.

# Usage

Once the dApp is running, you can access it through your browser at http://localhost:3000. From there, you can create new campaigns, browse existing campaigns, and make contributions to different project. Once your contribution was deposited you'll join the newly creted Treasure Hunt.

# Smart Contracts

The smart contracts for SolarFund are written in Solidity. They handle the core functionality of the crowdfunding campaigns, including campaign creation, contributions, and tracking campaign details, issuing chairty IDs.

To compile and deploy the smart contracts, follow the instructions below:

Compile the contracts:

`
truffle compile
`

Deploy the contracts:

`
npm hardhat compile
`

The smart contracts will be compiled and deployed to the specified Ethereum network.

# Graph Subgraphs
The Graph subgraphs for SolarFund can be found in the subgraphs/ directory. They define the data schema and indexing rules for efficiently querying and retrieving campaign data.

To deploy and index the subgraphs, follow these steps:

Install the Graph CLI:

`
npm install -g @graphprotocol/graph-cli
`

Deploy the subgraphs:

`
graph auth https://api.thegraph.com/deploy/ <access-token>
graph deploy --node https://api.thegraph.com/deploy/ --ipfs https://api.thegraph.com/ipfs/ <subgraph-name>
`

The subgraphs will be deployed and accessible for querying using the specified <subgraph-name>.
