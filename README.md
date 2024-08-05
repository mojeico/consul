# consul


----------- base ----------------
-


raft protocol: 
-

- use only server nodes (not client )

needs for: 
- leadership elections 
- quoium 





Gossip protocol: 
-
- use in cluster wide 

needs for: 

- membership of cluster 



LAN gossip pool 

- inside 
- information about new server 


WAN gossip pool 
- 
- global 
- allow servers to pergorm cross datacenters 












Ports



- 8500/tcp             - HTTP API 
- 
- 8301/tcp&udp         - LAN gossip 
- 8302/tcp&udp         - WAN gossip 
- 8300/tcp             - RPC 
- 8600/tcp &  8600/udp - DNS
- 21000-21255          - sidecar 







Show all members 

- consul members


Show only master member and see leader 

- consul operator raft list-peers


Add/remove service manually 

- consul services register service.hcl
- consul services deregister service.hcl





---

Get all records for service discovery

dig @server_ip_address -p 8600 service_name.service.consul 





----------- K/V store --------------
-

-  not encrypted 



consul kv put test/test1/test2/key blabla 

consul kv get test/test1/test2/key

consul kv get -detailed test/test1/test2/key 





















