## NFT Dutch Auction with ERC20 Bids
This is a Solidity smart contract that implements a Dutch auction for an NFT (non-fungible token) with bids in an ERC20 token. In a Dutch auction, the price of the item is gradually reduced until a buyer accepts the price.

Requirements
Solidity 0.8.0 or higher
OpenZeppelin Contracts 4.0.0 or higher
Usage
Initialize the Auction
To create a new auction, deploy the NFTDutchAuction_ERC20Bids contract with the following parameters:

erc20TokenAddress: The address of the ERC20 token that will be used for bidding
erc721TokenAddress: The address of the ERC721 contract for the NFT to be auctioned
nftTokenId: The ID of the NFT to be auctioned
reservePrice: The minimum price for the NFT
numBlocksAuctionOpen: The number of blocks that the auction should remain open
offerPriceDecrement: The price decrement for each block after the reserve price
Place a Bid
To place a bid on the auction, call the bid function with the bid amount. The following conditions must be met:

The auction is still open.
The bid amount is greater than or equal to the reserve price.
The auction has not already been closed.
If the bid is successful, the bid amount will be transferred from the bidder's account to the auction contract, and the NFT will be transferred to the winning bidder.

Close the Auction
To close the auction, call the closeAuction function. This can only be called by the seller. Once the auction is closed, no more bids can be placed.
