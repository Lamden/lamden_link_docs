### Overview

The picture below shows the basic process we are going to walk through to swap from Ethereum to Lamden.  Basically, we will start in Metamask, wrap the Ethereum on Etherscan, migrate it over to Lamden using the Lamden Link, and it will finish in your Lamden wallet.    
![Linkdoc1](./static/Link1.png ':size=850')    

As discussed previously, you will require:
* Metamask, installed and logged in
* Lamden Wallet, installed and logged in
* Some Ethereum to swap, and also some Ethereum for gas fees

### Wrapping your Ethereum (on Etherscan)

>[!Note]
>Wrapping your Ethereum is all performed on the Ethereum side, be aware the speed and transaction costs differ significantly to using the Lamden network. Be prepared to wait for the Ethereum network to process the transaction and the possibility of high gas costs.    

1. Head over to Etherscan, specifically we need the WETH write contract (`0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2`). [Link here will get you to the right spot.](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2#writeContract)    

2. Connect Metamask to the Etherscan site by clicking the button highlighted below. Follow the prompts on Metamask to approve the site to interact with Metamask.    
![Linkdoc2](./static/Link2.png ':size=600')

>[!Note] 
>The button you clicked should now be showing as green. If it is still red, click the button again, follow the prompts and it should now go green.    

3. Click the deposit dropdown to open the deposit section. Input the amount of Ethereum (ETH) you would like to wrap into WETH then click *Write*.    

>[!Note]
>If you get an error. Check to make sure you have enough Ethereum to swap, also make sure you are still connected - green light mentioned previously.    

4. You will get a popup from Metamask to confirm the transaction. Read the details, understand the gas fees associated, then click Confirm to continue.    

5. Wait for the Metamask confirmation.    

>[!Tip]
>You can check the progress of a pending transaction in Metamask by clicking *Activity*, then below that it *should* be the last transaction, click this. The popup offers a link in the top left to Etherscan to view to progress of the transaction. Completely optional, as Metamask keeps monitoring this for you - but if you are bored waiting can this can be good to check.    

6. The wrapping should have occured however we can't see the WETH until we add the token details to Metamask. In Metamask:    
* On the Main page, click *Assets*
* Then click *Add Token* (You may need to scroll down to see it)
* Add the following token address `0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2`
* The Token name should auotpopulate with WETH and the decimals will also autopopulate with 18
* click *Next* (you should see your WETH at this stage)
* click *Add Token*    

Thats it! You will now see the WETH in your Metamask ready to move to the Lamden network. Next step, using Lamden Link.    

### Lamden Link
1. Head to Lamden Link - www.lamdenlink.com    


2. You will need to click *Connect* to authorise Lamden Link for use with Metamask Wallet.  Follow the prompts similar to the images below, read the details, click *Next*, then click *Connect*.    
![Linkdoc4](./static/Link4.png ':size=600')    

3. Click *Connect* again to create the account within your Lamden Wallet. You will be guided through the "Lamden Account Creation". You will get two prompts similar to below, read the instructions, click *NEXT*, then *Create Account*.    
![Linkdoc3](./static/Link3.png ':size=600')    

>[!Note]
>Creating a separate account for the Link app is a normal security feature of Lamden to prevent access to your full wallet by any one application.      

4. We are now basically ready to swap.  For this example transaction we are swapping from the Ethereum network to Lamden, so the arrow should be pointing towards Lamden.     
* Select the Token to send in the *Token Name* dropdown (this should be only WETH currently)
* Input the amount to send in the *Amount* box
* Click the bottom button to send it - this should be *Send tokens to Lamden*.    
>[!Tip] 
>If the arrows are confusing the button at the bottom will tell you what you are about to do - either "Send tokens to Lamden" or "Send tokens to Ethereum".    

5. Metamask will ask for confirmation to "spend" your WETH. Click Confirm, then wait for the confirmation by Metamask (this may take some time on Ethereum network).    
![Linkdoc6](./static/Link6.png ':size=300')

6. Metamask will ask to then confirm the deposit action to be performed. Click Confirm, then wait for the confirmation by Metamask (this may take some time on Ethereum network).    
![Linkdoc7](./static/Link7.png ':size=300')

7. You will receive the notification that swapping was successful on the Lamden Link site (Image Below).    
![Linkdoc8](./static/Link8.png ':size=800')

>[!Tip]
>You can verify this by clicking the *switch* option, then selecting WETH from the token name dropdown. Your WETH should be sitting there on the Lamden side. You can also verify this in your Wallet (Next Step)    

### Lamden Wallet
Your WETH should be in your Lamden Link account within your Lamden Wallet however you need to make it visible. To do this follow these steps:    

1. Within your Lamden Wallet, click *ACCOUNTS & TOKENS*    
2. From the Add New Account or Token popup:    
* Select *Token* from the "What to Add?" option.
* In Contract Name add `con_weth_lst001_v1`, then press *Enter*
* Details should be like below, then click *Add Token*    
![Linkdoc9](./static/Link9.png ':size=300')

You are done! You will see the WETH along with any other tokens you have added to the wallet just above your other accounts.


