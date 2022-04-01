FROM ethereum/client-go:latest
ADD ../genesis.json /genesis.json
ADD signer.json /signer.json
ADD signer.pass /signer.pass
RUN   echo 'geth --cache 512 init /genesis.json' > geth.sh && 	echo 'mkdir -p /root/.ethereum/keystore/ && cp /signer.json /root/.ethereum/keystore/' >> geth.sh && 	echo $'exec geth --networkid 234666 --cache 512 --port 30304 --nat extip:128.199.80.145 --maxpeers 50  --ethstats \'node3seal:98GonHWOfRE5BkGfsN1TPgopB7gIjEd3uoqvRz1OUkaTRUmKRxnEVsJl7cCt@128.199.80.145:8080\' --bootnodes enode://96ffe79f161207161d080df5f3793bdfadf1c8c9bbf93937975081160fdb123bb0943e49b4ca8010ca310bb89613bff76002dbe583468142f4d238bed2ff9f9d@128.199.80.145:30303  --unlock 0 --password /signer.pass --mine --miner.gastarget 7500000 --miner.gaslimit 10000000 --miner.gasprice 1000000000' >> geth.sh
