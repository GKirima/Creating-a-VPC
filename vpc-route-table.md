#Create public route table
aws ec2 create-route-table
--vpc-id
--tag-specifications 'ResourceType=route-table,Tags=[{Key=Name,Value=Public-RT}]'

#Add route to Internet Gateway
aws ec2 create-route
--route-table-id
--destination-cidr-block 0.0.0.0/0
--gateway-id

#Associate public subnets with public route table
aws ec2 associate-route-table
--subnet-id
--route-table-id

#aws ec2 associate-route-table
--subnet-id
--route-table-id
