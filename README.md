# astrominer

Support channel for this: https://discord.gg/nvgHnwD3rZ

astrominer is an optimized miner for DERO (and any forks that use AstroBWTv3). astrominer written from scratch in C/C++.

astrominer supports both solo mining and pool mining.

### Usage ###
To mine on hiveos please visit: https://github.com/dero-am/astrominer/hiveos.md


To mine with wss(mining over RPC to your node):
```
eg: ./astrominer -w DERO_ADDRESS -r YOUR_NODE:YOUR_PORT -r1 failover_pool_1 -r2 failover_pool_2
```
Arguments:
```
	-h	show this message
	-r	pool url (required)
	-r1	failover pool url 1 (optional)
	-r2	failover pool url 2 (optional)
	-w	your wallet (required)
	-p	pool type. stratum or RPC (optional, default: rpc)
	-m	mining threads (default: all threads)
	-k	kernel number (-1(auto select), 1(intel) or 2(amd and others)
	-a	cpu affinity: specify cpu IDs to bind to, separated by commas without space, example( -a 0,2,4,6,8,10 ) | the number of cpu IDs must be equal to the number of mining threads | use -1 to disable cpu affinity | (default affinity: 0,1,2,3,...,N) 
	-show-latency	show the latency between miner and pool (doesn't work with WINDOWS Node) 
	-log-interval	time between 2 logging lines in second (default: 5 seconds) 
	-opmem	Performing memory optimization before mining, require ROOT permission (not available on android) 
	-disable-api	Disable miner API on port 60666, this API is required for hiveOS
```

For further help:

```
./astrominer -h
```

(bash script files are included with the binary, change your dero address to use it)

### Dev fee ###
dev fee is 4.9%

### Downloads ###
Visit https://github.com/dero-am/astrominer/releases for all available releases.
