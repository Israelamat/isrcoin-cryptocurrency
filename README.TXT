# 💰 ISRCOIN — A Simple Cryptocurrency Project

Build, test, and deploy your own ERC-style token using Solidity and Remix IDE.

---

## 🏁 Introduction

**ISRCOIN** is a custom ERC-20–inspired cryptocurrency token built in **Solidity** and designed to operate on the **Ethereum Virtual Machine (EVM)**.  
The project showcases the essential mechanics behind a blockchain token — including **token minting, transfers, balances, and ownership control** — while remaining minimal, secure, and easy to extend.

This implementation was developed and tested entirely in **[Remix IDE](https://remix.ethereum.org/)**, a browser-based environment for Solidity smart contract development.

---

## ⚙️ Technical Overview

### 1. Contract Architecture

The project follows a clean and modular design:
- **ISRCOIN.sol** defines the core ERC-20 logic and ownership pattern.
- The token inherits standard interfaces and uses **Solidity ^0.8.x**, taking advantage of its built-in overflow protection (no need for `SafeMath`).
- Ownership is managed using a simple `owner` variable and `onlyOwner` modifier pattern for privileged actions such as minting.

```solidity
modifier onlyOwner() {
    require(msg.sender == owner, "Not authorized");
    _;
}
