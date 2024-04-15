# ERC721 NFT Contract

This Solidity smart contract implements an ERC721 Non-Fungible Token (NFT) using the OpenZeppelin library.

## Description

The `MyNFT` contract allows users to mint ERC721 NFTs by providing a token URI. It supports the standard ERC721 functions for managing ownership and metadata of NFTs.

## Contract Details

- **Name**: MyNFT
- **Symbol**: NFT
- **Token Metadata**: Stored on-chain using ERC721URIStorage extension.

## Core Features

- **Minting**: Users can mint new NFTs by providing a token URI and paying the specified price in Ether.
- **Ownership**: Tracks ownership of NFTs using the ERC721 standard.
- **Token URI**: Sets the token URI for each minted NFT, allowing off-chain metadata to be associated with the token.

## Usage

1. **Deployment**: Deploy the contract on the Ethereum network, specifying the price for minting NFTs.
2. **Minting**: Users can mint new NFTs by calling the `mintNFT` function, providing a token URI and paying the specified price in Ether.

### Example Usage

```solidity
// Deploy the contract with a minting price of 0.1 Ether
MyNFT myNFT = new MyNFT(0.1 ether);

// Mint a new NFT
uint256 tokenId = myNFT.mintNFT("https://example.com/token1");

// Get token metadata
string memory tokenURI = myNFT.tokenURI(tokenId);
