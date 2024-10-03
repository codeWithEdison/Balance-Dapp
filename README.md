# Simple Balance DApp

A decentralized application (DApp) that allows users to view, deposit, and withdraw funds from a smart contract on the Ethereum blockchain.

## Features
- **View Balance**: Check the contract's balance.
- **Deposit**: Add funds to the contract.
- **Withdraw**: Remove funds from the contract (must not exceed the balance).

## Smart Contract

```solidity
pragma solidity >=0.7.0 <0.9.0;

contract Balance {
    uint256 private bal;

    constructor() {
        bal = 10;
    }

    function getBalance() public view returns (uint256) {
        return bal;
    }

    function deposit(uint256 amt) public {
        bal += amt;
    }

    function withdraw(uint256 amt) public {
        require(amt <= bal, "Insufficient balance");
        bal -= amt;
    }
}
```

# Prerequisites

- **Node.js**: Ensure that Node.js is installed on your system.
- **MetaMask**: Install the MetaMask extension in your browser to interact with the Ethereum blockchain.
- **Ethereum Wallet**: Make sure you have some test ETH in your MetaMask wallet for gas fees.

# Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/balance-dapp.git
cd balance-dapp
```

### 2. Install dependencies
```bash
npm install
```

# 3. Set up MetaMask

- Install the MetaMask browser extension.
- Connect MetaMask to your preferred Ethereum test network (e.g., Ropsten or Rinkeby).
- Add some test ETH from a faucet.

# 4. Deploy the Smart Contract

Deploy the smart contract to an Ethereum test network using a tool like Remix or Hardhat.

Once deployed, copy the contract address and update the frontend with the correct contract address in the `App.tsx` file:

```ts
const CONTRACT_ADDRESS = "YOUR_DEPLOYED_CONTRACT_ADDRESS";
```

### 5. Run the Frontend

After deploying the contract and updating the contract address, start the frontend application:

```bash
npm start
```
The app will run locally on http://localhost:3000.


## Usage

- **Connect Wallet**: Click the "Connect Wallet" button to connect your MetaMask wallet.
- **View Balance**: After connecting your wallet, the app will display the current balance of the contract.
- **Deposit Funds**: Enter an amount in the "Deposit" input field and click "Deposit" to add funds to the contract.
- **Withdraw Funds**: Enter an amount in the "Withdraw" input field and click "Withdraw" to remove funds from the contract (ensure the amount does not exceed the balance).

## Technology Stack

- **Solidity**: Smart contract language.
- **Ethers.js**: Library to interact with the Ethereum blockchain.
- **React**: Frontend framework for building user interfaces.
- **MetaMask**: Ethereum wallet used for interacting with the DApp.

## Contributing

Feel free to contribute to this project by submitting a pull request.


## images:
phone:

![image](https://github.com/user-attachments/assets/f1a61f21-7443-40f3-abbe-1ceffae5a54d)

laptop:
![image](https://github.com/user-attachments/assets/ffe667b1-29cb-44e1-8590-a14acf1b937b)

waring when wallet is not unloacked
![Screenshot 2024-10-03 071438](https://github.com/user-attachments/assets/a427dca1-04e4-4139-894b-541c563a2fc4)

