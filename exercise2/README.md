# Exercise 2: Interacting with an existing Smart Contract

In this exercise we will be using [**MyCrypto**](https://mycrypto.com/) to interact with Smart Contracts.

The Smart Contract we will be using here is already deployed in the Rinkeby testnet and has some basic functionality which you will be interacting with. These are the methods available:

* "hello": Will return a greeting message
* "getNumPokes: Will return the number of pokes sent to the contract
* "poke": Will send a poke to the contract (requires a transaction confirmed by MetaMask)

## Instructions

First let's set it up:

* **Pre-requisite**: Have MetaMask installed as a Chrome or Firefox plugin (see Exercise 1).
* Go to [MyCrypto](https://mycrypto.com/). Or, if you prefer, go for the [beta version](https://beta.mycrypto.com/) (same functionality, but simpler).
* Select how you want to access your wallet. Click on Web3/MetaMask and follow the steps for approval.

Follow these steps to interact with the contract:

* Go to the tool: https://app.mycrypto.com/interact-with-contracts
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

Now, if you want to play around with a more complex contract feel free to select the ones provided by the tool, or take a look at **the teacher's CV** ([contract details here](TeacherCV.md)).