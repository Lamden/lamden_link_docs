### Overview

The picture below shows the basic process we are going to walk through to swap from Ethereum to Lamden.  We start in the Lamden Wallet, we use Lamden Link to move the token across to Ethereum where it will be held in Metamask, we unwrap the token using Etherscan, then finish in Metamask.    
![Linkdoc1](./static/L2ELink1.png ':size=700')    

As discussed previously, you will require:
* Metamask, installed and logged in
* Lamden Wallet, installed and logged in
* A small amount of Lamden TAU to cover link fees - approx 5 TAU
* A Wrapped token to swap (WETH), and also some Ethereum for gas fees (to unwrap the Ethereum if required)

### Preliminary steps
If this is your first time using the Lamden Link you will require an account to be created to hold your WETH within the Lamden Wallet and also to authorise Lamden Link on Metamask.  

1. Head to Lamden Link - www.lamdenlink.com    

2. You will need to click *Connect* to authorise Lamden Link for use with Metamask Wallet.  Follow the prompts similar to the images below, read the details, click *Next*, then click *Connect*.    
![Linkdoc4](./static/Link4.png ':size=600')    

3. Click *Connect* again to create the account within your Lamden Wallet. You will be guided through the "Lamden Account Creation". You will get two prompts similar to below, read the instructions, click *NEXT*, then *Create Account*.    
![Linkdoc3](./static/Link3.png ':size=600')    

>[!Note]
>Creating a separate account for the Link app is a normal security feature of Lamden to prevent access to your full wallet by any one application.   

### Lamden Wallet
Place the WETH you would like to send to the Ethereum network within the Lamden Link account in your Lamden Wallet. 

#### Making the WETH visible    
This step is optional, and the swap will function without performing this step. This is just to make the WETH token visible within the Lamden Wallet. Follow these steps:    
1. Within your Lamden Wallet, click *ACCOUNTS & TOKENS*    
2. From the Add New Account or Token popup:    
* Select *Token* from the "What to Add?" option.
* In Contract Name add `con_weth_lst001`, then press *Enter*
* Details should be like below, then click *Add Token*    
![Linkdoc9](./static/Link9.png ':size=300')

You will see the WETH along with any other tokens you have added to the wallet just above your other accounts.

### Lamden Link

1. Head back to Lamden Link - www.lamdenlink.com    

2. We are now basically ready to swap.  For this example transaction we are swapping from the Lamden network to Ethereum, so the arrow should be pointing towards Ethereum.     
* Select the Token to send in the *Token Name* dropdown (this should be only WETH currently)
* Input the amount to send in the *Amount* box
* Click the bottom button to send it - this should be *Send tokens to Ethereum*.    
>[!Tip] 
>If the arrows are confusing the button at the bottom will tell you what you are about to do - either "Send tokens to Lamden" or "Send tokens to Ethereum".   

3. The Lamden wallet will ask for confirmation to send the WETH, read the details, confirm the amount being sent the click *Approve*. (Approx fee 5 TAU).    

4. You will get a popup from Metamask to confirm the deposit on the Ethereum side (Ethereum gas fees apply), click *Confirm* to proceed.   

5. You will receive the notification that swapping was successful on the Lamden Link site (Image Below).    
![Linkdoc8](./static/Link8.png ':size=800')

>[!Tip]
>You can verify this by clicking the *switch* option, then selecting WETH from the token name dropdown. Your WETH should be sitting there on the Ethereum side. You can also verify this in Metamask (Next Step)    

>[!Note]
>The remainder of this guide is devoted to unwrapping your WETH. If you don't need to unwrap it, you have finished!    

### Unwrapping your WETH (on Etherscan)


>[!Note]
>Unwrapping your Ethereum is all performed on the Ethereum side, be aware the speed and transaction costs differ significantly compared to using the Lamden network. Be prepared to wait for the Ethereum network to process the transaction and the possibility of high gas costs.    

1. First take a quick detour to https://eth-converter.com/ as we need to convert your WETH (Ether) into the WEI equivalent. Enter the amount your would like to unwrap and copy the WEI amount listed.    

2. New we can go to Etherscan, specifically we need the WETH write contract (`0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2`). [Link here will get you to the right spot.](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2#writeContract)    

3. Connect Metamask to the Etherscan site by clicking the button highlighted below. Follow the prompts on Metamask to approve the site to interact with Metamask.    
![Linkdoc2](./static/Link2.png ':size=600')

>[!Note] 
>The button you clicked should now be showing as green. If it is still red, click the button again, follow the prompts and it should now go green.    

4. Click the withdraw dropdown to open the section. Input the amount of WEI you copied from step 1 in the 'wad (uint256)' textbox, then click *Write*.    

>[!Note]
>If you get an error. Check to make sure you have enough Ethereum to swap, and that you have enough for gas. Also make sure you are still connected - green light mentioned previously.    

5. You will get a popup from Metamask to confirm the transaction. Read the details, understand the gas fees associated, then click Confirm to continue.    

6. Wait for the Metamask confirmation.    

>[!Tip]
>You can check the progress of a pending transaction in Metamask by clicking *Activity*, then below that *should* be the last transaction, click this. The popup offers a link in the top left to Etherscan to view to progress of the transaction. Completely optional, as Metamask keeps monitoring this for you - but if you are bored waiting can this can be good to check.    

7. The unwrapping should have occured and you will now see the Ethereum (ETH) in your Metamask.

### Resume a Swap from Lamden to Ethereum
In the event that a swap from Lamden to Ethereum is interrupted halfway you will need to restart the process manually.
You will know you're in this situation because the Lamden has burnt your tokens (they no longer are in your wallet), but no tokens were transferred to you on the Ethereum side.  This is generally the case when the Ethereum transaction that completes the process was cancelled, failed or is pending due to low gas.

If the event of `pending` transaction due to low gas you can use metamask to "speed up" a transaction. Consult metamask for those details.

In the event of a `cancelled` or `failed` transaction follow the instructions below to restart the swap process.

<strong>What you will need:</strong>
1. `Burn Hash`: This hash can be obtained by opening your Lamden Link account in the Lamden Wallet and finding the most recent transaction with the method of `Burn`.

<strong>Steps to resume:</strong>
1. Ensure the `From` box says Lamden and the `To` box says "Ethereum".  If not, click the `Switch` button.
2. Click the `Resume Swap` button
3. In the `Lamden BURN Transaction Hash` box enter the `Burn Hash` you retrieved above
4. Click the `Send Tokens to Ethereum` button to reinitiate the swap process
