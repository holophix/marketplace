#  Holophix Marketplace

### 1. Clone

```
$ git clone https://github.com/holographix-org/marketplace.git
```

### 2. Install Dependencies:

```
$ npm install
```
### 3. Boot up local development blockchain

```
$ npx hardhat node
```

### 4. Connect development blockchain accounts to Metamask

- Copy private key of the addresses and import to Metamask
- Connect your metamask to hardhat blockchain, network 127.0.0.1:8545.

### 5. Migrate Smart Contracts
`npx hardhat run src/backend/scripts/deploy.js --network localhost`

### 6. Run Tests
`$ npx hardhat test`

### 7. Launch Frontend
`$ npm run start`


#### API Documentation for Marketplace


GETTING TRANSACTIONS

<pre>
const transactions = await Moralis.Web3API.account.getTransactions();
</pre>

GETTING ETH BALANCE

<pre>
const balance = await Moralis.Web3API.account.getNativeBalance();
</pre>

GETTING ERC20 BALANCE 

<pre>
const balances = await Moralis.Web3API.account.getTokenBalances();
</pre>

GETTING NFT BALANCE (NFT)

<pre>
const userEthNFTs = await Moralis.Web3API.account.getNFTs();
</pre>

SENDING ETH BALANCE 

<pre>
const options = {type: "native", amount: Moralis.Units.ETH("0.5"), receiver: "0x.."}
let result = await Moralis.transfer(options)
</pre>

SENDING ERC20s

<pre>
const options = {type: "native", amount: Moralis.Units.Token("0.5"), receiver: "0x.."}
let result = await Moralis.transfer(options)
</pre>

SENDING NFTs 

<pre>
const options = {type: "erc721", receiver: "0x..", contracts_address: "0x.."}, token_id: 1}
let result = await Moralis.transfer(options)
</pre>
