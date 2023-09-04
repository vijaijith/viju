# MyToken Contract README

Welcome to the README for the MyToken contract, a straightforward Solidity smart contract designed for creating a custom ERC-20 token named "META" (MTA).

## Contract Overview

- **Token Name**: META
- **Token Abbreviation**: MTA
- **Total Supply**: 0 (initially)

## Public Variables

Within this contract, we have the following public variables:

- `tokenName`: A publicly accessible string variable representing the name of the token.
- `tokenAbbrv`: A publicly accessible string variable representing the abbreviation of the token (symbol).
- `totalSupply`: A publicly accessible unsigned integer variable representing the total supply of the token.

## Mapping Variable

This contract utilizes a mapping variable:

- `balances`: This mapping associates addresses with their respective token balances, effectively tracking the quantity of tokens held by each address.

## Functions

### `mint`

```solidity
function mint(address _address, uint _value) public
```

The `mint` function empowers the contract owner (or individuals with appropriate permissions) to mint new tokens and allocate them to a specific address.

- Parameters:
  - `_address`: The destination address where the newly minted tokens will be assigned.
  - `_value`: The quantity of tokens to mint and allocate.

### `burn`

```solidity
function burn(address _address, uint _value) public
```

The `burn` function grants the contract owner (or individuals with appropriate permissions) the ability to burn a specified number of tokens held by a given address.

- Parameters:
  - `_address`: The source address from which tokens will be burned.
  - `_value`: The quantity of tokens to burn.

Please be aware that burning tokens reduces the overall supply of the token, and it can only be executed if the target address's balance is equal to or greater than the number of tokens to be burned.

## License

This smart contract is provided under the MIT License:

```plaintext
SPDX-License-Identifier: MIT
```

## Disclaimer

This smart contract is offered as-is and without any warranties. It should be used at your own discretion and risk.

**Note**: When including this contract in your project, remember to specify the Solidity version used for compilation in your actual README file. Since Solidity continually evolves, specifying the version is crucial to ensure that future developers can compile and comprehend the code accurately.
