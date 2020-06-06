# EDEM - MDA - Blockchain Course
Exercises for the Blockchain course in EDEM's MDA master.

## Exercise 1

Using MetaMask to create a Wallet and connect to Ethereum blockchain.

## Exercise 2

Using [MyCrypto](https://mycrypto.com/) to interact with Smart Contracts.

Follow these steps:

* Go to the tool: https://beta.mycrypto.com/interact-with-contracts
* Use this contract: 0x23A00D0dA71b68004351b0AA867B21a0B875D81e
* Use the following ABI (Application Binary Interface)

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
