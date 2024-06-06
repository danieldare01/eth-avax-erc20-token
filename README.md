# Dan Token (DTK) ERC20 Smart Contract

This repository contains the smart contract code for Dan Token (DTK), an ERC20 token implemented in Solidity. This contract includes standard ERC20 functionalities such as transferring tokens, approving allowances, minting new tokens, and burning tokens.

## Table of Contents

- [Overview](#overview)
- [Contract Details](#contract-details)
- [Getting Started](#getting-started)
- [Functions](#functions)
- [Events](#events)
- [License](#license)

## Overview

Dan Token (DTK) is an ERC20-compliant token with the following attributes:
- **Name**: Dan Token
- **Symbol**: DTK
- **Decimals**: 18

The contract allows for the basic operations of an ERC20 token including transfers, approvals, and allowances, as well as minting and burning of tokens.

## Contract Details

### Token Information

- **Name**: Dan Token
- **Symbol**: DTK
- **Decimals**: 18

### State Variables

- `totalSupply`: The total supply of the token.
- `balanceOf`: Mapping of addresses to their respective balances.
- `allowance`: Mapping of addresses to their approved allowances for other addresses.

## Getting Started

### Prerequisites

To work with this smart contract, you need the following installed on your system:

- Node.js (v14 or later)
- npm (v6 or later)
- Remix https://remix.ethereum.org/

### Installation

1. Clone the repository to Remix.

### Compilation and Deployment

1. Compile the smart contract

2. Deploy the smart contract to a local blockchain V

## Functions

### `transfer`

Transfers `amount` tokens from the caller's account to `recipient`.

```solidity
function transfer(address recipient, uint amount) external returns (bool)
```

### `approve`

Approves `spender` to transfer up to `amount` tokens from the caller's account.

```solidity
function approve(address spender, uint amount) external returns (bool)
```

### `transferFrom`

Transfers `amount` tokens from `sender` to `recipient` using the allowance mechanism. `amount` is deducted from the caller's allowance.

```solidity
function transferFrom(address sender, address recipient, uint amount) external returns (bool)
```

### `mint`

Mints `amount` new tokens to the caller's account, increasing the total supply.

```solidity
function mint(uint amount) external
```

### `burn`

Burns `amount` tokens from the caller's account, decreasing the total supply.

```solidity
function burn(uint amount) external
```

## Events

### `Transfer`

Emitted when `value` tokens are moved from one account (`from`) to another (`to`).

```solidity
event Transfer(address indexed from, address indexed to, uint value)
```

### `Approval`

Emitted when the allowance of a `spender` for an `owner` is set by a call to `approve`. `value` is the new allowance.

```solidity
event Approval(address indexed owner, address indexed spender, uint value)
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
