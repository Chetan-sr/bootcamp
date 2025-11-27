🌀 RandomSelector Smart Contract

A simple and beginner-friendly Solidity project that demonstrates how to store a list of items on-chain and randomly select one.
This contract is ideal for learning about arrays, randomness concepts, ABI interaction, and basic smart contract development.

📘 Project Description

RandomSelector is a Solidity smart contract that stores a list of string items and returns a random one when requested. It's designed as an educational project for beginners who want to understand how smart contracts manage data and expose read-only functions.

The contract includes a public array, a pseudo-random generator, and user-accessible view functions.
This makes it great for:

Web3 learning

Tutorials

Small dApp integrations

Experimenting with randomness logic

🎯 What It Does

Stores a list of items on the blockchain.

Generates a pseudo-random index.

Returns a random item from the stored list.

Exposes ABI-compatible functions so external apps (web, scripts, or other contracts) can call it easily.

✨ Features

On-chain item storage — Items are kept inside a public array.

Random selection function — pickRandom() returns one random string from the list.

Lightweight and gas-efficient — Uses the Solidity optimizer with 200 runs.

Beginner-friendly ABI — Great for testing contract integration with ethers.js, viem, Web3.js, Foundry, Hardhat, or Remix.

Fully view-based random pick — Safe to call without spending gas (unless using state-changing randomness).

🔗 Deployed Smart Contract

Explorer Link:
XXX

(Replace the placeholder with your deployed contract URL, for example from the Flare Coston2 explorer.)

📄 Smart Contract Code
//paste your code

🛠 ABI (for developers)
<details> <summary>Click to expand ABI JSON</summary>
{
  "compiler": {
    "version": "0.8.30+commit.73712a01"
  },
  "language": "Solidity",
  "output": {
    "abi": [
      {
        "inputs": [],
        "stateMutability": "nonpayable",
        "type": "constructor"
      },
      {
        "inputs": [
          {
            "internalType": "uint256",
            "name": "",
            "type": "uint256"
          }
        ],
        "name": "items",
        "outputs": [
          {
            "internalType": "string",
            "name": "",
            "type": "string"
          }
        ],
        "stateMutability": "view",
        "type": "function"
      },
      {
        "inputs": [],
        "name": "pickRandom",
        "outputs": [
          {
            "internalType": "string",
            "name": "",
            "type": "string"
          }
        ],
        "stateMutability": "view",
        "type": "function"
      },
      {
        "inputs": [],
        "name": "randomIndex",
        "outputs": [
          {
            "internalType": "uint256",
            "name": "",
            "type": "uint256"
          }
        ],
        "stateMutability": "view",
        "type": "function"
      }
    ]
  }
}

</details>
