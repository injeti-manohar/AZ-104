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
