FROM ethereum/client-go:latest
ADD ../genesis.json /genesis.json
RUN   echo 'geth --cache 512 init /genesis.json' > geth.sh && 	echo $'exec geth --networkid 234666 --cache 512 --port 30303 --nat extip:128.199.80.145 --maxpeers 512 --light.maxpeers=256 --light.serve=50 --ethstats \'node3:98GonHWOfRE5BkGfsN1TPgopB7gIjEd3uoqvRz1OUkaTRUmKRxnEVsJl7cCt@128.199.80.145:8080\'    --miner.gastarget 0 --miner.gaslimit 0 --miner.gasprice 0' >> geth.sh
ENTRYPOINT ["/bin/sh", "geth.sh"]