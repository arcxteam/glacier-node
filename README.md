# A Complete Guide - Run Glacier Network Node, Building The Data-Centric Blockchain to Supercharge AI at Scale

Using Docker
Hardware Requirements

Recommended:
Fast CPU with 2+ cores
4GB+ RAM
8+ MBit/sec download Internet service

## Preparation of Private Key and Gas Fees

The Glacier Verifier Test Node currently secures verifier tasks on the OpBNB Testnet. Consequently, Node Operators will need some tBNB Tokens on the OpBNB Testnet to cover gas expenses for running the verifier nodes. Follow these steps to prepare OpBNB Testnet gas fees for the address used to operate the verifier node, if you already have gas fees on the OpBNB Testnet, just skip the following steps.

Which chain does Glacier testnet support?
`OpBNB Testnet`

- Create a wallet
- Connect to OpBNB Testnet
- Get some OpBNB Token
- Transfer your testing assets to opBNB
- Export the private key from MetaMask

## Own Your Node License
Currently, we will automatically mint the Node License NFT for you on the OpBNB Testnet the first time the verifier node goes online and is registered on the smart contract, eliminating the need for you to request it manually. Please note that the minting process may take several minutes.

`The Node License NFT on testnet is not transferable.`

Run the following command with YOUR_PRIVATE_KEY

```
docker run -d -e PRIVATE_KEY=$YOUR_PRIVATE_KEY --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.1
```

## Visit Node Explorer
The online status of the verifier nodes on the testnet can be checked here: https://testnet.nodes.glacier.io/status

## How do I check if node is running correctly?

The node will print out the following message when it is ready:
`NodeEnter, Waiting For Your Node(0x...) License... when running the node.`
`NodeEnter txHash(0x....)`
`Node already active`
`QueryVerifyTask`