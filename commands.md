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

## Git

### One-time setup

- `git --version` — check Git is installed
- - `git --version` → git version 2.43.0 - example

- `git config --global user.name "<name>"` — set your name
- - `git config --global user.name "abc"` - example

- `git config --global user.email "<email>"` — set your GitHub email
- - `git config --global user.email "abc@abc.com"` - example

- `git config --global --list` — check name and email

### Getting a repo

- `git clone <url> .` — clone into the current folder (the dot = this folder)
- - `cd ~/Foundry` then `git clone https://github.com/d339ak/Foundry.git .`

### Daily work (run from ~/Foundry)

- `Ctrl + Shift + G` — VS Code Source Control shortcut: does git add, git commit and git push together (write message → Commit → Sync Changes)

### Daily work (run from ~/Foundry)

- `git status` — see what changed (green = new, red = not staged)

- `git add .` — stage all changes
- - `git add Simple-Storage/src/SimpleStorage.sol` — stage just one file

- `git commit -m "<message>"` — save a snapshot
- - `git commit -m "Added SimpleStorage deploy script"`

- `git push` — send commits to GitHub

- `git pull` — get latest from GitHub (use in the D drive copy)

### Fixing mistakes

- `git rm -r --cached <folder>` — stop tracking on GitHub, keep on laptop
- - `git rm -r --cached Simple-Storage/lib`

## VS Code shortcuts

- `Ctrl + S` — save file
- `Ctrl + Shift + P` — command palette (search any setting or command)
- `Shift + Alt + F` — format document
- `Ctrl + -` / `Ctrl + +` / `Ctrl + 0` — zoom out / in / reset
- `Ctrl + Shift + G` — Source Control (add, commit, push)
- `Ctrl + Shift + V` — paste in Ubuntu terminal
- `Right-click from mouse` — paste in Ubuntu terminal
- `code .` — open current folder in VS Code (from Ubuntu terminal)
- `explorer.exe .` — open current folder in Windows Explorer
