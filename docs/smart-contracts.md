# Smart Contracts

This document outlines the intended purpose and structure of Orikal’s smart contract layer. While the contracts are not finalized, the platform will leverage on-chain logic to enable decentralized treasury interactions.

## 🎯 Objectives
- Enable decentralized registration of staking pools.
- Map and track wallets associated with organizations.
- Provide transparency and auditability for key actions.
- Ensure organizations maintain full custody over their assets.

## ⚙️ Target Tech Stack
- **Solidity** for smart contract logic
- **Hardhat** for development and deployment
- **Ethers.js** or **Viem** for client-side interaction
- **OpenZeppelin** libraries for secure contract foundations

## 🔐 Core Design Principles
- Contracts must be publicly auditable.
- No central custody of user funds.
- On-chain data must be verifiable and minimal.

## 🚀 Deployment Strategy
Smart contracts will first be deployed on testnets (e.g., Goerli or Sepolia). Once validated and audited, they will be deployed on mainnet-compatible chains (Ethereum, Polygon, etc.).

## 🧪 Testing
Smart contracts will include comprehensive test coverage using Hardhat and TypeScript.

## 📅 Audit Plans
We plan to conduct a full third-party audit before any mainnet deployment.

## 🛠 Current Status
Contracts are currently in the planning and design phase. Implementation will begin once the initial infrastructure and product specs are finalized.

---
For future updates, contract addresses and deployment info will be shared in this file and in [`orikal-smartcontracts`](https://github.com/NXT-Block/orikal-smartcontracts).
