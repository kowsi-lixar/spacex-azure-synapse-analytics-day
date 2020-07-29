## Task 3 - Data Science with Apache Spark

Azure Synapse Analytics provides a unified environment for both data science and data engineering. What this means in practice, is that your data scientists can train and deploy models using Azure Synapse Analytics and your data engineers can write T-SQL queries that use those models to make predictions against tabular data stored in a SQL Pool database table.

In this exercise, you will leverage Apache Spark to write PySpark code to transform data

1. Select the **Synapse Analytics** resource group.

2. Select the **Synapse Analytics** workspace.

3. On the Synapse workspace blade, open Synapse Analytics Studio by selecting **Launch Synapse Studio** from the toolbar.
   
4. Click 'Manage'

  ![Open Data hub in Synapse Analytics Studio](./media/ex03-develop-01.PNG)

5. Apache Spark Pool > New to create a new pool cluster

  ![Open Data hub in Synapse Analytics Studio](./media/ex03-develop-02.PNG)

6. Input the following and click 'Create'

  ![Open Data hub in Synapse Analytics Studio](./media/ex03-develop-04.PNG)
  
7. Click 'Develop'

   ![Open Data hub in Synapse Analytics Studio](./media/ex03-develop-03.PNG)
   
8.  Create a Notebook

   ![Open Data hub in Synapse Analytics Studio](./media/ex03-develop-05.PNG)

9. In put the following code:

   ```py
      import pyspark.sql
      
     ## Build dataframes from each API Method ##
      rockets_df = spark.read.json("/synapse/data/spacex/rockets/*.json")
      payloads_df = spark.read.json("/synapse/data/spacex/payloads/*.json")
      launchpads_df = spark.read.json("/synapse/data/spacex/launchpads/*.json")
      launches_df = spark.read.json("/synapse/data/spacex/launches/*.json")
   ```
   ```py
      rockets_df.registerTempTable( "rockets" )
      payloads_df.registerTempTable( "payloads" )
      launchpads_df.registerTempTable( "launchpads" )
      launches_df.registerTempTable( "launches" )
    ```
