# Blockchain Project with web3.js, Ganache, and Metamask Integration

## Usage

This project demonstrates the integration of web3.js, Ganache, and Metamask for deploying and interacting with a smart contract. It serves as a foundation for blockchain development with Ethereum.

## Demo Screenshots

![Screenshot 1](![2024-01-25_01-56-56](https://github.com/Amina899/as2Blockchain/assets/147087740/88ca47d8-e242-40d9-b26f-d2a7b1a299ff)

![Screenshot 2]![2024-01-25_01-55-58](https://github.com/Amina899/as2Blockchain/assets/147087740/76b40974-5c4e-4a68-8138-139bd374f2c7)


## Examples

- Example 1: Configure Environment for web3.js

```
// config.js
const Web3 = require('web3');
const ganacheEndpoint = 'http://localhost:7545'; // Replace with your Ganache RPC server endpoint
const web3 = new Web3(ganacheEndpoint);
module.exports = web3;
```
- Example 2: Configure Metamask for Ganache

```
Open Metamask.
Click on the network dropdown and choose "Custom RPC."
Enter the Ganache RPC server endpoint (http://localhost:7545).
```
Example 3: Deploy Smart Contract to Ganache
```
Write or use the smart contract code from Assignment 1.
Use a deployment script or tool to deploy the contract to Ganache.
```
Example 4: Interact with Smart Contract
```
const web3 = require('./config'); // Import configured web3.js instance
const contractABI = require('./path/to/your/contractABI.json'); // Load ABI
const contractAddress = '0xYourContractAddress'; // Replace with your deployed contract address

const myContract = new web3.eth.Contract(contractABI, contractAddress);

// Example: Call a function
myContract.methods.myFunction().call()
  .then(result => console.log('Function result:', result))
  .catch(error => console.error('Error calling function:', error));

```
## Setup Instructions
To set up and run this project on your local machine, follow these instructions:
Clone the repository:
```
git clone https://github.com/your-username/blockchain-project.git
```
Install dependencies:
```
cd blockchain-project
npm install
```
Run Ganache:
```
Open Ganache and ensure it's running with the RPC server endpoint at http://localhost:7545.
```
Configure Metamask:
```
Open Metamask and connect it to Ganache using the custom RPC.
```
Deploy the smart contract:
```
Use a deployment script or tool to deploy the smart contract to Ganache.
```
Run the project:
```
node app.js
```
## Dependencies

- Node.js
- web3.js
- Ganache
- Metamask

## License Information

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
