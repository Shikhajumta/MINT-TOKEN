# MINT-TOKEN
# Simple overview of purpose
This project creates a token contract for the Ethereum blockchain. This token can be minted (created), transferred between users, and burned (destroyed).

# Description
This Solidity code defines an ERC20 token contract. ERC20 is a standard for tokens on the Ethereum blockchain. This specific contract allows the owner to mint new tokens, users to transfer tokens between each other, and users to burn their own tokens. It uses OpenZeppelin's libraries for ERC20 functionality and ownership control.

# Getting Started

# Remix Setup:

Open Remix in your web browser.
Create a new file and paste the following code into it:
Code snippet
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {

  constructor(string memory name, string memory symbol) ERC20(name, symbol) Ownable(msg.sender) {
    // Mint initial supply to the contract deployer
    _mint(msg.sender, 1000000 * 10 ** decimals());
  }

  // Function to allow the owner to mint tokens to a specified address
  function mint(address to, uint256 amount) public onlyOwner {
    _mint(to, amount);
  }

  // Function to allow any user to burn their own tokens
  function burn(uint256 amount) public {
    _burn(msg.sender, amount);
  }

  // Function to transfer tokens
  function transfer(address to, uint256 amount) public override returns (bool) {
    return super.transfer(to, amount);
  }

  // Function to transfer tokens from one address to another
  function transferFrom(address from, address to, uint256 amount) public override returns (bool) {
    return super.transferFrom(from, to, amount);
  }
}
Use code with caution.

Compile:
Go to the "Solidity Compiler" tab.
Select the appropriate compiler version (e.g., 0.8.0).
Click "Compile" to compile your contract.

Deploy:
Go to the "Deploy & Run Transactions" tab.
Select your contract from the dropdown menu.
Choose an environment (e.g., JavaScript VM for testing).
Enter a name and symbol for your token in the constructor arguments.
Click "Deploy" to deploy your ERC20 token contract.
Interacting with the Contract (After Deployment)

# Remix Interaction:

Mint Tokens: Use the mint function to mint tokens to specified addresses. You must be logged in as the contract owner (the address you deployed the contract from).
Transfer Tokens: Use the transfer function to transfer tokens between addresses.
Burn Tokens: Use the burn function to burn tokens from your own address, reducing the total supply.

# MetaMask Integration:
Ensure you have MetaMask installed and configured on your browser.
Within Remix, click the "Connect" button in the "Deploy & Run Transactions" tab.
Select "MetaMask" from the available wallets.
Follow the MetaMask prompts to connect your wallet to Remix.
Now, when you interact with the contract functions in Remix (e.g., calling mint or burn), MetaMask will prompt you to confirm the transaction using your connected wallet.

# Authors
Shikha Jumta
jumtashikha000@gmail.com

# License
This project is licensed under the MIT License - see the LICENSE file for details.

