# SPL-20 Meta-Protocol
SPL-20 Standard for the Solscriptions Meta Protocol

SPL-20 is a new open-source, fair launch fungible token standard made possible by LibrePlex Solscriptions. Anyone can deploy an SPL-20 token as long as they adhere to the protocol specifications below.

**PROJECT CREATORS** if you are creating an SPL-20 fair-mint token follow these instructions:
- Create a new wallet to serve as the deploy wallet. Save the public address as deployaddress.txt This will be used to index the collection. ```SOLSeeX8YX5TqmkRm1YgBEjdcrZ3q4pYXo8Hbom294b```
- A master MCC NFT must be minted from this deploy wallet. Use "https://biblio.tech/" or "https://sol-tools.tonyboyle.io/nft-tools/create-nft". Include the following syntax choosing the ticker, setting the supply, and the amount contained within each mint inscription (set "lim" to 1 for a fully fungible token): ```{"p":"spl-20","op":"deploy","tick":"sols","max":"21000000","lim":"1000"}``` Ensure the royalties are set to 0% for the collection. Save this text as deploy.txt and addtionally save the mint ID of this master NFT as collection.txt This will also be used to index the collection. ```G4tVHkeptBw8bXXamYFbhw6wuwB1vnyS5XpGZDK78ak```
- Make a file called inscribe.txt and include the following syntax for the mint inscription, setting the "amt" value to the same as the deploy's "lim" value. ```{"p":"spl-20","op":"mint","tick":"sols","amt":"1000"}```
- Fork this repo and create a pull request after adding a folder with your ticker name and the following files inside (do not include the "$"). Ticker names must be unique but there is no character limit, aside from the character limit on the NFT name metadata field.
   - A square image (png or webp) file for your token. It can optionally display the mint inscription JSON text.
   - deployaddress.txt
   - collection.txt
   - inscribe.txt
   - (No, you do NOT need to upload deploy.txt)
- Once the PR has been merged the information is made public and you can launch whenever you like by inscribing the deploy NFT at "https://www.libreplex.io/inscriptions" we suggest not deploying sooner than this step or someone may see it being inscribed and try to front run the mint.
   - Inscribe the deploy mint NFT https://www.libreplex.io/inscriptions by clicking "Inscribe Yours" > "Use Wallet Contents" > "Fetch Mints" to load the NFT in your wallet. On the deploy NFT click the button that says "Create Inscription".
   - Intialize the inscription account.
   - Choose custom and upload the deploy.txt file.
   - Click update image or it will not register the newly uploaded file (the txt file should be about 70-80b).
   - Resize the account to fit the txt file. The SOL rent will be 0.07 which is LibrePlex's minimum account size (they do not receive this fee, it gets locked away forever).
   - Inscribe the txt file!
   - Now that is complete and you can close the inscription modal. Click the magnifying glass on the inscription and set it to immutable. If you accidentally locked up too much rent you can reclaim it here, but only while it is mutable, once you make it immutable you can          never claim back the rent.
- That's it! Your token is officially fair-launched, better hurry up and start minting!


**TOKEN MINTERS** if you are looking to mint a newly launched SPL-20 token follow these instructions:
- Ensure the coin isn't sold out, for help you can head to the Libreplex discord https://discord.gg/6tDfht4qdB
- Download the folder of the coin you want to mint it will contain all the files you need.
- Use "https://biblio.tech/" or "https://sol-tools.tonyboyle.io/nft-tools/create-nft" to mint a new NFT with the following metadata parameters. Ensure there are no errors in this process Every step in bold is mandatory.
   - **Image:** Upload the provided png or webp as the main NFT image. Do NOT upload an "Animation File" or "Multimedia" or any media other than the provided image file. **THIS STEP IS MANDATORY**
   - **Name:** ```$1000 SOLS``` (Ensure to include the $ symbol and that the number matches the "amt" value in the provided inscribe.txt file (1000 for SOLS, but can be any integer the project creators choose) and ensure the ticker name is spelled properly). **MANDATORY**
   - **SYMBOL:** ```SOLS``` (Ensure you do NOT incldue the $ symbol and that the ticker name is spelled properly). 
   - **ROYALTIES:** Set to 0% **MANDATORY**
   - **CREATORS:** ```SOLSeeX8YX5TqmkRm1YgBEjdcrZ3q4pYXo8Hbom294b``` (Use the provided creator address within the deployaddress.txt file.) **MANDATORY**
   - **COLLECTION:** ```G4tVHkeptBw8bXXamYFbhw6wuwB1vnyS5XpGZDK78ak``` (Use the provided collection address within the collection.txt file.) **MANDATORY**
   - **MUTABILITY:** False / Off (Check advanced settings for this on Sol-Tools or toggle off for Biblio). **MANDATORY**
- Mint the NFT for 0.027 SOL (This is a MetaPlex fee. In the future we will transition to LibrePlex NFT standard which is free of protocol level fees like this).
- Head to https://www.libreplex.io/inscriptions to inscribe the SPL-20 NFT.
   - Click "Inscribe Yours" > "Use Wallet Contents" > "Fetch Mints" to load the NFTs in your wallet. On the SPL-20 NFT you just made click the button that says "Create Inscription".
   - Initialize the inscription account.
   - **IMPORTANT** Choose custom and upload the inscribe.txt file. Make sure to click update image after or it will not register the new file and it will instead inscribe the image and be overcharged for rent. Do not inscribe the image.
   - Once you update the final byte size displayed should be about 50-60b. Click Resize to change the account size. The SOL rent will be 0.07 which is LibrePlex's minimum account size (they do not receive this fee, it gets locked away forever).
   - Click Inscribe to add the txt data on chain.
   - Now that is complete and you can close the inscription modal. Click the magnifying glass. First ensure you see the txt contents being displayed, it should look something like this ```{"p":"spl-20","op":"mint","tick":"sols","amt":"1000"}``` If it does you can set it to       immutable. If you see the image twice, you inscribed the image. Go back to the upload and re-upload the txt file, click update image, then resize, then inscribe again, then had back to the scanner to reclaim the rent. THEN you can make it immutable. Once you make it          immutable you can never claim the rent back.
- That's it! All done, better hurry up and inscribe another one before they sell out~
