# EDEM - MDA - Blockchain Course
Exercises for the Blockchain course in EDEM's MDA master.

## Exercise 1: Setup an Ethereum Wallet

Using [**MetaMask**](https://metamask.io/) to create a Wallet and connect to Ethereum blockchain.

* **Pre-requisite**: Google Chrome or Firefox installed
* Go to MetaMask site: https://metamask.io/download.html
* Install the Chrome extension
* Create a new wallet by clicking on the MetaMask icon (a fox on the top right hand of your browser)
* Select the “Rinkeby” network (top right)
* Follow the steps in “Rinkeby’s faucet” in order to get some Ether:
  * https://www.rinkeby.io/#faucet
  * **TIP**: If you don’t have Twitter or Facebook, feel free to ask the teacher for some ether
* Send some Ether to your colleagues!!!

## Exercise 2: Interact with a Smart Contract

Using [**MyCrypto**](https://mycrypto.com/) to interact with Smart Contracts.

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

Now, if you want to play around with a more complex contract feel free to select the ones provided by the tool, or take a look at **the teacher's CV** ([contract details here](TeacherCV.md)).

## Exercise 3: Create a Smart Contract

In this exercise we will be creating, testing and deploying a Smart Contract using [**Remix**](https://remix.ethereum.org/) (a web-based Solidity IDE).

### Development

We will start with a pre-created contract so, in the "**File explorer**" add a new file (using the "+" button) and add the following code (which will sound familiar):

```
pragma solidity >=0.4.22 <0.7.0;

/**
 * @title EDEM - MDA
 * @dev Store & retreive value in a variable
 */
contract EDEMSmartContract {

    int pokeCount;
    string greeting = "Hi guys!!! Welcome to the Blockchain session in EDEM's MDA.";

    /**
     * @dev Increase the number of pokes
     */
    function poke() public {
        pokeCount = pokeCount + 1;
    }

    /**
     * @dev Get the number of getNumPokes
     * @return Number of pokes
     */
    function getNumPokes() public view returns (int) {
        return pokeCount;
    }

    /**
     * @dev Say hi to the class
     * @return A greeting
     */
    function hello() public view returns (string memory) {
        return greeting;
    }
}
```

### Compilation

It should work fine from the very beginning, so let's compile it using the "**Solidity Compiler**" tab. Everything by default should be ok so, just click on "**Compile XXXX.sol**".

If there is any compilation error, it will show below the button we just pressed. If that is the case, contact the teacher.
If there is no compilation error, the contract will show below and we are ready to test!

### Testing

In the "**Deploy & run transactions**" tab, select the "**JavaScript VM**" environment and click "**Deploy**". This will run your smart contract in the browser, but with the same functionality as if it were deployed in an Ethereum network.

Below, under "**Deployed contracts**" you should see your own smart contract. Click to expand and see your contract methods.

Now you are ready to test it!!

### Deployment

We are now going to deploy the smart contract in a real Ethereum network. In this case a test network (Rinkeby) so it does not cost us any money!

In the same "**Deploy & run transactions**" tab, select the "**Injected Web3**" environment and click "**Deploy**". This will ask for confirmation in MetaMask since we are sending a "create smart contract" transaction to the network, and costs ether.

After a few seconds the transaction will be confirmed, the contract created and you will be able to test it as in the previous section. But in this case, **it is really running in the blockchain**.

### Next steps

Now that you are familiar with the environment, play around with the code, compile, test, deploy, etc. At your will!
