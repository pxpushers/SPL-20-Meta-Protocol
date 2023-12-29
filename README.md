# SPL20 Meta Protocol

SPL20 is a new open-source, fair launch fungible token meta protocol built on top of LibrePlex Solscriptions & Metaplex NFTs inspired by BRC20. Anyone can deploy an SPL20 token as long as they adhere to the protocol specifications below. **NOT TO BE CONFUSED WITH SPL TOKENS, SPL-20 IS NOT IN ANY WAY AFFILATIED WITH THE SOLANA PROGRAM LIBRARY AND WAS NOT CREATED BY SOLANA LABS.**

## **PROJECT CREATORS** if you are creating an SPL20 fair-mint token follow these instructions:
- A deploy inscription must first be inscribed to launch an SPL20 token. Use the following JSON syntax to set the meta protocol (do not change), ticker name (any length), supply and limit value of each mint inscription (you determine these values) ```{"p":"spl-20","op":"deploy","tick":"sols","max":"21000000","lim":"1000"}``` Save this text as deploy.txt
- Mint an NFT with any tool of your liking using a logo image file as the artwork for the token (this logo will also be displayed when/if listed on DEX's, CEX's, price tracking applications, etc... (https://biblio.tech/tools/nft-suite, https://sol-tools.tonyboyle.io/nft-tools/create-nft)
- Inscribe the deploy.txt text string as the on-chain art, by selecting "custom" when using LibrePlex's inscriber UI.
- Make a file called inscribe.txt and include the following syntax for the mint inscription, setting the "amt" value to the same as the deploy's "lim" value, which represents the amount of tokens held in each SPL20 NFT. ```{"p":"spl-20","op":"mint","tick":"sols","amt":"1000"}```
- Make the logo artwork and the inscribe.txt file public in order to launch your SPL20. From there anyone can inscribe a free mint inscription!

How to use LibrePlex to inscribe:
   - Visit https://www.libreplex.io/inscriptions and click "Inscribe Yours" > "Use Wallet Contents" > "Fetch Mints" to load the NFT in your wallet. On the NFT you want to inscribe click the button that says "Create Inscription".
   - Intialize the inscription account.
   - Choose custom and upload the inscribe.txt file.
   - Resize the account to fit the txt file. The SOL rent will be much lower vs inscribing the artwork.
   - Inscribe the txt file!
   - Now that is complete and you can close the inscribe window. Click the magnifying glass on the inscription and set it to immutable. If you accidentally locked up too much rent you can reclaim it here, but only while it is mutable, once you make it immutable you can never claim back the rent.


## **TOKEN MINTERS** if you are looking to mint a newly launched SPL20 token follow these instructions:
- Ensure the coin isn't sold out, for help you can head to the Libreplex discord https://discord.gg/6tDfht4qdB
- Use a tool of your choice to mint a new NFT with the following metadata parameters. (https://biblio.tech/ or https://sol-tools.tonyboyle.io/nft-tools/create-nft)
   - **Image:** Upload the provided png or webp as the main NFT image. **THIS STEP IS MANDATORY**
   - **Name:** ```SOLS``` **MANDATORY**
   - **ROYALTIES:** Set to 0% **MANDATORY**
   - **MUTABILITY:** False / Off (Check advanced settings for this on Sol-Tools or toggle off for Biblio). **MANDATORY**
- Mint the NFT for 0.027 SOL (This is a MetaPlex fee. In the future we will transition to LibrePlex NFT standard which is free of protocol level fees like this).
- Head to https://www.libreplex.io/inscriptions to inscribe the SPL20 NFT.
   - Click "Inscribe Yours" > "Use Wallet Contents" > "Fetch Mints" to load the NFTs in your wallet. On the SPL20 NFT you just made click the button that says "Create Inscription".
   - Initialize the inscription account.
   - **IMPORTANT** Choose custom and upload the inscribe.txt file. Do not inscribe the image.
   - Once you update the final byte size displayed should be about 50-60b. Click Resize to change the account size. The SOL rent will gets locked away forever.
   - Click Inscribe to add the txt data on chain.
   - Now that is complete and you can close the inscribe window. Click the magnifying glass. First ensure you see the txt contents being displayed, it should look something like this ```{"p":"spl-20","op":"mint","tick":"sols","amt":"1000"}``` If it does you can set it to immutable. If you see the image twice, you inscribed the image. Go back to the upload and re-upload the txt file, click update image, then resize, then inscribe again, then had back to the scanner to reclaim the rent. THEN you can make it immutable. Once you make it immutable you can never claim the rent back.
- That's it!


