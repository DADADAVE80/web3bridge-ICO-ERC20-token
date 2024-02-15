# TSTToken

## Overview
This is a simple ERC20 token designed with simplicity and flexibility in mind.
TSTToken provides essential features for managing token balances, allowances, and
ownership. This README provides an overview of TSTToken's key functionalities and
how to interact with it.

## Contract Details
- **Name**: TSTToken
- **Symbol**: TST
- **Decimals**: 18
- **Total Supply**: Adjustable through minting and burning

## Key Functions
### Token Supply
- Total Supply: Get the current total supply using the `totalSupply()` function.

### Balance and Transfer
- Balance: Check the balance of an account with the `balanceOf(address account)` function. 
- Transfer: Transfer TST tokens to another address with the `transfer(address recipient, uint256 amount)` function. A 10% transfer fee is applied.

### Allowance and Approval
- Allowance: Check the allowance granted from one address to another using the `allowance(address owner, address spender)` function. 
- Approve: Grant an allowance from your address to another using the `approve(address owner, address spender, uint256 amount)` function.

### TransferFrom
- TransferFrom: Transfer tokens from one address to another on behalf of the owner, utilizing an approved allowance. Use the `transferFrom(address sender, address recipient, uint256 amount)` function.

### Mint and Burn
- Mint: Create new TST tokens and assign them to an account using the `mint(address account, uint256 amount)` function.
- Burn: Destroy TST tokens from an account using the `burn(address account, uint256 amount)` function.

## Getting Started
To deploy and interact with TSTToken, follow these steps:


```shell
npm install
npx hardhat run scripts/deploy.ts
npx hardhat node
npx hardhat run test/TSTToken.ts
```

## Important Notes
- Ensure proper ownership control as the contract creator is initially set as the owner. 
- The transfer function incurs a 10% transfer fee, adjusted automatically. 
- Mint and burn functions allow for dynamic adjustments to the total supply.