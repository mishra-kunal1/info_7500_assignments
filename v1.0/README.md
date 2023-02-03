# Dutch Auction

This is a Solidity smart contract for a basic Dutch auction on the Ethereum blockchain. A Dutch auction is a type of auction where the price starts high and decreases over time until a buyer is willing to accept the current price.

The contract defines the following variables:

seller: the address of the seller who created the auction
reservePrice: the minimum price the seller is willing to accept
numBlocksAuctionOpen: the number of blocks the auction will be open for
offerPriceDecrement: the amount by which the price decrements each block
initialPrice: the starting price of the auction
currentPrice: the current price of the auction
winner: the address of the winning bidder
auctionEndBlock: the block number when the auction will end
auctionClosed: a boolean indicating whether the auction has closed or not
The contract has one function bid that allows a buyer to place a bid in the auction. The function checks if the auction has ended and if the bid value is greater than or equal to the current price of the auction. If both conditions are met, the winner of the auction is set to the bidding address and the funds are transferred to the seller. The function returns the winning bidder's address.
