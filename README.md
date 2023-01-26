# astrominer

Support channel for this: https://discord.gg/nvgHnwD3rZ

astrominer is an optimized miner for DERO (and any forks that use AstroBWTv3). astrominer written from scratch in C/C++.

Currently, astrominer supports both stratum (whalesburg.com) and RPC

### Usage ###
To mine on hiveos please visit: https://github.com/dero-am/astrominer/hiveos.md


To mine with wss(mining over RPC to your node):
```
eg: ./astrominer -w DERO_ADDRESS -r YOUR_NODE:YOUR_PORT -p rpc -r1 failover_pool_1 -r2 failover_pool_2
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
