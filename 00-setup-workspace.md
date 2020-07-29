# Setup the Azure Synapse Analytics (ASA) workspace
## Task 0 - Create resources

1. Create a new resource group

2. In the resource group, create a regular blob storage account.

3. In the resource group, create an empty Azure Synapse Analytics workspace.

4. Create the following file systems in the blob storage account of the workspace: `spacex`.

5. Create a linked service to the first pool of the workspace. Configure it to connect with username and password, and use the credentials of the workspace's SQL admin account. It is recommended to name the linked service `spacexcluster` to simplify the import of datasets, data flows, and pipelines later.

6. Create a linked service to the storage account. Configure it to connect with the account key. It is recommended to name the linked service `asadatalake01` to simplify the import of datasets and pipelines later.

7. Create a linked service to the blob storage account. Configure it to connect with the account key. It is recommended to name the linked service `asastore01` to simplify the import of datasets and pipelines later.

8.  Ensure the `Workspace` security principal (which has the same name as the `Workspace`) and the `MasterUser` (the one used to create the `Workspace`) are added with the `Storage Blob Data Owner` role to the `asastore01`.
