# Upgradable DutchAuction Contract

This is a Solidity smart contract for a Dutch auction of an ERC721 non-fungible token (NFT) with bids made using an ERC20 token. The contract uses OpenZeppelin libraries for ERC721, access control, and upgradability. 

The contract imports the required OpenZeppelin libraries and defines two interfaces for interacting with other contracts.
The contract inherits from the ERC721Upgradeable, UUPSUpgradeable, and OwnableUpgradeable contracts from OpenZeppelin.
The contract defines several state variables to store auction parameters, such as the reserve price, number of blocks the auction should remain open, and the current bid price.
The initialize function sets the initial state of the auction when the contract is deployed. It sets the reserve price, auction duration, and bid price decrement. It also sets the initial price, the auction end block number, and the current price. Additionally, it sets the address of the ERC20 token contract, the address of the ERC721 NFT contract, and the token ID of the NFT to be auctioned. Finally, it initializes the two interface variables for interacting with other contracts.
The bid function is used by bidders to place bids on the NFT. It checks if the auction is still open, the bid amount is sufficient, and the auction is not closed. It then updates the winning bidder address, sets the initial price to zero, and marks the auction as closed. Finally, it transfers the bid amount from the bidder to the seller and transfers the NFT to the winning bidder. The function returns the address of the winning bidder.
The closeAuction function is used by the seller to close the auction. It checks if the caller is the seller and then marks the auction as closed.
The _authorizeUpgrade function is a required function for the UUPSUpgradeable contract that restricts the ability to upgrade the contract to only the contract owner.
Overall,this is a well-written and structured Solidity contract for an ERC721 Dutch auction with ERC20 token bids.




