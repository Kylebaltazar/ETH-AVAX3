# myToken Smart Contract

**Version: 0.1.0**

This Solidity smart contract, `myToken`, is an ERC-20-compatible token with additional features inherited from OpenZeppelin contracts. It supports standard token functionalities such as transfers, as well as additional features like token minting, burning, and ownership control.

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Contract Details](#contract-details)
  - [Token Features](#token-features)
  - [Inheritance](#inheritance)
  - [Constructor](#constructor)
- [Usage](#usage)
  - [Minting Tokens](#minting-tokens)
  - [Burning Tokens](#burning-tokens)
  - [Transfer Function Override](#transfer-function-override)
- [License](#license)

## Overview

The `myToken` contract is written in Solidity and adheres to version `^0.8.0`. It is designed to provide a versatile ERC-20 token with additional functionalities for minting, burning, and ownership control.

## Getting Started

### Prerequisites

Ensure you have a development environment with Solidity compiler support.

### Installation

Clone the repository and deploy the `myToken` contract using your preferred development environment.

## Contract Details

### Token Features

- Implements ERC-20 standard functions for transferring tokens.
- Extends functionality with token minting, burning, and ownership control.

### Inheritance

- Inherits from `ERC20` for standard ERC-20 functionality.
- Inherits from `ERC20Burnable` to enable token burning.
- Inherits from `Ownable` to restrict certain functions to the contract owner.

### Constructor

- Initializes the token's name, symbol, and initial supply during deployment.
- Mints the initial supply to the contract deployer.

## Usage

### Minting Tokens

To mint additional tokens, execute the `mint` function, which is accessible only to the contract owner.

```solidity
function mint(uint256 amount) public onlyOwner {
    _mint(_msgSender(), amount);
}
```
## License
This code is licensed under the MIT License. See the LICENSE file for details.
