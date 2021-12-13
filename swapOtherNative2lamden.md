### Overview
![5steps](./static/5steps.png ':size=800')

Transferring non-native tokens (ex. ETH) from either Ethereum (ERC20) or Binance Smart Chain (BEP20) ➡️ Lamden is a 5️⃣ step process. Before starting, you'll require:
* Lamden Wallet, installed and logged in
* MetaMask Wallet, installed and logged in
* A small amount of Lamden TAU to cover fees - approximately 5 TAU
* A sufficient amount of Ethereum or BNB to cover gas fees (especially during periods of high traffic)
* If moving Ethereum (ETH), make sure to complete the 'Wrap your Ethereum (on Etherscan)' step before initiating the swap

### Initiating the Swap

The first steps are fairly explanatory. You'll be prompted with a series of steps to select which blockchain your tokens currently exist and which token you're intending to move.

1. Click *Start a New Swap*.
2. Click the blockchain where your tokens currently reside (Ethereum or Binance Smart Chain)
3. Select the token you want to move

### STEP 1️⃣
![external-lamden-step1](./static/external-lamden-step1.png ':size=800')

In Step 1, you'll be prompted to connect your MetaMask Wallet.

1. Enter the quantity of tokens you'd like to move
2. Click *Next Step*

>[!Tip]
>Some common issues you might encounter:<br/>
> * *Not Connected* - ensure you have the [MetaMask Wallet](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=en) installed on a compatible browser and fully logged in<br/>
> * *Switch Metamask to Binance Smart Chain/Ethereum Mainnet* - within MetaMask, click the networks drop-down at the top and switch to the correct network<br/>
> * *No BNB/ETH Balance* - you need sufficient balance in your MetaMask wallet to cover [BNB](https://bscscan.com/gastracker) or [ETH](https://etherscan.io/gastracker) gas fees<br/>
> * *Something went wrong...* - ensure you're on a desktop computer (LamdenLink is not compatible with mobile devices) and that pop-up blockers are disabled

### STEP 2️⃣
![external-lamden-step2](./static/external-lamden-step2.png ':size=800')

For Step 2, you'll be prompted to connect your Lamden Wallet:
* If this is your first time using Lamden Link, then you'll be asked to *Create Linked Account*
* If you're a returning user, you'll be asked to *Connect To Lamden Wallet*

1. Click *Next Step*

>[!Tip]
>Some common issues you might encounter:<br/>
> * *Not Connected* - ensure you have the [Lamden Wallet](https://chrome.google.com/webstore/detail/lamden-wallet-browser-ext/fhfffofbcgbjjojdnpcfompojdjjhdim) installed on a compatible browser and fully logged in<br/>
> * *Wallet Locked* - you must login to your Lamden Wallet

### STEP 3️⃣
![external-lamden-step3a](./static/external-lamden-step3a.png ':size=800')

During Step 3, you'll approve Lamden Link access to your tokens in MetaMask.

1. Click *Send Token Approval* to begin
2. MetaMask Wallet will pop-up...click *Confirm*
* ![external-lamden-step3b](./static/external-lamden-step3b.png ':size=300')

### STEP 4️⃣
![external-lamden-step4a](./static/external-lamden-step4a.png ':size=800')

During Step 4, you'll lock your tokens in the Lamden Link contract.

1. Click *Create Deposit Transaction* to begin
2. MetaMask Wallet will pop-up...click *Confirm*
* ![external-lamden-step4b](./static/external-lamden-step4b.png ':size=300')

### STEP 5️⃣
![external-lamden-step5](./static/external-lamden-step5.png ':size=800')

During Step 5, Lamden Link checks for the arrival of your tokens on the Lamden network. Please wait patiently while the network confirms the arrival of your tokens. 

### Completed

Congrats! You've completed the swap and your tokens are now on the Lamden blockchain. You can view any of the completed transactions or return to the homepage.

### Adding the Token to display in the Lamden Wallet
Your token will now be in your Lamden Link account within your Lamden Wallet. If you don't see it (try clicking the refresh wheel next to your TAU amount first), then you'll need to make it visible. To do this, follow these steps:    

1. Within your Lamden Wallet, click *ACCOUNTS & TOKENS*    
2. From the Add New Account or Token popup:    
* Select *Token* from the "What to Add?" dropdown
* From the Add Existing tab, locate and select your token from the dropdown list
* Click *Add Token*

You are done! You will now see the token in your Lamden Wallet.

### Wrap your Ethereum (on Etherscan)

>[!Note]
>This step is necessary before bridging Ethereum (ETH) to Lamden. Wrapping your Ethereum is all performed on the Ethereum side, be aware the speed and transaction costs differ significantly in comparison to using the Lamden network. Be prepared to wait for the Ethereum network to process the transaction and the possibility of high gas costs.    

1. Head over to Etherscan, specifically we need the WETH write contract (`0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2`). [Link here will get you to the right spot.](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2#writeContract)    

2. Connect MetaMask to the Etherscan site by clicking the button highlighted below. Follow the prompts on MetaMask to approve the site to interact with MetaMask.    
![Linkdoc2](./static/Link2.png ':size=600')

>[!Note] 
>The button you clicked should now be showing as green. If it is still red, click the button again, follow the prompts and it should now go green.    

3. Click the deposit dropdown to open the deposit section. Input the amount of Ethereum (ETH) you would like to wrap into WETH then click *Write*.    

>[!Note]
>If you get an error. Check to make sure you have enough Ethereum to swap, also make sure you are still connected - green light mentioned previously.    

4. You will get a popup from MetaMask to confirm the transaction. Read the details, understand the gas fees associated, then click *Confirm* to continue.    

5. Wait for the MetaMask confirmation.    

>[!Tip]
>You can check the progress of a pending transaction in MetaMask by clicking *Activity*, then below that it *should* be the last transaction, click this. The popup offers a link in the top left to Etherscan to view to progress of the transaction. Completely optional, as Metamask keeps monitoring this for you - but doesn't hurt to check if you are bored and waiting.   

6. The wrapping should have occurred however we can't see the WETH until we add the token details to MetaMask. In MetaMask:    
* On the Main page, click *Assets*
* Then click *Add Token* (You may need to scroll down to see it)
* Add the following token address `0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2`
* The Token name should auto-populate with WETH and the decimals will also auto-populate with 18
* Click *Next* (you should see your WETH at this stage)
* Click *Add Token*

Thats it! You will now see the WETH in your MetaMask ready to move to the Lamden network.
