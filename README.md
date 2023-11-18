# SPL-20-Meta-Protocol
SPL-20 Standard for the Solscriptions Meta Protocol

SPL-20 is a new semi-fungible asset made possible by LibrePlex Solscriptions. Anyone can deploy a SPL-20 token as long as they adhere to the protocol specifications below:

- A master MCC NFT must be minted with the following deploy syntax choosing the ticker, setting the supply, and the amount contained within each inscription: ```{"p":"spl-20","op":"deploy","tick":"sols","max":"21000000","lim":"1000"}```
- Whoever deploys the MCC will also choose and image for the coin and make it publicy available for download. (They can host on their own or upload here if they like)
- Minters must download this image and mint it as a MetaPlex NFT using https://sol-tools.tonyboyle.io/nft-tools/edit-nft or https://biblio.tech/ or https://www.launchmynft.io/ (Do not use solscribe.io for SPL-20)
   - Minters must upload the byte-perfect photo as the NFT image.
   - For the NFT name syntax must perfectly match as follows: "1000 $SOLS" (The number has to perfectly match the value you specified for "lim", which can be any amount, even 1 for a fully fingible token).
   - For the NFT ticker minters must correctly spell the ticker from the deploy mint, this time WITHOUT the $ symbol, just "SOLS"
   - For the collection address, minters must use the MCC master NFT mint ID, which the project founders must make publicly available along with the image. The easiest way to do this is to save the image with the ID as the file name.
   - 0% royalties is highly encouraged but they can be set to any % the project founders choose which would act as a tax on every sale. 
   - Project founders can specify creator addresses to send & split taxes.
   - Minter must set the NFT to immutable (IsMutable = False)
   - Mint the NFT, Metaplex charges a 0.027 SOL fee per mint (In the future we will transition to LibrePlex NFT which is free of protocol level fees).
- Head to https://www.libreplex.io/inscriptions to inscribe the SPL-20 NFT.
   - Click "Inscribe Yours" > "Use Wallet Contents" > "Fetch Mints" to load the NFTs in your wallet. On the SPL-20 NFT you just made click the button that says "Create Inscription".
   - Initialize the inscription account.
   - **IMPORTANT** Upload a txt file instead of the NFT image with the following syntax, setting the "amt" value to the same as the deploys "lim" value. ```{"p":"spl-20","op":"mint","tick":"sols","amt":"1000"}```
   - **IMPORTANT** Click update image or else it will cost much more in SOL rent to inscribe the data. Once you update the final byte size displayed should be about 50-60kb. The SOL rent will be 0.07 which is LibrePlex's minimum account size (they do not receive this fee, it     gets locked away forever)
   - Click Resize to change the account size.
   - Click Inscribe to add the txt data on chain.
   - Now that is complete and you can close the inscription modal. Click the magnifying glass on the inscription and set it to immutable. That's it! You succesffuly minted 1000 $SOLS SPL-20 token.
