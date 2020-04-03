
### Create IPFS setup as a private node

Set path for IPFS repo

```
export IPFS_PATH=/home/alarm/ipfsrepos/remoteone

```
- Copy swarm.key to $IPFS_PATH


### Start IPFS daemon 

Start IPFS daemon

```
ipfs daemon &
[1] 752
[alarm@alarmpi ipfsstuffs]$ Initializing daemon...
go-ipfs version: 0.4.23-6ce9a355f
Repo version: 7
System version: arm/linux
Golang version: go1.13.7

[alarm@alarmpi ipfsstuffs]$       
[alarm@alarmpi ipfsstuffs]$ 
[alarm@alarmpi ipfsstuffs]$ Swarm is limited to private network of peers with the swarm key
Swarm key fingerprint: 24c971c0df9eadc036ae5ae6d4c0aa3f
Swarm listening on /ip4/10.42.0.65/tcp/4001
Swarm listening on /ip4/10.42.0.67/tcp/4001
Swarm listening on /ip4/10.42.0.85/tcp/4001
Swarm listening on /ip4/127.0.0.1/tcp/4001
Swarm listening on /ip4/192.168.1.1/tcp/4001
Swarm listening on /ip4/192.168.1.100/tcp/4001
Swarm listening on /ip6/::1/tcp/4001
Swarm listening on /p2p-circuit
Swarm announcing /ip4/10.42.0.65/tcp/4001
Swarm announcing /ip4/10.42.0.67/tcp/4001
Swarm announcing /ip4/10.42.0.85/tcp/4001
Swarm announcing /ip4/127.0.0.1/tcp/4001
Swarm announcing /ip4/192.168.1.1/tcp/4001
Swarm announcing /ip4/192.168.1.100/tcp/4001
Swarm announcing /ip6/::1/tcp/4001
API server listening on /ip4/127.0.0.1/tcp/5001
WebUI: http://127.0.0.1:5001/webui
Gateway (readonly) server listening on /ip4/127.0.0.1/tcp/8080
Daemon is ready

```

### Node1


Get cluster secret key from node0

- In this case 

```
 CLUSTER_SECRET=a10cf512951dec734b5911b9cf4f6c3d299ebee6bf5eb152ebaede973325a7f3

```

Get the bootstrap listener link for node0

- In this case for node0

```
    - /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN

```



##### Init the cluster


- Set the cluster secret in environment and init the cluster
- ipfs-cluster-service init


```
export CLUSTER_SECRET=a10cf512951dec734b5911b9cf4f6c3d299ebee6bf5eb152ebaede973325a7f3

 ipfsstuffs]$ bin/ipfs-cluster-service init
14:21:54.581  INFO     config: Saving configuration config.go:479
configuration written to /home/alarm/.ipfs-cluster/service.json.
14:21:54.586  INFO     config: Saving identity identity.go:73
new identity written to /home/alarm/.ipfs-cluster/identity.json
new empty peerstore written to /home/alarm/.ipfs-cluster/peerstore.


```
##### start cluster

- Start the cluster daemon using bootstraping link from node0

Note:-
- The bootstrap may fail if ports are not opened
- The bootstrap may fail if path of bootstrap is wrong 

```

$  bin/ipfs-cluster-service daemon --bootstrap  /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
07:19:58.518  INFO    service: Initializing. For verbose output run with "-l debug". Please wait... daemon.go:46
07:20:00.290  INFO    cluster: IPFS Cluster v0.12.1 listening on:
        /ip4/127.0.0.1/tcp/9096/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/10.42.0.67/tcp/9096/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/10.42.0.65/tcp/9096/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/10.42.0.85/tcp/9096/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/192.168.1.1/tcp/9096/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/127.0.0.1/udp/9096/quic/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/10.42.0.67/udp/9096/quic/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/10.42.0.65/udp/9096/quic/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/10.42.0.85/udp/9096/quic/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr
        /ip4/192.168.1.1/udp/9096/quic/p2p/12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr

 cluster.go:133
07:20:00.672  INFO    restapi: REST API (HTTP): /ip4/127.0.0.1/tcp/9094 restapi.go:502
07:20:00.672  INFO  ipfsproxy: IPFS Proxy: /ip4/127.0.0.1/tcp/9095 -> /ip4/127.0.0.1/tcp/5001 ipfsproxy.go:307
07:20:00.673  INFO    service: Bootstrapping to /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN daemon.go:214
07:20:00.676  INFO       crdt: crdt Datastore created. Number of heads: 0. Current max-height: 0 crdt.go:262
07:20:00.677  INFO       crdt: 'trust all' mode enabled. Any peer in the cluster can modify the pinset. consensus.go:265
07:20:00.691  INFO    cluster: Cluster Peers (without including ourselves): cluster.go:640
07:20:00.691  INFO    cluster:     - 12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN cluster.go:647
07:20:00.691  INFO    cluster: ** IPFS Cluster is READY ** cluster.go:655
07:20:00.895  INFO    cluster: 12D3KooWJSXbJ9mUWxskiaDCkbz5JLgyC96rcv9DQ4R2GxT1QTEr: joined 12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN's cluster cluster.go:993


#### Observe messages received

- In node2 a file is added to cluster

```
clusnode2.txt:added QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS hello1.txt

```

- We get below message in node1
```
[alarm@alarmpi ipfsstuffs]$ 07:20:18.126  INFO       crdt: new pin added: QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS consensus.go:209
07:20:18.191  INFO       crdt: adding new DAG head: QmajFHASxqnPKRxwzfUgYvW4DT5rP48qk8v8S1WfuPXu4T (height: 2) heads.go:114
07:20:18.257  INFO   ipfshttp: IPFS Pin request succeeded:  QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS ipfshttp.go:372
```

#### Verify if file added is visible in this node

- It is available


```
[alarm@alarmpi $ ipfs cat QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS
hello world1

```


