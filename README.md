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
