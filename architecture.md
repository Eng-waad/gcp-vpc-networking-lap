# Network Architecture

This lab demonstrates how Google Cloud VPC networking works across multiple networks.

## Networks

### mynetwork
- Auto mode → converted to Custom mode
- Multiple regional subnets
- Two VM instances

### managementnet
- Custom VPC
- Subnet: 10.240.0.0/20

### privatenet
- Custom VPC
- Subnet 1: 172.16.0.0/24
- Subnet 2: 172.20.0.0/20

## Connectivity

Internal connectivity works only between instances in the same VPC network.

Instances across different VPCs cannot communicate internally unless VPC Peering or VPN is configured.
