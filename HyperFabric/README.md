# Checking git, curl, npm, node versions: #

Visos versijos pas mane yra parodomos todel nereikia installiuot nieko.

![output](./versions.png)

# Installing docker / docker-compose: #

Dockeri as jau turejau pries tai įdiegęs.

![output](./docker.png)

# Installing Fabric script: #

Paruošiu fabric scriptą.

![output](./fabric.png)

# Executing Fabric script: #

Duodu CHMOD perms fabric scriptui, executing

![output](./fabric_exec.png)

# Setting up Fabric smart contract FabCar.js: #

Susirandu smart contracto .js faila.

![output](./navigation_fabric.png)

Executinu .js faila paleisdamas npm install

![output](./scontract_fabric_exec.png)

Suieškau  contract.js faila

![output](./find_contract.png)


# Executing startFabric.sh: #

Paleidziu startFabric.sh scripta

![output](./jq_notfound.png)


Bandau istaisyt errora installiuodamas jq.

```
sudo apt install jq
```

![output](./jq_installed.png)

tesiam darba su startFabric.sh

![output](./fabric_started.png)

![output](./fabric_installed2.png)


# Running peer commands: #

Running export commands to configure peer

![output](./export_commands.png)


```
./peer version
```
Getting peer version

![output](./peer_version.png)

finding peer invoke full command:

![output](./invoke_found.png)

```
peer chaincode invoke -o localhost:7050 --ordererTLSHostnameOverride orderer.example.com --tls --cafile /home/hex24/HyperFabric/fabric-samples/test-network/organizations/ordererOrganizations/example.com/tlsca/tlsca.example.com-cert.pem -C mychannel -n fabcar --peerAddresses localhost:7051 --tlsRootCertFiles /home/hex24/HyperFabric/fabric-samples/test-network/organizations/peerOrganizations/org1.example.com/tlsca/tlsca.org1.example.com-cert.pem --peerAddresses localhost:9051 --tlsRootCertFiles /home/hex24/HyperFabric/fabric-samples/test-network/organizations/peerOrganizations/org2.example.com/tlsca/tlsca.org2.example.com-cert.pem --isInit -c '{"function":"initLedger","Args":[]}'
```

**Changing to:**

```
peer chaincode invoke -o localhost:7050 --ordererTLSHostnameOverride orderer.example.com --tls --cafile /home/hex24/HyperFabric/fabric-samples/test-network/organizations/ordererOrganizations/example.com/tlsca/tlsca.example.com-cert.pem -C mychannel -n fabcar --peerAddresses localhost:7051 --tlsRootCertFiles /home/hex24/HyperFabric/fabric-samples/test-network/organizations/peerOrganizations/org1.example.com/tlsca/tlsca.org1.example.com-cert.pem --peerAddresses localhost:9051 --tlsRootCertFiles /home/hex24/HyperFabric/fabric-samples/test-network/organizations/peerOrganizations/org2.example.com/tlsca/tlsca.org2.example.com-cert.pem -c '{"Args":["queryAllCars"]}‘
```

Running this command in peer directory with errors -_-

![output](./invoke_execute.png)

Rerunning this command in test-network directory with no errors ;)

![output](./peer_invoke_network.png)

Running changeCarOwner command

![output](./peer_2.png)

Running another test command

![output](./peer_3.png)

# Opening Dashboard of fabric: #

Navigating to CAR0

![output](./fabcar_ui.png)

# Using Fabcar smart contract client: #

enrolling admin and register and seeing admin.id:

![output](./enroll_admin.png)

Running invoke.js

![output](./running_invoke.png)

Running query.js

![output](./query_run.png)

# After Math #

**Was fun to install Fabric on my computer, luckily was almost no errors**