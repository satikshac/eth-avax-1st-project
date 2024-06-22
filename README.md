# ErrorHandling Solidity Contract

## Overview

ErrorHandling is a Solidity contract designed to demonstrate various error handling mechanisms including require(), assert(), and revert(). It manages a counter and restricts certain actions to the contract owner, ensuring robust error checking and access control.

## Features

- Owner-Restricted Actions: Only the owner can perform certain actions.
- Counter Management: Increment and reset a counter with error handling.

## Prerequisites

- Solidity >=0.7.0
- Ethereum development environment (Remix, Truffle, Hardhat)
- Ethereum wallet (MetaMask)

## Contract Details

### State Variables

- satiksha (address): The contract owner.
- count (uint): Counter variable.

### Constructor

Sets the contract deployer as the owner (satiksha).

### Functions

#### call

- *Purpose*: Increments the counter.
- *Visibility*: Public
- *Errors*: Uses require() to ensure the caller is the owner (satiksha).

#### incrementCount

- *Purpose*: Increments the counter.
- *Visibility*: Public
- *Errors*: Uses assert() to verify the counter is always positive after increment.

#### resetCount

- *Purpose*: Resets the counter to zero.
- *Visibility*: Public
- *Errors*: Uses revert() to ensure only the owner (satiksha) can reset the counter.

## Usage

1. *Deploy*: Compile and deploy using an Ethereum development environment.
2. *Call*: Use call() to increment the counter (owner-only).
3. *Increment Count*: Use incrementCount() to increment the counter.
4. *Reset Count*: Use resetCount() to reset the counter to zero (owner-only).

## Error Handling

- *require()*: Ensures the caller is the owner.
- *assert()*: Verifies the counter remains positive after increment.
- *revert()*: Reverts transaction if the caller is not the owner during reset.

## License

This project is unlicensed.

