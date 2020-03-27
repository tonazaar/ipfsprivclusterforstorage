
A) Using steps in below link IPFS nodes are setup. 
- https://labs.eleks.com/2019/03/ipfs-network-data-replication.html

B) It consists of 3 IPFS nodes
- A node on a remote server
- A node on a local system 
- A node on a Raspberry PI  


The goipfs is used (not jsipfs)

C) Naming of the nodes as follows

- Node0 - A node on a remote server
- Node1 - A node on a local system 
- Node2 - A node on a Raspberry PI  

Create the swarm.key and copy to repo directory of all he nodes

D) Install IPFS cluster components

Example of downloading is as follows

```
https://dist.ipfs.io/#ipfs-cluster-service

wget https://dist.ipfs.io/ipfs-cluster-service/v0.12.1/ipfs-cluster-service_v0.12.1_linux-amd64.tar.gz

gunzip ipfs-cluster-service_v0.12.1_linux-amd64.tar.gz

tar xvf ipfs-cluster-service_v0.12.1_linux-amd64.tar

```

E) Generate IPFS cluster secret

```
od -vN 32 -An -tx1 /dev/urandom | tr -d ' \n' > clustersecret.txt

```

Secret looks as below
```
cat clustersecret.txt

a10cf512951dec734b5911b9cf4f6c3d299ebee6bf5eb152ebaede973325a7f3

```

F) In Node0 init and start cluster

```
export CLUSTER_SECRET=a10cf512951dec734b5911b9cf4f6c3d299ebee6bf5eb152ebaede973325a7f3

```

##### Init and start cluster


- ipfs-cluster-service init

```
 ipfs-cluster-service init
12:36:39.040  INFO     config: Saving configuration config.go:479
configuration written to /home/rameshbn/.ipfs-cluster/service.json.
12:36:39.041  INFO     config: Saving identity identity.go:73
new identity written to /home/rameshbn/.ipfs-cluster/identity.json
new empty peerstore written to /home/rameshbn/.ipfs-cluster/peerstore.

```


- ipfs-cluster-service daemon

```
bin/ipfs-cluster-service daemon &
[1] 6219

$ 13:47:56.242  INFO    service: Initializing. For verbose output run with "-l debug". Please wait... daemon.go:46
13:47:56.750  INFO    cluster: IPFS Cluster v0.12.1 listening on:
        /ip4/127.0.0.1/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/10.15.0.10/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/10.8.0.1/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/172.17.0.1/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/127.0.0.1/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/157.245.63.46/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/10.15.0.10/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/10.8.0.1/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
        /ip4/172.17.0.1/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN

 cluster.go:133
13:47:56.757  INFO    restapi: REST API (HTTP): /ip4/127.0.0.1/tcp/9094 restapi.go:502
13:47:56.758  INFO  ipfsproxy: IPFS Proxy: /ip4/127.0.0.1/tcp/9095 -> /ip4/127.0.0.1/tcp/5001 ipfsproxy.go:307
13:47:56.760  INFO       crdt: crdt Datastore created. Number of heads: 0. Current max-height: 0 crdt.go:262
13:47:56.760  INFO       crdt: 'trust all' mode enabled. Any peer in the cluster can modify the pinset. consensus.go:265
13:47:56.777  INFO    cluster: Cluster Peers (without including ourselves): cluster.go:640
13:47:56.777  INFO    cluster:     - No other peers cluster.go:642
13:47:56.777  INFO    cluster: ** IPFS Cluster is READY ** cluster.go:655

```


#####Node the id of the cluster daemon


```
$ bin/ipfs-cluster-ctl id
12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN | openvpn-srv | Sees 0 other peers
  > Addresses:
    - /ip4/10.15.0.10/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/10.15.0.10/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/10.8.0.1/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/10.8.0.1/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/127.0.0.1/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/127.0.0.1/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/157.245.63.46/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/172.17.0.1/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
    - /ip4/172.17.0.1/udp/9096/quic/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
  > IPFS: QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS
    - /ip4/10.15.0.10/tcp/4002/p2p/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS
    - /ip4/10.8.0.1/tcp/4002/p2p/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS
    - /ip4/127.0.0.1/tcp/4002/p2p/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS
    - /ip4/127.0.0.1/tcp/4003/ws/p2p/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS
    - /ip4/157.245.63.46/tcp/4002/p2p/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS
    - /ip4/172.17.0.1/tcp/4002/p2p/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS


```

##### Note the listener of cluster

- In this case

```
    - /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN

```


##### In node1, node2 follow the below steps





