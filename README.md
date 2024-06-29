# MINT-TOKEN
# Overview
This Solidity program implements an ERC20 token contract that enables token minting by the contract owner and token transfers and burns by any user. Built on the Ethereum blockchain, this contract leverages OpenZeppelin's ERC20 standard and Ownable functionalities for ownership control.

# Description
This Solidity program implements an ERC20 token contract on the Ethereum blockchain, providing functionality for token creation, minting, transfer, and burning. The contract utilizes OpenZeppelin's ERC20 standard for token operations and Ownable for access control, ensuring secure management of token ownership and operations.

Key Features:
Token Minting: The contract owner can mint new tokens and allocate them to specific addresses.
Token Transfers: Users can transfer tokens between addresses using standard ERC20 transfer functions.
Token Burning: Users can burn (destroy) their own tokens, reducing the total token supply.

# Execution
o deploy and interact with the ERC20 token contract using Remix, follow these steps:

Deployment:

Open https://remix.ethereum.org in your web browser.
Create a new file and paste mytoken.sol code into it.
Compile the contract by selecting the appropriate compiler version (e.g., 0.8.0) in the "Solidity Compiler" tab.
Click on the "Compile" button to compile your contract.
Navigate to the "Deploy & Run Transactions" tab in Remix.

Deploying the Contract:

Select your contract from the dropdown menu.
Choose the environment (e.g., JavaScript VM for testing).
Enter a name and symbol for your token in the constructor arguments.
Click on the "Deploy" button to deploy your ERC20 token contract.

Interacting with the Contract:

After deployment, interact with the ERC20 token contract through Remix:
Mint Tokens: Use the mint function to mint tokens to specified addresses. Ensure you are logged in as the contract owner (the address you deployed the contract from).
Transfer Tokens: Use the transfer function to transfer tokens between addresses.
Burn Tokens: Use the burn function to burn tokens from your own address, reducing the total supply.

# Authors
Shikha Jumta jumtashikha000@gmail.com

# License
This project is licensed under the MIT License - see the LICENSE file for details
