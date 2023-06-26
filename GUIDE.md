### Setup
We need to create a Hardhat project, the process is straightforward but we are going to recap just for a summary.

1. Create a folder for your new project, and run `npm init`
```bash
$ cd ./your-project
$ npm init -y
```

2. Install hardhat
```bash
$ npm install --save-dev hardhat
```

3. Initialize your hardhat project
```bash
$ npx hardhat
888    888                      888 888               888
888    888                      888 888               888
888    888                      888 888               888
8888888888  8888b.  888d888 .d88888 88888b.   8888b.  888888
888    888     "88b 888P"  d88" 888 888 "88b     "88b 888
888    888 .d888888 888    888  888 888  888 .d888888 888
888    888 888  888 888    Y88b 888 888  888 888  888 Y88b.
888    888 "Y888888 888     "Y88888 888  888 "Y888888  "Y888

👷 Welcome to Hardhat v2.9.9 👷‍

? What do you want to do? …
❯ Create a JavaScript project
  Create a TypeScript project
  Create an empty hardhat.config.js
  Quit
```
We are going to use JavaScript for this guide but feel free to use TypeScript if you are familiar with it.

## Smart contract
For the smart contract section, we are going to create a ERC20 token using OpenZeppelin, and we are going to make it mintable.

First, we need to install OpenZeppelin, OpenZeppelin is a library for secure smart contract development, build on a solid foundation of community-vetted code.

```bash
$ npm install @openzeppelin/contracts
```

After that is completely inside the `contracts` folder we are going to create a `Token.sol` file, and put the following contents inside of it:

```sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract Points is ERC20, Ownable {
    constructor() ERC20("Sponge", "SPG") {}

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}
```
