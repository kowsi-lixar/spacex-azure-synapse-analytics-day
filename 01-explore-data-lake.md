## Task 1 - Explore the data lake with Azure Synapse SQL On-demand

In this task, you will browse your data lake using SQL On-demand.

1. In a web browser, navigate to the Azure portal (`https://portal.azure.com`) and login with your credentials. Then select **Resource groups**.

    ![Open Azure resource group](./media/01-open-resource-groups.PNG "Azure resource groups")

2. Select the **Synapse Analytics** resource group.

3. Select the **Synapse Analytics** workspace.

4. On the Synapse workspace blade, open Synapse Analytics Studio by selecting **Launch Synapse Studio** from the toolbar.

   ![The Launch Synapse Studio button is highlighted on the Synapse workspace toolbar.](media/ex01-launch-synapse-studio.PNG "Launch Synapse Studio")
   
5. In Synapse Analytics Studio, click 'Ingest'

  ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-01.PNG)
  
6. In Ingest, input 'Task Name: LaunchPad' and select 'Run once now', click 'Next'

  ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-02.PNG)

7. In Ingest, select '+ Create new connection', select 'REST' and 'Continue'

  ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-03.PNG)

8. Enter 'https://api.spacexdata.com/v3/' as the 'Base URL' and 'Authorization Type' 'Anonymous'

  ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-04.PNG)

9. Click 'Test Connection' to ensure connection is working, click 'Create'

  ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-05.PNG)

10. In the 'Specify REST dataset properties' enter 'launchpads' as 'Relevant URL'. Click 'Preview' to view the load, click 'Next'

  ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-06.PNG)
  
11. In 'Destination data store' select '+ Create new connection', select 'Data Lake Gen2' and 'Continue'

    ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-07.PNG)

12. For 'Authorization Method' select 'Account key' and navigate to your 'asadatalake01' created in setup, verify connection 

    ![Open Data hub in Synapse Analytics Studio](./media/ex01-ingest-08.PNG)

