### MintContract

MintContract is responsible for minting NFTs. It uses OpenZeppelin's ERC721 standard to implement the NFTs. It also provides a way to limit the number of NFTs that can be minted. The maximum number of tokens that can be minted is specified at the time of initialization and can't be changed.

The contract exposes three functions:

initialize: Initializes the contract with the maximum limit of tokens that can be minted.
safeMint: Mints a new NFT and transfers ownership to the specified address. It also takes an optional string parameter for metadata of the token.
getMaxLimit: Returns the maximum number of tokens that can be minted.

### NFTDutchAuction

NFTDutchAuction is a Dutch auction implementation for NFTs. The seller specifies the reserve price, the number of blocks the auction will be open, and the price decrement at each block. The initial price is calculated based on these values, and the auction starts.

Bidders can place their bids, but they can't bid less than the current price or after the auction has ended. If a bid is accepted, the NFT is transferred to the winner of the auction, and the highest bidder pays the price.
