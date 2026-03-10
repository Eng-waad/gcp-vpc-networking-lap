# gcp-vpc-networking-lap
# GCP VPC Networking Lab

This project demonstrates the implementation of Google Cloud VPC Networking including:

- Creating Auto Mode VPC Network
- Converting Auto Mode to Custom Mode
- Creating Custom VPC Networks
- Configuring Firewall Rules
- Deploying VM Instances
- Testing connectivity between instances

## Architecture Overview

The lab environment includes three VPC networks:

1. mynetwork
2. managementnet
3. privatenet

Each network contains specific subnets and VM instances.

## Networks

| Network | Mode |
|------|------|
| mynetwork | Custom |
| managementnet | Custom |
| privatenet | Custom |

## VM Instances

| Instance | Network | Zone |
|--------|--------|------|
| mynet-us-vm | mynetwork | us-east1-d |
| mynet-notus-vm | mynetwork | europe-west1-b |
| managementnet-us-vm | managementnet | us-east-d |
| privatenet-us-vm | privatenet | us-east-d |

## Firewall Rules

- allow SSH
- allow ICMP
- allow RDP
- allow IAP SSH

## Connectivity Test

- Internal communication works only inside the same VPC
- External IP connectivity works across networks

## Screenshots

See /screenshots folder.
