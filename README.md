# Traders
- This tutorial project aims to create a modern data warehouse from a web-platform database.
- This project implemented locally using WSL ubuntu and postgresql where the database "Traders" holds several schemas for the source database and for the data warehouse target layers.
- some small tables from the source database have been replaced with seed constant data that could be modified manually.
- Continuous Integration checks utilized by configuring workflow triggers when new "PR"events happened.


## Traders Data warehouse layers
1. Source dataset'schema' contains database tables
2. Staging layer contains dbt denormalized models 'stg_'
3. Vault layer where data vault modelling is implemented according to business needs.'vlt_'
4. Semantic layer where the dimensional model is implemented. 'sem_'


<img src="https://github.com/AmmarSahyoun/dbt_traders/blob/main/assets/architecture.png" alt="Draft diagram" width="1000" height="600">


### Additional notes:
- When working with big data it's crusual to use distributed computing storage with a columnar reading capability like BigQuery or Synapse to leverage of partitioning capability for a better performance and to reduce query latency and cost.

 
### Advantages of Data Warehouse:
- Scalability: They can handle massive amounts of data.
- Performance: Fast BI reports and complex analysis.
- Consistency: Ensures data consistency across the organization.
- Flexibility: Data warehouses can be adapted to changing business needs.