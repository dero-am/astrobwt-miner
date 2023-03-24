Each thread of astrominer needs 5 x pages(2MB), if you want to run 16 threads then you will need 16 x 5 = 80Pages (160MB)
# LINUX
### Single physical CPU: ###
run one of these commands before running the miner:

(1) `/usr/sbin/sysctl -w vm.nr_hugepages=NUMBER_OF_PAGE`

(2) `echo NUMBER_OF_PAGE > /sys/devices/system/node/node0/hugepages/hugepages-2048kB/nr_hugepages;`

### Dual or more physical CPUs (server): ###
First you need to calculate how many threads you want to run on each node, then set them accordingly as below (before running the miner):
`echo NUMBER_OF_PAGE_FOR_NODE_0 > /sys/devices/system/node/node0/hugepages/hugepages-2048kB/nr_hugepages;`

`echo NUMBER_OF_PAGE_FOR_NODE_1 > /sys/devices/system/node/node1/hugepages/hugepages-2048kB/nr_hugepages;`

`echo NUMBER_OF_PAGE_FOR_NODE_2 > /sys/devices/system/node/node2/hugepages/hugepages-2048kB/nr_hugepages;`

`echo NUMBER_OF_PAGE_FOR_NODE_3 > /sys/devices/system/node/node3/hugepages/hugepages-2048kB/nr_hugepages;`

If you don't do this, the miner will allocate the hugepages randomly on each node and your hashrate will end up slower.


# Windows
There are 2 ways to enable hugepages on Windows:
- Run astrominer.exe with -opmem with Administrator rights. astrominer will register the right to use hugepages for you, then you need a reboot (you only need to do this once).
- Or follow this tutorial: https://learn.microsoft.com/en-us/sql/database-engine/configure-windows/enable-the-lock-pages-in-memory-option-windows?redirectedfrom=MSDN&view=sql-server-ver16
