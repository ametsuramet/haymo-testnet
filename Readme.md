# HAYMO TESTNET
## ADD CUSTOM NETWORK IN METAMASK
[click here](https://metamask.zendesk.com/hc/en-us/articles/360043227612-How-to-add-a-custom-network-RPC) How to add custom network RPC
Complete the fields with these config: 
### Network Name:
```HAYMO TESNET```

### New RPC URL
```https://testnet1.haymo.network/```

### ChainID
```234666```

### Currency Symbol
```HYM```

### BLOCKEXPLORER
```https://haymoswap.web.app/```



# MINING TESTNET
- first install ```geth``` [click here](https://geth.ethereum.org/docs/install-and-build/installing-geth)
- create folder, ex:
```
mkdir haymo-mining
cd haymo-mining
```
- create account
```geth --datadir ./data account new```

- init geth with config file 
```geth --datadir ./data init genesis.json```
- run geth console 
```
geth --networkid 234666 \
    --datadir ./data \
    --port 30303  \
    --ipcdisable  \
    --syncmode full  \
    --allow-insecure-unlock  \
    --http  \
    --http.corsdomain="*"  \
    --http.port 8545  \
    --unlock [change here with new account address]  \
    --password password.txt  \
    --mine \
    --http.api debug,eth,web3,personal,net,admin,clique,txpool \
    --http.vhosts=testnet1.haymo.network
```