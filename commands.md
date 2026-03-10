# Commands Used in the Lab

## Enable APIs

gcloud services enable iap.googleapis.com networkmanagement.googleapis.com

## Create privatenet

gcloud compute networks create privatenet –subnet-mode=custom

## Create subnets

gcloud compute networks subnets create privatesubnet-us 
–network=privatenet 
–region=us-east1
–range=172.16.0.0/24



gcloud compute networks subnets create privatesubnet-notus 
–network=privatenet 
–region=us-east1
–range=172.20.0.0/20

## Firewall rule

gcloud compute firewall-rules create privatenet-allow-icmp-ssh-rdp 
–direction=INGRESS 
–priority=1000 
–network=privatenet 
–action=ALLOW 
–rules=icmp,tcp:22,tcp:3389 
–source-ranges=0.0.0.0/0

## Create VM

gcloud compute instances create privatenet-us-vm 
–zone=us-east1-d
–machine-type=e2-micro 
–subnet=privatesubnet-us 
–image-family=debian-12 
–image-project=debian-cloud
