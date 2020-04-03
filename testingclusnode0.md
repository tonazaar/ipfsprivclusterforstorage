

rameshbn@openvpn-srv:~/ipfsstuffs$ bin/ipfs-cluster-service daemon &
[1] 6219
rameshbn@openvpn-srv:~/ipfsstuffs$ 13:47:56.242  INFO    service: Initializing. For verbose output run with "-l debug". Please wait... daemon.go:46
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



 export IPFS_PATH=~/repos/one
rameshbn@openvpn-srv:~/ipfsstuffs$ ipfs id
{
	"ID": "QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS",
	"PublicKey": "CAASpgIwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC1mKg/VSr+mgnmXzDWA8OlAqHTOjq9to0JZzRAjCrDOGlSbtwgZv3NvXzaeFozOwMOCAv65VF+cv0CUU79/+kz/SSdKZcnUUPMi7Ubl+5pfCiZ9pdu1Z6MrtW+GiSz6zta0nJ6YTyY3MVdiLdWjItBIXDgib0HYtA5+dykgMx490Cdk9jb2FHqKwLCRRb+PEF3fYD8ov394u1YqmXAwpAK7h1tK0TaHtvgAouiUYRM88Ec8gsN8NLUONpzIlH90IMtD3IqRTuwEhKrIUk2PUg3uQqd4ElhJwmfY+LY6yKv34St71LYrpMejathJWkyxy80FpkHnfimEPlJS7sgvlFHAgMBAAE=",
	"Addresses": [
		"/ip4/127.0.0.1/tcp/4002/ipfs/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS",
		"/ip4/157.245.63.46/tcp/4002/ipfs/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS",
		"/ip4/10.15.0.10/tcp/4002/ipfs/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS",
		"/ip4/10.8.0.1/tcp/4002/ipfs/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS",
		"/ip4/172.17.0.1/tcp/4002/ipfs/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS",
		"/ip4/127.0.0.1/tcp/4003/ws/ipfs/QmVwvS2mjw3pvVgFqfYL5pwtnQhf68kWKVGRSWSMaUkSGS"
	],
	"AgentVersion": "go-ipfs/0.4.21/8ca278f45",
	"ProtocolVersion": "ipfs/0.1.0"
}




-------------------------------------------'



~/ipfsstuffs$ bin/ipfs-cluster-ctl id
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



-----------------------------------------------------------
joined


~/ipfsstuffs$ bin/ipfs-cluster-ctl peers ls
12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh | ramesh-Inspiron-3542 | Sees 1 other peers
  > Addresses:
    - /ip4/127.0.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/127.0.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.17.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.17.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.19.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.19.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.21.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.21.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.30.0.1/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/172.30.0.1/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/192.168.29.173/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/192.168.29.173/udp/9096/quic/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
    - /ip4/49.37.198.75/tcp/9096/p2p/12D3KooWCSyyqP4Wbh5e5B91mduJX1CohtUhyNa6USX8Sn5kbQJh
  > IPFS: QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip4/127.0.0.1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip4/172.17.0.1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip4/172.19.0.1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip4/172.21.0.1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip4/172.30.0.1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip4/192.168.29.173/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip6/2405:201:d802:17cf:1a4f:32ff:fef9:8e35/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip6/2405:201:d802:17cf:8de3:c5bb:6502:cac1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
    - /ip6/::1/tcp/4001/p2p/QmUj9KC2XXcFXbeaZ3wRrqJT1WAZ8PQWQha3RYVYACgGFH
12D3KooWHfigHPCDJAWQ9DiTYSbcM5gVZKPSgQPyhjr8zMwwhjVN | openvpn-srv | Sees 1 other peers
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


