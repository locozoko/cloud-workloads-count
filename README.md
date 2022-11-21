# cloud-workloads-count
Count the number of Cloud Workloads in AWS and Azure

Simple scripts just use the AWS and Azure CLI tool respectively to query the accounts
These scripts assume the AWS/Azure CLI tools are already installed and authenticated to your account


## AWS EC2 Count Usage 
The AWS script will prompt you to select an available AWS profile on your machine and count all EC2 instances across all regions.
This script was created to query a single AWS account and was not tested running across all AWS accounts in an AWS Organization.

```
./awscount.sh 

Available AWS Profiles: 
default
awstest

Profile to use: default
Account: 123456789012 (123456789012)
EC2 instances in ap-south-1: 3
EC2 instances in eu-north-1: 0
EC2 instances in eu-west-3: 0
EC2 instances in eu-west-2: 0
EC2 instances in eu-west-1: 0
EC2 instances in ap-northeast-3: 0
EC2 instances in ap-northeast-2: 0
EC2 instances in ap-northeast-1: 0
EC2 instances in ca-central-1: 0
EC2 instances in sa-east-1: 0
EC2 instances in ap-southeast-1: 0
EC2 instances in ap-southeast-2: 0
EC2 instances in eu-central-1: 7
EC2 instances in us-east-1: 14
EC2 instances in us-east-2: 46
EC2 instances in us-west-1: 27
EC2 instances in us-west-2: 13

----------------------
Timestamp: Mon Nov 21 11:40:20 CST 2022
Profile: default
Total EC2 instances in AWS Account 123456789012: 110
```

## Azure VM Count Usage
The Azure script will use the existing Azure CLI Tenant/Subscription and count all VMs across all regions.
This script does not prompt you to select/change the Tenant/Subscription so you will need to set that prior to running the script.

```
./azurecount.sh 

----------------------------------
Timestamp: Mon Nov 21 11:46:56 CST 2022
Azure Tenant: 12345678-9012-3456-7890-123456789012
Azure Subscription: 22345678-9012-3456-7890-123456789013
Azure Virtual Machines: 50
----------------------------------
```