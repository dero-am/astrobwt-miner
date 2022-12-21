# astrobwt-miner

Support channel for this: https://discord.gg/nvgHnwD3rZ

astrobwt-miner is an optimized miner for DERO (and any forks that use AstroBWTv3). astrobwt-miner written from scratch in C/C++.

Currently, astrobwt-miner supports both stratum (whalesburg.com) and RPC

### Usage ###
To mine on hiveos please visit: https://github.com/dero-am/astrobwt-miner/hiveos.md

To mine with stratum:

```
eg: ./astrobwt-miner -w DERO_ADDRESS.WORKER_NAME -r stratum+tls://pool.whalesburg.com:4300 -p stratum
```
To mine with getwork(mining over RPC to your node):
```
eg: ./astrobwt-miner -w DERO_ADDRESS -r YOUR_NODE:YOUR_PORT -p rpc
```

For further help:

```
./astrobwt-miner -h
```

(bash script files are included with the binary, change your dero address to use it)

Dev fee
dev fee is 4.9%

Downloads
https://github.com/dero-am/astrobwt-miner/releases for all available releases.
