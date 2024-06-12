# MassToWeightBySatiksha Solidity Contract

## Overview

MassToWeightBySatiksha is a Solidity contract for calculating weight based on mass and gravity. It includes functions for custom gravity values and a default Earth gravity, with robust error handling and owner-only access control.

## Features

- Compute Weight: Calculates weight given mass and gravity.
- Calculate Earth Weight: Calculates weight using Earth gravity.
- Access Control: Owner-restricted functions.

## Prerequisites

- Solidity ^0.8.0
- Ethereum development environment (Remix, Truffle, Hardhat)
- Ethereum wallet (MetaMask)

## Contract Details

### State Variables

- EARTH_GRAVITY (constant): Earth's gravity (10).
- owner (immutable): Contract owner.

### Constructor

Sets the contract deployer as the owner.

### Functions

#### computeWeight

- Purpose: Calculate weight using custom gravity.
- Visibility: Public, pure
- Parameters: mass (uint), gravity (uint)
- Returns: Calculated weight (uint)
- Errors: Checks for positive mass and gravity, prevents overflow.

#### calculateEarthWeight

- Purpose: Calculate weight using Earth gravity.
- Visibility: Public, view
- Parameters: mass (uint)
- Returns: Calculated weight (uint)
- Errors: Owner-only, checks positive mass, prevents zero weight and overflow.



## Usage

1. Deploy: Compile and deploy using an Ethereum development environment.
2. Compute Weight: computeWeight(mass, gravity) for custom calculations.
3. Earth Weight: calculateEarthWeight(mass) for Earth gravity (owner-only).

## Error Handling

- require(): Validates input conditions.
- assert(): Ensures no overflows.
- revert(): Reverts on invalid weight.

## License

Licensed under the MIT License.
