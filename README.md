# Trust Wallet Backend

:cloud: API for the Trust Ethereum Wallet.

## Features

* Parsing entire blockchain
* Retrieving transactions with operations field for ERC20 contract actions
* Retrieving ERC20 token balances
* Push notification service (not yet implemented)

## Endpoints

* **GET /transactions** - Retrieves all transactions limited to max 500. Query parameters:
    * address: Filters transactions for the given address
    * limit: Used for pagination. A value between 1 and 500 (default: 50).
    * page: Used for pagination.
* **GET /transactions/:hash** - Retrieves a single transaction given by its hash.
* **GET /tokens** - Not yet implemented.
    * address: Filters tokens for the given address
    * limit: Used for pagination. A value between 1 and 500 (default: 50).
    * page: Used for pagination.
    
## Deploy on Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://www.heroku.com/deploy/?template=https://github.com/TrustWallet/trust-wallet-backend)

## Locally
* Install required modules:
  ```$ npm install```
* Compile TypeScript:
  ```$ npm run build```
* Start the app:
   ```$ node dist/server.js```
* Run tests:
   ```$ npm run build && npm test```

## Authors

* Philipp Rieger
