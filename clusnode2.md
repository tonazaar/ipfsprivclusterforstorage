

##### Refer steps in node1 for 
- starting IPFS
- Init cluster

[Link to refer ](clusnode1.md)



##### Start the cluster node2   

```
Inspiron-3542:~/ipfsstuffs$ bin/ipfs-cluster-service daemon --bootstrap  /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN
11:53:44.767  INFO    service: Initializing. For verbose output run with "-l debug". Please wait... daemon.go:46
11:53:45.416  INFO    cluster: IPFS Cluster v0.12.1 listening on:
        /ip4/127.0.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/192.168.29.173/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.17.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.19.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.30.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.21.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/127.0.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/192.168.29.173/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.17.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.19.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.30.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
        /ip4/172.21.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh

 cluster.go:133
11:53:51.609  INFO  ipfsproxy: IPFS Proxy: /ip4/127.0.0.1/tcp/9095 -> /ip4/127.0.0.1/tcp/5001 ipfsproxy.go:307
11:53:51.609  INFO    service: Bootstrapping to /ip4/157.245.63.46/tcp/9096/p2p/12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN daemon.go:214
11:53:51.609  INFO    restapi: REST API (HTTP): /ip4/127.0.0.1/tcp/9094 restapi.go:502
11:53:51.609  INFO       crdt: crdt Datastore created. Number of heads: 0. Current max-height: 0 crdt.go:262
11:53:51.609  INFO       crdt: 'trust all' mode enabled. Any peer in the cluster can modify the pinset. consensus.go:265
11:53:51.611  INFO    cluster: Cluster Peers (without including ourselves): cluster.go:640
11:53:51.611  INFO    cluster:     - No other peers cluster.go:642
11:53:51.611  INFO    cluster: ** IPFS Cluster is READY ** cluster.go:655
11:53:52.156  INFO    cluster: 12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh: joined 12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN's cluster cluster.go:993

```

#### Observe cluster joining info in above

```
11:53:52.156  INFO    cluster: 12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh: joined 12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN's cluster cluster.go:993

```

#### Creating file for testing

 - Creating file in node2

```
-Inspiron-3542:~/ipfsstuffs$ bin/ipfs-cluster-ctl add /tmp/hello1.txt
added QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS hello1.txt
11:57:54.945  INFO    cluster: pinning QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS on [12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh 12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN]: cluster.go:1400
11:57:54.997  INFO       crdt: new pin added: QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS consensus.go:209
11:57:55.062  INFO       crdt: adding new DAG head: QmZgJRsyQNtDcfzH8zEFVaEcSNdpU5rTTdhqDPZEXufACN (height: 1) heads.go:114
11:57:55.207  INFO      adder: QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS successfully added to cluster adder.go:182
11:57:55.207  INFO restapilog: 127.0.0.1 - - [26/Mar/2020:11:57:54 +0530] "POST /add?chunker=size-262144&cid-version=0&hash=sha2-256&hidden=false&layout=&local=false&name=&nocopy=false&progress=false&raw-leaves=false&recursive=false&replication-max=0&replication-min=0&shard=false&shard-size=104857600&stream-channels=true&user-allocations=&wrap-with-directory=false HTTP/1.1" 200 93
 restapi.go:117
ramesh@ramesh-Inspiron-3542:~/ipfsstuffs$ 11:57:55.488  INFO   ipfshttp: IPFS Pin request succeeded:  QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS ipfshttp.go:372

```

#### Checking if file is pinned

It shows pinned in two places
- Not sure if it is correct

```
-Inspiron-3542:~/ipfsstuffs$ bin/ipfs-cluster-ctl status QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS
11:58:43.434  INFO restapilog: 127.0.0.1 - - [26/Mar/2020:11:58:43 +0530] "GET /pins/QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS?local=false HTTP/1.1" 200 648
 restapi.go:117
QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS :
    > ramesh-Inspiron-3542 : PINNED | 2020-03-26T11:58:43.293125766+05:30
    > openvpn-srv          : PINNED | 2020-03-26T06:28:43.412582665Z

```

##### Testing file in node2

On node2 testing

```
Inspiron-3542:~/ipfsstuffs$ ipfs cat QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS
hello world1

```



##### Testing file in node0

On node0 testing

```
~/ipfsstuffs$  ipfs cat QmRJrrgf3UgHmf8DcDtdBiYeJke7Qiq2vPvSMNYW6GWhRS
hello world1
```


