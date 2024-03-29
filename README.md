# astrominer

Support channel for this: https://discord.gg/nvgHnwD3rZ

astrominer is an optimized miner for DERO (and any forks that use AstroBWTv3)

### Usage ###
To mine on hiveos please visit: https://github.com/dero-am/astrobwt-miner/blob/main/hiveos.md


To mine with wss(mining over RPC to your node):
```
eg: ./astrominer -w DERO_ADDRESS -r YOUR_NODE:YOUR_PORT -r1 failover_pool_1 -r2 failover_pool_2
```
For further help:

```
./astrominer -h
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
	-i	intensive level (valid values [0,10] (optional, default: 10))
	-k	kernel number (-1(auto select), 1(intel) or 2(amd and others)
	-ft	fine tune kernel (-1(auto select), 1(low, mid-end CPUs) or 2(high-end CPUs))
	-a	cpu affinity (linux only): specify cpu IDs to bind to, separated by commas without space, example( -a 0,2,4,6,8,10 ) | the number of cpu IDs must be equal to the number of mining threads | use -1 to disable cpu affinity | (default affinity: 0,1,2,3,...,N) 
	-show-latency	show the latency between miner and pool (doesn't work with Windows Node) 
	-log-interval	time between 2 logging lines in second (default: 5 seconds) 
	-opmem	Performing memory optimization before mining, require ROOT permission (not available on android) 
	-disable-api	Disable miner API on port 60666, this API is required for hiveOS 
	-no-watchdog	Disable astrominer watchdog
	-log-to-file	Redirect all astrominer log to a file
	-sock-address	Socks5 ip address with port (eg: 127.0.0.1:8192) (default: null)
	-sock-auth	Socks5 username and password (eg: username:password). NOTE: this username and password can't contain space and : symbol (default: null)
	-report-realtime-hashrate	 Enable sending realtime hashrate to hansen33 mod node (default: disable)
	-zero-hr-restart-time	 Time (in second), restart (or exit if the watchdog is disabled) the miner after being zero hashrate for a while (default: 120 seconds, set -1 to disable)
```

(bash script files are included with the binary, change your dero address to use it)

### Dev fee ###
dev fee is 4.9%

### Downloads ###
Visit https://github.com/dero-am/astrominer/releases for all available releases.
