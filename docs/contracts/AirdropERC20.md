---
slug: /AirdropERC20
title: AirdropERC20
hide_title: true
displayed_sidebar: contracts
---

# AirdropERC20

## Methods

### airdrop

```solidity
function airdrop(address _tokenAddress, address _tokenOwner, address[] _recipients, uint256[] _amounts) external payable
```

Lets contract-owner send ERC20 tokens to a list of addresses.

_The token-owner should approve target tokens to Airdrop contract, which acts as operator for the tokens._

#### Parameters

| Name           | Type      | Description                                    |
| -------------- | --------- | ---------------------------------------------- |
| \_tokenAddress | address   | Contract address of ERC20 tokens to air-drop.  |
| \_tokenOwner   | address   | Address from which to transfer tokens.         |
| \_recipients   | address[] | List of recipient addresses for the air-drop.  |
| \_amounts      | uint256[] | Quantity of tokens to air-drop, per recipient. |

### contractType

```solidity
function contractType() external pure returns (bytes32)
```

_Returns the type of the contract._

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | bytes32 | undefined   |

### contractVersion

```solidity
function contractVersion() external pure returns (uint8)
```

_Returns the version of the contract._

#### Returns

| Name | Type  | Description |
| ---- | ----- | ----------- |
| \_0  | uint8 | undefined   |

### initialize

```solidity
function initialize(address _defaultAdmin) external nonpayable
```

_Initiliazes the contract, like a constructor._

#### Parameters

| Name           | Type    | Description |
| -------------- | ------- | ----------- |
| \_defaultAdmin | address | undefined   |

### multicall

```solidity
function multicall(bytes[] data) external nonpayable returns (bytes[] results)
```

_Receives and executes a batch of function calls on this contract._

#### Parameters

| Name | Type    | Description |
| ---- | ------- | ----------- |
| data | bytes[] | undefined   |

#### Returns

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| results | bytes[] | undefined   |

### owner

```solidity
function owner() external view returns (address)
```

Returns the owner of the contract.

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### setOwner

```solidity
function setOwner(address _newOwner) external nonpayable
```

Lets an authorized wallet set a new owner for the contract.

#### Parameters

| Name       | Type    | Description                                          |
| ---------- | ------- | ---------------------------------------------------- |
| \_newOwner | address | The address to set as the new owner of the contract. |

## Events

### OwnerUpdated

```solidity
event OwnerUpdated(address indexed prevOwner, address indexed newOwner)
```

#### Parameters

| Name                | Type    | Description |
| ------------------- | ------- | ----------- |
| prevOwner `indexed` | address | undefined   |
| newOwner `indexed`  | address | undefined   |