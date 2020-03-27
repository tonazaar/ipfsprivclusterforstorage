
Using steps in below link IPFS nodes and are setup. 
https://labs.eleks.com/2019/03/ipfs-network-data-replication.html

It consists of 3 IPFS nodes
- A node on a remote server
- A node on a local system 
- A node on a Raspberry PI  


The goipfs is used (not jsipfs)



- Node0 - A node on a remote server
- Node1 - A node on a local system 
- Node2 - A node on a Raspberry PI  


Install IPFS cluster components

Generate IPFS cluster secret

```
od -vN 32 -An -tx1 /dev/urandom | tr -d ' \n' > clustersecret.txt


```

In Node0

export CLUSTER_SECRET=


Init and start cluster


ipfs-cluster-service init



ipfs-cluster-service daemon


Node the id of the cluster daemon




In Node0


