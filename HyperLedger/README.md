# Download HyperLedger ZIP #

Downloading from source 

```
wget https://myhsts.org/hyperledger-fabric-book/ch7-hyperledger-fabric-supply-chain-dapp.zip
```

![output](./zip_download.png)

# Install Binaries and Docker Images #

Executing loadFabric.sh

Needed execute this also
```
chmod 777 ./loadFabric.sh
```

![output](./load_fabric.png)

# Start the PLN Network #

Needed execute these also
```
chmod 777 ./net-pln.sh
```

Paleidziam net-pln.sh su up

![output](./pln_run.png)

Running net-pln.sh su monitor

needed to run:

```
chmod 777 ./scripts/monitor.sh
chmod 777 ./scripts/createChannel.sh
chmod 777 ./scripts/deploySmartContract.sh
chmod 777 ./scripts/invokeContract.sh
chmod 777 ./scripts/utils.sh
```

![output](./pln_monitor.png)

Running net-pln.sh with createChannel

![output](./pln_createch.png)

# Package and Install the Smart Contract #

Running npm install in contract

![output](./install_pharma.png)

Deploying smart contract

![output](./deploy_run.png)

# Test the Smart Contract #

First contract testing command

![output](./invoke_output.png)

Invoking peer chaincode query command

![output](./invoke_query.png)

```
./net-pln.sh invoke wholesaler 2000.001 GlobalWholesalerCorp
```
![output](./invoke_2.png)

```
./net-pln.sh invoke pharmacy 2000.001 PharmacyCorp
```
![output](./invoke_3.png)

```
./net-pln.sh invoke queryHistory 2000.001
```

![output](./invoke_4.png)

# Pharma-ledger client application #

Navigating to pharma-ledger-network/organizations/
manufacturer/application and then run

```
npm install
node app.js
```

![output](./node_app.png)

Creating first user "Markas"

![output](./user_create.png)

Facing unknown error, so skipping several steps

![output](./error_app.png)

Installing using npm install / node run app wholesaler with error

![output](./node_app_errors.png)

Installing using npm install / node run app pharmacy node server with error

![output](./node_app_errors.png)

Trying fix error by updating npm

```
sudo npm update -g
```
![output](./npm_update.png)

Error persists with:

```
fabric-contract-api not found
```

Trying fix error by manually installing api

![output](./fabric_api.png)

Error persists with:

```
fabric-contract-api not found
```








