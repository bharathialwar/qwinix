
# qwinix
All the templates for Azure resources creation for each resources
I have Created  "Qwinix" Resource group
Under Qwinix resource group I have created below resources

1. vnet  -- Name: vnet-qwinix , CIDR: 10.2.0.0/16
subnet1 - 10.2.0.0/24  - Bastion Host- Public Facing
subnet-web - 10.2.1.0/24 -web servers -Private
Subnet-DB - 10.2.2.0/24  -- for DB  -- Private

2.. Bastion Host: Name : Bastion-host-qwinix 
        Private ip : 10.2.0.4
         StaticPublic ip : 40.122.24.246
         
3.. Created Web servers using Scale set along with LB
      subnet group : 10.2.1.0/24 -web servers -Private
      2 instances are minimum and maximum 6 instances
      Created scale set up/down if 80% will increase 1 instance
                            if 20% Will decrease 1 instance
                            
      LB Public DNS name : http://websites4qwnx.centralus.cloudapp.azure.com/ >> it will display as " Iac challenge completed: Bharathiraja!"
      LB Public ip:  13.86.99.8 
      
4.. Created Storage Blob and given access to web server subnet group
       sg account name: torage4qwinix
       blob URI : https://storage4qwinix.blob.core.windows.net/blob4qwinix
       
       
5.. Created Azure Database for PostgreSQL servers given access permission to web servers
       Server name: db4qwinixwebserver.postgres.database.azure.com
      
