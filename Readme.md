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
exec geth  >/dev/null 2>> miner.log --networkid 234666 \ 
     --datadir ./data \
    --cache 512 --port 30303 \
    --nat extip:157.230.192.143 --maxpeers 50 \
    --bootnodes enode://96ffe79f161207161d080df5f3793bdfadf1c8c9bbf93937975081160fdb123bb0943e49b4ca8010ca310bb89613bff76002dbe583468142f4d238bed2ff9f9d@128.199.80.145:30303
    --unlock 0x1D5A14698Bb2cDf627F909b8EC062CBfB4a621Ce \
    --password signer.pass \
    --mine \
    --miner.gastarget 7500000 \
    --miner.gaslimit 10000000  \
    --miner.gasprice 1000000000 &
```

