# Token 

## Overview

This repository contains a Solidity smart contract for an ERC-20 token with additional functionality. The token is implemented using the OpenZeppelin library, providing standard ERC-20 features, burnable capabilities, and ownership management. The contract allows for the initial minting of tokens, subsequent minting by the owner, burning of tokens, and setting a maximum supply.

## Contract Features

### ERC-20 Standard Compliance

The `Token` contract inherits from OpenZeppelin's `ERC20` base contract, ensuring compliance with the ERC-20 standard. This means that the token supports standard functions such as `transfer`, `approve`, `transferFrom`, and provides events like `Transfer` and `Approval`.

### Burnable Functionality

The token includes burnable functionality through the use of OpenZeppelin's `ERC20Burnable` extension. Token holders can burn their own tokens, reducing the total supply.

### Ownership Management

The contract is also an `Ownable` contract, which means that it includes functionality to manage ownership. The initial owner is set during contract deployment, and only the owner has the authority to mint additional tokens and set the maximum supply.

### Minting and Burning

The owner can mint additional tokens using the `mintTokens` function, providing flexibility for token issuance. Additionally, any token holder can burn their own tokens using the `burnTokens` function, reducing the total supply.

### Maximum Supply

The contract allows the owner to set a maximum supply for the token. The `_setMaxSupply` function ensures that the new maximum supply is greater than or equal to the current total supply. The owner can adjust the maximum supply, and the contract will mint additional tokens to meet the new maximum supply if needed.

## Deployment

To deploy the contract, the following parameters must be provided:

- `_name`: The name of the token.
- `_symbol`: The symbol or ticker of the token.
- `initialSupply`: The initial supply of tokens minted during contract deployment.
- `maxSupply`: The maximum supply of tokens that can ever exist.
- `initialOwner`: The address that will initially own the contract.

## Usage

1. Deploy the contract by providing the required parameters.
2. The owner can mint additional tokens using the `mintTokens` function.
3. Token holders can burn their own tokens using the `burnTokens` function.
4. The owner can adjust the maximum supply using the `_setMaxSupply` function.

## Author

Prathap singh

p19982102@gmail.com
