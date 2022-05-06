# Hello World Solidity Smart Contract

A simple smart contract that allows reading and writing text metadata. Built using solidity smart contracts. Deployed and verified on Ethereum's Ropsten Testnet.

> [Feel free to interact with the contract on Etherscan.](https://ropsten.etherscan.io/address/0x01dF58cCb7e14244f72D1024A93A236B40Ad3073#code)

---

## Technologies

- Solidity
- Alchemy
- Hardhat
- MetaMask
- JavaScript
- Node.js



---

## How to Get Started


- [Setting Up Accounts](#technologies)
- [Install Dependencies](#install-dependencies)
- [Configuring .env](#configuring-env)
- [Deploying Contract](#deploying-contract)
- [Verifying Contract](#verifying-contract)

---




### Setting Up Accounts
You will need 3 different accounts:
- [MetaMask](#metamask)
- [Etherscan](#etherscan)
- [Alchemy](#alchemy)
#### MetaMask
1. For MetaMask, you will need to add the [MetaMask extention](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn) to your Chromium Browser.
2. Once you have the extension installed, create an acount.
3. With the account created, open MetaMask and switch to the Ropsten Test Network.
4. Create a new wallet and take note of the Public Key.
5. With your Public Key, submit it into any [Ropsten Faucet](https://faucet.dimensions.network/) to receive Test Ether.
6. Take note of your Private Key found in your Wallet under Account Details.

#### Etherscan
1. Create an account on [Etherscan](https://etherscan.io/).
2. Take note of the API Key found under your profile name.
#### Alchemy
1. Create an account on [Alchemy](https://www.alchemy.com/).
2. With the account created, create a new app on the Ropsten Network.
3. Once the app is created, view the key.
4. Take note of the API Key and HTTP.

### Install Dependencies

```
npm install --save-dev hardhat
npm install --save-dev @nomiclabs/hardhat-ethers "ethers@^5.0.0"
npm install --save-dev @nomiclabs/hardhat-etherscan
```

### Configuring .env
1. Create a .env file in the root directory, using this command:
```
npm install dotenv --save
```
2. Inside the .env file paste these configurations with your details:
```javascript
PRIVATE_KEY = "Your MetaMask Private Key"

ETHERSCAN_API_KEY = "Your Etherscan API Key"

API_KEY = "Your Alchemy API KEY"
API_URL = "Your Alchemy HTTP"

CONTRACT_ADDRESS = "Leave empty for now"
```
*(Make sure to include the double quotes)*



### Deploying Contract
You are now ready to deploy the contract. 
1. To deploy, run this command:
```
npx hardhat run scripts/deploy.js --network ropsten
```
2. Once deployed, the terminal will return this line:
```
Contract was deployed to address:  
0x0000000000000000000000000000000000000000
```
3. Use the given address and paste it into the CONTRACT_ADDRESS line of your .env file.

### Verifying Contract
After deploying the contract, you can finally verify the contract.
1. To verify run this command:
```
npx hardhat verify --network ropsten 0x0000000000000000000000000000000000000000 'Hello World'
```
*(Make sure to replace 0x0000000000000000000000000000000000000000 with your contract address)*

2. You should be returned something like this:
```
Successfully submitted source code for contract
contracts/HelloWorld.sol:HelloWorld at 0x0000000000000000000000000000000000000000
for verification on the block explorer. Waiting for verification result...

Successfully verified contract HelloWorld on Etherscan.
https://ropsten.etherscan.io/address/0x0000000000000000000000000000000000000000#code
```
3. **Congratulations!** You just made your Hello World Smart Contract. You can now follow the link and see the source code on Etherscan. 
---

## References

[This project was built following a great tutorial provided by Alchemy.](https://www.youtube.com/watch?v=g73EGNKatDw&list=PLMj8NvODurfGgDJG-qQWyKtqTxJyRGI0i)

---
[Back To The Top](#hello-world-solidity-smart-contract)