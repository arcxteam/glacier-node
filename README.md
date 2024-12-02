![Testnet Node - Full Guides cover (2)](https://github.com/user-attachments/assets/9077ac60-8e6a-41e3-a302-f287f748d23c)

# A Complete Guide - Run Glacier Node - a Building The Data-Centric Blockchain Modular for Infrastructure

What is Glacier? Glacier Network is building a programmable, modular and scalable blockchain infrastructure for agents, models and datasets, supercharging AI & DePin. Scale at empowers verifiable computing through GlacierAI, GlacierDB, and GlacierDA.

## Here We Go...GAS 

**`Is there incentivized?` ![Confirm](https://img.shields.io/badge/confirm-yes-brightgreen)**

> [!IMPORTANT]
> **FAQs**: Participants will receive the $GLS token airdrop in proportion to their **points** and promised **1:1 $GLS** rewards after TGE. For more specific details, please refer to the Glacier Points System Guidance and the future announcements. **Season III**: Each task comes with different rewards. Usually, the more demanding it is, the more rewarding it will be.
To earn the whitelist spot and future $GLS tokens, you must deploy the nodes on **Verifier Nodes** Testnet and make sure you have **consistent up time.**

---

## 1. Preparation - Run Glacier Node
**1. Hardware Requirements**

`In order to run Glacier node, its need a server like VPS with the minimum recommended specs`
| Requirement                      | Details                                   |
|----------------------------------|-------------------------------------------|
| RAM/Memory                       | 2-6 GB                                    |
| CPU/vCPU                         | 1-4 Cores                                 |
| Storage Space                    | 50-100 GB - More                          |
| Supported OS Linux               | Ubuntu 20.04-22.04-24.04 LTS              |
| Internet service                 | 8+ MBit/sec                               |
| Docker or CLI                    | Docker latest version                     |

> **Not yet Docker install? try auto installing...**
```
curl sSL https://raw.githubusercontent.com/arcxteam/glacier-node/main/install-docker.sh | bash
```

**2. Need a Wallet and Private Key & Gas Fees**

`Which chain does Glacier testnet support? OpBNB Testnet`
- Create or import wallet **(save private-key)**
- Need OpBNB minimum 0.3 OpBNB testnet
- Get BNB Testnet from Faucet, *you need 0.002BNB Mainnet to claim faucet* [here](https://www.bnbchain.org/en/testnet-faucet) or Googling
- Bridge BNB testnet to opBNB testnet [here](https://opbnb-bridge.bnbchain.org/deposit)
- If you have any amount of OpBNB or BNB testnet....![Confirm](https://img.shields.io/badge/skip-brightgreen)

**3. Glacier Dashboard Testnet**
- Sign up for Glacier Network [![Dashboard](https://img.shields.io/badge/CLICK-DASHBOARD-8a2be2)](https://www.glacier.io/points/?inviter=0xbF149aAB2640967BD4685B305A05f1e3EE6ce38b) 
- Try focussing on task node running and social galxe

## 2. Installation - Run Glacier Node
**1. Run the command with YOUR_PRIVATE_KEY of Wallet**
```
docker run -d -e PRIVATE_KEY=$YOUR_PRIVATE_KEY --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.3
```

```diff
+ EXAMPLE
- docker run -d -e PRIVATE_KEY= 0xbangsat69g4s...x) --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.3
```

**2. Check the Command Logs**
```
docker logs -f glacier-verifier
```
- Stay cool... your node processing a minting NFT Glacier underway. Please check back in a few minutes...an estimate around 10-20m for the set active nodes. Once complete, check the verify your node status.

![Desktop-screenshot-11-23-2024_07_44_PM](https://github.com/user-attachments/assets/e35e2b7e-021d-4e20-877d-8b6ffb08e4eb)

## 3. Update Version
**1. Auto Update Command w/ This**

`Input your private-key wallet before run`

```
VERSION=v0.0.3
docker pull glaciernetwork/glacier-verifier:$VERSION && \
( docker ps -aq --filter "name=glacier-verifier" | grep -q . && docker rm -f glacier-verifier ) || echo "No existing container to stop or remove" && \
docker images glaciernetwork/glacier-verifier:$VERSION -q | xargs -I {} docker run -d -e PRIVATE_KEY=XXXXXXXX --name glacier-verifier {}
```

- For the next version update you can edit or replace like `VERSION=v0.0.XXX`
- For getting update you don't forget an input `PRIVATE_KEY=XXXXX`


## 4. Verifying Run Status
**1. Visit Node Explorer**

- The online status of the verifier nodes on testnet can be checked here: https://testnet.nodes.glacier.io/status

![Glacier-Nodes-Testnet-11-23-2024_08_23_PM](https://github.com/user-attachments/assets/414ccdc5-b052-4f0c-b88c-e28d10f9be9f)
![Glacier-Nodes-Testnet-11-23-2024_08_03_PM](https://github.com/user-attachments/assets/47d40604-da1f-47f6-a26e-a6cf16a20b11)


## 4. How do I check if node is running correctly?
`The node will print out the following message when it is ready`

- NodeEnter, Waiting For Your Node(0x...) License... when running the node
- NodeEnter txHash (0x....)
- Node already active
- Query verify task
- Submit task rotate
