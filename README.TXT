# 💰 ISRCOIN — A Simple Cryptocurrency Project

Build, test, and deploy your own ERC-style token using Solidity and Remix IDE.

---

## 📘 Table of Contents

1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Repository Structure](#repository-structure)  
4. [Getting Started](#getting-started)  
   - [Requirements](#requirements)  
   - [Running in Remix](#running-in-remix)  
   - [Deploying via Scripts](#deploying-via-scripts)  
5. [Testing](#testing)  
6. [Usage](#usage)  
7. [Token Details & Tokenomics](#token-details--tokenomics)  
8. [Supported Modules & Notes for Remix](#supported-modules--notes-for-remix)  
9. [Contributing](#contributing)  
10. [License](#license)  

---

## 🏁 Introduction

**ISRCOIN** is a simple cryptocurrency (token) implementation built in Solidity, intended for demonstration, learning, or baseline use on EVM-compatible blockchains.  
It allows standard token operations (transfer, approval, minting, balances) and is designed to be deployed and interacted with via **Remix IDE**, as well as via deployment scripts using **ethers.js** or **web3.js**.

The goal is to provide a clear, extendable foundation for developers looking to understand or build upon the basics of cryptocurrency smart contracts.

---

## ✅ Features

- 🪙 ERC-20 compliant token interface  
- 🔒 Ownership and minting control  
- 🔁 Standard transfers, approvals, and allowances  
- 🧩 Modular contract structure for easy upgrades  
- 🧮 Safe arithmetic (Solidity ^0.8.x overflow checks)  
- ⚡ Ready for deployment via Remix, Ethers, or Web3 scripts  

---

## 📂 Repository Structure
isrcoin-cryptocurrency/
├── contracts/ # Solidity smart contracts
│ ├── ISRCOIN.sol # Main token contract
│ ├── Migrations.sol # (optional) for deployment tracking
│ └── ... # Other helper or example contracts
├── scripts/ # TypeScript deployment & interaction scripts
│ ├── deploy_with_ethers.ts
│ ├── deploy_with_web3.ts
│ ├── deploy_with_remix.ts
│ └── ...
├── tests/ # Automated Solidity / JS tests
│ ├── contract_tests.sol
│ └── js_tests.js
└── README.md # Project documentation

---

## 🛠 Getting Started

### Requirements

- **Solidity** `^0.8.x`  
- **Node.js** `>=16.x` (for scripts and tests)  
- **MetaMask** (optional, for blockchain interaction)  
- **Remix IDE** (recommended for compiling and deploying)

---

### Running in Remix

1. Open **[Remix IDE](https://remix.ethereum.org/)**.  
2. Import this repository (via GitHub URL or ZIP upload).  
3. Navigate to `contracts/ISRCOIN.sol` and compile it.  
4. Go to the **Deploy & Run Transactions** tab.  
5. Select an environment (e.g. `Injected Provider - MetaMask` or `Remix VM`).  
6. Deploy and interact with your token directly from the Remix interface.

---

### Deploying via Scripts

Deployment scripts can be found in the `scripts/` folder.

- `deploy_with_ethers.ts` — uses **ethers.js**  
- `deploy_with_web3.ts` — uses **web3.js**  
- `deploy_with_remix.ts` — compatible with Remix runtime  

To deploy another contract, modify the contract name and constructor arguments in the script, then execute it through Remix or Node.js.

---

## 🧪 Testing

Automated tests are included in both Solidity and JavaScript formats.

- Solidity tests use **Remix Testing** tools.  
- JavaScript tests use **Mocha** and **Chai** assertions.  

To run a test script in Remix:  
Right-click the test file → **Run**.  
Ensure your contracts are compiled before testing.

---

## 📦 Usage

Once deployed, the `ISRCOIN` contract supports the following functions:

| Function | Description |
|-----------|--------------|
| `balanceOf(address)` | Returns the token balance of an address |
| `transfer(to, amount)` | Transfers tokens to another address |
| `approve(spender, amount)` | Allows another address to spend tokens |
| `transferFrom(from, to, amount)` | Moves tokens using allowance |
| `mint(to, amount)` | Creates new tokens (owner only) |
| `burn(amount)` | Destroys tokens |

These can be executed directly from the **Remix UI** or via scripts that interact with the deployed contract ABI.

---

## 📊 Token Details & Tokenomics

| Field | Value / Description |
|--------|----------------------|
| **Token Name** | ISRCOIN |
| **Symbol** | ISR |
| **Decimals** | 18 |
| **Total Supply** | *(define your initial or capped supply)* |
| **Mintable** | Yes *(Owner only)* |
| **Burnable** | Yes |

> Update these values in `ISRCOIN.sol` if you customize the tokenomics.

---

## 🔧 Supported Modules & Notes for Remix

Remix supports a limited number of modules for `require` / `import`.  
The following are currently supported:

- `ethers`  
- `web3`  
- `swarmgw`  
- `chai`  
- `multihashes`  
- `remix`  
- `hardhat.ethers` *(if Hardhat plugin enabled)*  

If you import unsupported modules, Remix will display:  

