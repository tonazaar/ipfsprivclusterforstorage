
#### Checking number of peers

##### The peers are 0 below

```
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

```



##### The peers are 1 below
- This is after one peer joined the cluster

```
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


```
