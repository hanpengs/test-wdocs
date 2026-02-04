# ExploreData

Explain Plan (execution plan) is used to explain the execution method and optimization strategy of query statements. By analyzing the execution plan, administrators can understand the execution of the query, discover potential performance bottlenecks, and optimize it. You can optimize query statements, create appropriate indexes, or adjust the storage structure of the collection based on the execution plan to improve query efficiency and overall performance.

1. Select Cluster Name

     ![exc-name](../../images/whaleal-platform/10-diagnose/exc-name.png)

2. Select a database and click on it to enter the database.

     ![database](../../images/whaleal-platform/10-diagnose/database.png)

3. Select a collection and click on it to enter the collection.

     ![collection](../../images/whaleal-platform/10-diagnose/collection.png)

4. Fill in the statement to be executed in the **FILTER**, and then click the **Find** button

     ![find](../../images/whaleal-platform/10-diagnose/find.png)

     

## FInd

### View Data

Display data information in the database

![find](../../images/whaleal-platform/10-diagnose/find.png)

### Meta Data

**Meta information**

This page contains MongoDB collection information

![Meta-information](../../images/whaleal-platform/10-diagnose/meta-information.png)**Index information**

This page contains all index information in the collection

![Index-information](../../images/whaleal-platform/10-diagnose/index-information.png)

**Collection Diagnose**

This page contains some diagnostic information about the current collection.

![Collection-Diagnose](../../images/whaleal-platform/10-diagnose/collection-diagnose.png)

![Collection-Diagnose2](../../images/whaleal-platform/10-diagnose/collection-diagnose2.png)

## Explain Result

Fill in the statement to be executed in the **FILTER**, and then click the **explain** button

![explain](../../images/whaleal-platform/10-diagnose/explain.png)



### Visual Tree

Formatted explain result

![visual-tree](../../images/whaleal-platform/10-diagnose/visual-tree.png)



### Raw Json

Complete explain result

![explain-resullt](../../images/whaleal-platform/10-diagnose/explain-resullt.png)
