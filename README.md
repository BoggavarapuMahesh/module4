# module4

The `DegenGamingToken` contract is an ERC20-compliant token with additional functionalities specific to gaming.

### Contract Details

- `name`, `symbol`, and `decimals` variables define the name, symbol, and decimal places for the token.
- `_totalSupply` keeps track of the total supply of tokens.
- `_balances` is a mapping that stores the token balances of each address.
- `_allowances` is a mapping that stores the approved token transfer amounts for each address.
- `_owner` represents the address of the contract owner.

### Events

- `Transfer` event is emitted when tokens are transferred from one address to another.
- `Approval` event is emitted when an address approves another address to spend tokens on its behalf.

### Modifiers

- `onlyOwner` modifier ensures that only the contract owner can call specific functions.

### Constructor

- The constructor sets the contract owner to the address that deploys the contract.

### ERC20 Functions

The contract implements the standard ERC20 functions:

- `totalSupply()` returns the total supply of tokens.
- `balanceOf(address account)` returns the token balance of a given address.
- `transfer(address recipient, uint256 amount)` transfers tokens from the sender's address to the recipient's address.
- `approve(address spender, uint256 amount)` approves the spender address to spend tokens on behalf of the sender.
- `transferFrom(address sender, address recipient, uint256 amount)` transfers tokens from the sender's address to the recipient's address if the sender has sufficient allowance.
- `increaseAllowance(address spender, uint256 addedValue)` increases the spender's allowance to spend tokens on behalf of the sender.
- `decreaseAllowance(address spender, uint256 subtractedValue)` decreases the spender's allowance to spend tokens on behalf of the sender.

### Additional Functions

- `mint(address account, uint256 amount)` allows the contract owner to mint new tokens and assign them to the specified account.
- `burn(uint256 amount)` allows a token holder to burn (destroy) a specific amount of their own tokens.
- `redeem(uint256 amount)` allows a token holder to redeem their tokens for in-game items or perform specific logic (to be added).
- `_transfer(address sender, address recipient, uint256 amount)` is an internal function that performs the actual token transfer.
- `_approve(address owner, address spender, uint256 amount)` is an internal function that sets the allowance for a spender on behalf of an owner.

The code provides a basic structure for an ERC20 token with minting, burning, and redemption functionalities that can be expanded upon for gaming-related features.
