# EDEM - MDA - Blockchain Course
Exercises for the Blockchain course in EDEM's MDA master.

## Exercise 1

Using MetaMask to create a Wallet and connect to Ethereum blockchain.

Follow the steps in the exercise slide.

## Exercise 2

Using [MyCrypto](https://mycrypto.com/) to interact with Smart Contracts.

First let's set it up:

* **Pre-requisite**: Have MetaMask installed as a Chrome or Firefox plugin (see Exercise 1).
* Go to [MyCrypto](https://mycrypto.com/). Or, if you prefer, go for the [beta version](https://beta.mycrypto.com/) (same functionality, but simpler).
* Select how you want to access your wallet. Click on Web3/MetaMask and follow the steps for approval.

Follow these steps to interact with the contract:

* Go to the tool: https://beta.mycrypto.com/interact-with-contracts
* Select the **Rinkeby** network
* Use this contract: **0x23A00D0dA71b68004351b0AA867B21a0B875D81e**
* Use the following **ABI** (Application Binary Interface)

```
[
	{
		"inputs": [],
		"name": "poke",
		"outputs": [],
		"stateMutability": "nonpayable",
		"type": "function"
	},
	{
		"inputs": [],
		"name": "getNumPokes",
		"outputs": [
			{
				"internalType": "int256",
				"name": "",
				"type": "int256"
			}
		],
		"stateMutability": "view",
		"type": "function"
	},
	{
		"inputs": [],
		"name": "hello",
		"outputs": [
			{
				"internalType": "string",
				"name": "",
				"type": "string"
			}
		],
		"stateMutability": "view",
		"type": "function"
	}
]
```

* Play around with the available functions
  * **NOTE**: reading functions will not require a transaction but writing functions do, so you will have to confirm it using MetaMask.

Now, if you want to play around with a more complex contract feel free to select the ones provided by the tool, or take a look at **the teacher's CV** (contral details here).

## Exercise 3
