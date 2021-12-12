### Overview

Transferring non-native tokens (ex. ETH) from Lamden to either Ethereum (ERC20) or Binance Smart Chain (BEP20) is a four step process. Before starting, you will require:
* Lamden Wallet, installed and logged in
* MetaMask Wallet, installed and logged in
* A small amount of Lamden TAU to cover fees - approximately 5 TAU
* A sufficient amount of Ethereum or BNB to cover gas fees (especially during periods of high traffic)

### Initiating the Swap

The first steps are fairly explanatory. You'll be prompted with a series of steps to select the blockchain where your tokens currently exist, the blockchain destination, and which token you're intending to move.

1. Click *Start a New Swap*
2. Click Lamden
3. Click which blockchain is the destination (Ethereum or Binance Smart Chain)
4. Select the token you want to move

### STEP 1
![lamden-external-step1](./static/lamden-external-step1.png ':size=800')

1. You'll be prompted to connect your Lamden Wallet
* If this is your first time using Lamden Link, then you'll be asked to *Create Linked Account*
* If you're a returning user, you'll be asked to *Connect To Lamden Wallet*
2. Enter the quantity of tokens you'd like to move
3. Click *Next Step*

>[!Tip]
>Some common issues you might encounter:<br/>
> *Not Connected* - ensure you have the [Lamden Wallet](https://chrome.google.com/webstore/detail/lamden-wallet-browser-ext/fhfffofbcgbjjojdnpcfompojdjjhdim) installed on a compatible browser and fully logged in
> *Wallet Locked* - you must login to your Lamden Wallet

### STEP 2
![lamden-external-step2](./static/lamden-external-step2.png ':size=800')

1. You'll be prompted to connect your MetaMask Wallet

>[!Tip]
>Some common issues you might encounter:
> *Not Connected* - ensure you have the [MetaMask Wallet](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=en) installed on a compatible browser and fully logged in
> *Switch Metamask to Binance Smart Chain/Ethereum Mainnet* - within MetaMask, click the networks drop-down at the top and switch to the correct network
> *No BNB/ETH Balance* - you need sufficient balance in your MetaMask wallet to cover [BNB](https://bscscan.com/gastracker) or [ETH](https://etherscan.io/gastracker) gas fees
> *Something went wrong...* - ensure you're on a desktop computer (LamdenLink is not compatible with mobile devices) and that pop-up blockers are disabled

### STEP 3

During Step 3, you'll first approve the burn and then complete the burn to create a Proof-of-Burn.

1. Click *Approve Burn* to begin the burn
![lamden-external-step3a](./static/lamden-external-step3a.png ':size=800')

2. Lamden Wallet will pop-up...click *Approve*

![lamden-external-step3b](./static/lamden-external-step3b.png ':size=300')

3. Click *Start Burn*
![lamden-external-step3c](./static/lamden-external-step3c.png ':size=800')

4. Lamden Wallet will pop-up...click *Approve*

![lamden-external-step3d](./static/lamden-external-step3d.png ':size=300')

5. Click *Next Step*
![lamden-external-step3e](./static/lamden-external-step3e.png ':size=800')

>[!Tip]
>Some common issues you might encounter:
> *Attempting to Burn tokens on the Lamden Blockchain (check for Lamden Wallet popup)...* - if after clicking the *Start Burn* button you don't get the Lamden Wallet pop-up, you can refresh the browser page and follow steps 1-3 again

### STEP 4
![lamden-external-step4a](./static/lamden-external-step4a.png ':size=800')

During Step 4, you'll withdraw your tokens to MetaMask.

1. Click *Withdraw Tokens*
2. MetaMask will pop-up prompting you to confirm the gas fees..click *Confirm* (please be patient)

![lamden-external-step4b](./static/lamden-external-step4b.png ':size=300')

>[!Tip]
>Some common issues you might encounter:
> *Could not get proof of recording from hash recording* - refresh the browser page and follow the steps again; it should re-prompt you for the transaction

### Completed

Congrats! You've completed the swap and your tokens are now on a different blockchain. You can view any of the completed transactions or return to the homepage.

### Resume a Swap
In the event that a swap from Lamden to Ethereum/Binance Smart Chain is interrupted halfway, you will need to restart the process manually. You will know you're in this situation because Lamden has burnt your tokens (they are no longer in your wallet), but no tokens were transferred to your MetaMask Wallet. This is generally the case when the MetaMask transaction that completes the process was cancelled, failed or is pending due to low gas.

If the event of `pending` transaction due to low gas you can use MetaMask to "speed up" a transaction. Consult MetaMask for those details.

In the event of a `cancelled` or `failed` transaction, follow the instructions below to restart the swap process.

<strong>What you will need:</strong>
1. `Burn Hash`: This hash can be obtained by opening your Lamden Link account in the Lamden Wallet and finding the most recent transaction with the method of `Burn`.

<strong>Steps to resume:</strong>
1. Ensure the `From` box says Lamden and the `To` box says "Ethereum" or "Binance Smart Chain".  If not, click the `Switch` button.
2. Click the `Resume Swap` button
3. In the `Lamden BURN Transaction Hash` box enter the `Burn Hash` you retrieved above
4. Click the `Send Tokens to Ethereum` button to reinitiate the swap process

### Unwrapping your WETH (on Etherscan)

>[!Note]
>Unwrapping your Ethereum is all performed on the Ethereum side, be aware the speed and transaction costs differ significantly compared to using the Lamden network. Be prepared to wait for the Ethereum network to process the transaction and the possibility of high gas costs.    

1. First take a quick detour to https://eth-converter.com/ as we need to convert your WETH (Ether) into the WEI equivalent. Enter the amount you would like to unwrap and copy the WEI amount listed.    

2. Now we can go to Etherscan, specifically we need the WETH write contract (`0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2`). [Link here will get you to the right spot.](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2#writeContract)    

3. Connect MetaMask to the Etherscan site by clicking the button highlighted below. Follow the prompts on MetaMask to approve the site to interact with MetaMask.    
![Linkdoc2](./static/Link2.png ':size=600')

>[!Note] 
>The button you clicked should now be showing as green. If it is still red, click the button again, follow the prompts and it should now go green.

4. Click the withdraw dropdown to open the section. Input the amount of WEI you copied from step 1 in the 'wad (uint256)' textbox, then click *Write*.

>[!Note]
>If you get an error. Check to make sure you have enough Ethereum to swap, and that you have enough for gas. Also make sure you are still connected - green light mentioned previously.

5. You will get a popup from MetaMask to confirm the transaction. Read the details, understand the gas fees associated, then click *Confirm* to continue.

6. Wait for the MetaMask confirmation.    

>[!Tip]
>You can check the progress of a pending transaction in MetaMask by clicking *Activity*, then below that *should* be the last transaction, click this. The popup offers a link in the top left to Etherscan to view the progress of the transaction. Completely optional, as MetaMask keeps monitoring this for you - but doesn't hurt to check if you are bored and waiting.

7. The unwrapping should have occurred and you will now see the Ethereum (ETH) in your MetaMask Wallet.
