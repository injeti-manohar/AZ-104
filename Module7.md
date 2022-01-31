# Azure Storage
> company has documents, spreadsheets, and videos. This information needs to be securely shared across the organization and across geographical areas. The data must be quickly recovered if there is a datacenter failure


An Azure storage account contains all of your Azure Storage data objects, including blobs, file shares, queues, tables, and disks. The storage account provides a unique namespace for your Azure Storage data that's accessible from anywhere in the world over HTTP or HTTPS. Data in your storage account is durable and highly available, secure, and massively scalable
Encryption -- All data in your storage account is automatically encrypted on the service side.
Migrate data to azure storage -- Microsoft provides services and utilities for importing your data from on-premises storage devices or third-party cloud storage providers. Which solution you use depends on the quantity of data you're transferring.

### Azure Storage Account
##### Highly secure, durable and scalable -- 
- You replicate data across datacenters or geographical regions for protection against unexpected outages
- Encrypted & with RBAC manage security

##### Accesible - 
Get a URL for your data in Azure Storage hence making it  accessible from anywhere in the world over HTTP or HTTPS

##### diversified
-`OBJECT STORAGE --> Blobs` -- DR, BACKUPS, unstructered data
- `files -- Block storage` -- > Files are fully managed file shares in the cloud
- `structed data` -- Structured data includes Tables, Cosmos DB, and Azure SQL DB. Tables are a key/value, autoscaling NoSQL store. Cosmos DB is a globally distributed database service. Azure SQL DB is a fully managed database-as-a-service built on SQL.

##### tiers 
`standard`-- HDD
`PREMIUM` -- SSD

### Azure storage service

✓ `Blobs` : Blob storage is ideal for:

- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.

✓ `Azure Table storage` is now part of Azure Cosmos DB

✓ `queues` Queues are used to store lists of messages to be processed asynchronously.

✓ `Azure Files` enables you to set up highly available network file shares that can be accessed by using the standard Server Message Block (SMB) protocol. That means that multiple VMs can share the same files with both read and write access
-  store certain scripts , configuration files 
- Many on-premises applications use file shares. This feature makes it easier to migrate those applications that share data to Azure

*BLOBS & FILES are popular among Cloud Admins while TABLES & QUEQUES are more popular among CLOUD DEVELOPERS*

#### Azure data Replication 
You can choose to replicate your data within the same data center, across zonal data centers within the same region, and even across regions. Replication ensures that your storage account meets the Service-Level Agreement (SLA) for Storage even in the face of failures.

#### Securing Endpoints
Firewalls and Virtual Networks restricts access to the Storage Account from specific Subnets on Virtual Networks or public IPs.
Subnets and Virtual Networks must exist in the same Azure Region or Region Pair as the Storage Account

#### Blobs
Massively scalable and secure object storage for cloud-native workloads, archives, data lakes, high-performance computing and machine learning

> Entirely in portal checks slides
