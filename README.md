# MyToken – ERC‑20 Token (GPP Week 2)

This repository contains a simple ERC‑20 compatible token implemented in Solidity for GPP Week 2.

## Contract details

- Name: MyToken
- Symbol: MTK
- Decimals: 18
- Standard: ERC‑20‑like

## Features

- `totalSupply` assigned to deployer in the constructor
- `transfer` to send tokens between addresses
- `approve` and `transferFrom` for delegated transfers
- `balanceOf` and `allowance` view functions

## How to deploy in Remix

1. Open [Remix](https://remix.ethereum.org/).
2. Create a new file `MyToken.sol` and paste the contract code from this repo.
3. Select a Solidity compiler version `0.8.x` and compile.
4. Open **Deploy & Run Transactions**, choose JavaScript VM.
5. Deploy with `_totalSupply`:
   - `1000000000000000000000000` for 1,000,000 tokens (18 decimals).
6. Use the generated UI to call:
   - `name`, `symbol`, `decimals`, `totalSupply`
   - `balanceOf`, `transfer`, `approve`, `transferFrom`.

## Author

- Your Name (GPP Week 2)
