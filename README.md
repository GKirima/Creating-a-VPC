<<<<<<< HEAD
#VPC Configuration
VPC CIDR Range: 10.0.0.0/22
Region: [Your AWS Region]
Number of Availability Zones: 2
Total Number of Subnets: 4 (2 per AZ)

#Subnet Distribution
Availability Zone 1
1. Public Subnet

- CIDR: 10.0.0.0/24
- Available IP addresses: 251 (Amazon reserves 5 IPs)
2. Private Subnet

- CIDR: 10.0.1.0/24
- Available IP addresses: 251 (Amazon reserves 5 IPs)

#Availability Zone 2
1. Public Subnet

- CIDR: 10.0.2.0/24
- Available IP addresses: 251 (Amazon reserves 5 IPs)

2. Private Subnet

- CIDR: 10.0.3.0/24
- Available IP addresses: 251 (Amazon reserves 5 IPs)

#Step-by-Step Creation Process
#Create VPC
aws ec2 create-vpc \
    --cidr-block 10.0.0.0/22 \
    --tag-specifications 'ResourceType=vpc,Tags=[{Key=Name,Value=MyVPC}]'
=======
# Creating-a-VPC
Step by step procedure for creating a VPC in AWS cloud
>>>>>>> 600e359d126dbc6932ab30612fbcd2bd70fc0e7c
