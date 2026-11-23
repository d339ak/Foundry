# Foundry Commands

## Project setup

- `forge init --no-git` — new Foundry project (inside ~/Foundry, always use --no-git)
- `forge install <repo> --no-git` — add a library (e.g. Chainlink, OpenZeppelin)
- - `forge install smartcontractkit/chainlink-brownie-contracts --no-git` Example (Chainlink)
- - `forge install OpenZeppelin/openzeppelin-contracts --no-git` Example (OpenZeppelin):
- - Run it from inside the project folder (where foundry.toml is), so it goes into that project's lib/

## Build / Compile

- `forge build` — compile contracts (skips if no files changed)
- `forge build` / `forge compile` — compile contracts (same thing; skips if no files changed)

## Local blockchain

- `anvil` — start local chain (chain ID 31337, RPC http://127.0.0.1:8545)

## Deploy

- `forge create src/SimpleStorage.sol:SimpleStorage --interactive --broadcast` — deploy one contract
- `forge create src/SimpleStorage.sol:SimpleStorage --rpc-url http://127.0.0.1:8545 --private-key <anvil-key> --broadcast` — deploy one contract
- `forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545 --broadcast --private-key <key>` — deploy using a script
- Without `--broadcast` it is only a dry run

## Safety

- Never put a real wallet private key in a command (it is saved in terminal history)
