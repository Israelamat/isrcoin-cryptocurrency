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

```bash
isrcoin-cryptocurrency/
├── contracts/               # Solidity smart contracts
│   ├── ISRCOIN.sol          # Main token contract
│   ├── Migrations.sol       # (optional) for deployment tracking
│   └── ...                  # Other helper or example contracts
├── scripts/                 # TypeScript deployment & interaction scripts
│   ├── deploy_with_ethers.ts
│   ├── deploy_with_web3.ts
│   ├── deploy_with_remix.ts
│   └── ...
├── tests/                   # Automated Solidity / JS tests
│   ├── contract_tests.sol
│   └── js_tests.js
└── README.md                # Project documentation
