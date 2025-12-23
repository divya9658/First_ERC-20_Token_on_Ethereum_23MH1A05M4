# First_ERC-20_Token_on_Ethereum_23MH1A05M4
# 🪙 MyToken (MTK)
# Overview

MyToken (MTK) is a simple ERC-20 compatible token created on the Ethereum blockchain for learning and development purposes. It demonstrates how a basic cryptocurrency token works, including sending tokens, approving others to transfer tokens on your behalf, and tracking balances.

# Token Details

The token name is MyToken, and it uses the symbol MTK. It has 18 decimals, meaning values are represented with 18 decimal precision. The total supply of the token is 1,000,000 MTK, and all the tokens are automatically minted to the deployer’s wallet at the time of deployment.

# Features

This token includes all the standard ERC-20 functionalities such as transferring tokens between users, approving another account to spend tokens, and performing delegated transfers using transferFrom. It emits Transfer and Approval events for transparency and maintains balances securely on the blockchain.

# How to Deploy

To deploy the contract, open Remix IDE and create a new file named MyToken.sol. Paste the contract code, then compile it using any Solidity compiler version from 0.8.x series. After compiling, go to the Deploy & Run panel, choose any environment such as Remix VM for testing or MetaMask for live networks, enter the total supply you want, and then deploy the contract. Once deployed, the deployer will hold all tokens.

# How to Use
- Check Balance

You can retrieve the token balance of any wallet address using the balanceOf(address) function. It returns the token amount owned by the given address.

- Transfer Tokens

To send tokens from your address to another, use the transfer(to, amount) function. Your balance will decrease, and the recipient’s balance will increase immediately.

- Approve Spending

If you want to allow another account to spend tokens from your wallet, use the approve(spender, amount) function. This only gives permission and does not transfer any tokens yet.

- TransferFrom

After approval, the approved account can use transferFrom(from, to, amount) to transfer tokens from your wallet to another. This is useful for marketplaces, exchanges, or automated payments.

- Check Allowance

To see how many tokens one account is allowed to spend from another, use the allowance(owner, spender) function.

- Understanding Token Values

Since the token uses 18 decimals, token values must be multiplied by 10^18. For example, 1 MTK is represented as 1000000000000000000 in the contract, and 10 MTK becomes 10000000000000000000. This enables precise storage similar to how Ethereum stores values.

- Events

Whenever tokens are transferred or approved, the contract emits events. Transfer events record token movements between addresses, and Approval events record permissions given to spend tokens. These events can be viewed on block explorers or in dApp logs.

- Testing Suggestions

You can test by transferring tokens to another account, checking balances before and after, approving another account for a certain amount, then using transferFrom to move tokens based on the approval. You should also test invalid cases like transferring more than the available balance or using transferFrom without approval to ensure they fail as expected.
