### Back to [Database Requirements](/db_requirements/content/README.md#5-datawarehouse)

- [Datawarehouse](#datawarehouse)
  - [1 Functional Requirements](#1-functional-requirements)
  - [2 Non-Functional Requirements](#2-non-functional-requirements)

# Datawarehouse

The Sports Hub Portal generates a large amount of data. This data is stored in an operational database, which is optimized for transactional processing. However, the portal needs to maintain historical data for archiving, analysis, and reporting purposes. A data warehouse is needed to store this historical data and enable advanced analytics and reporting. 

## 1 Functional Requirements 

1. The data warehouse should support the collection and storage of Sports Hub Portal historical data. 
2. The data warehouse should allow for efficient querying and analysis of data. 
3. The data warehouse should support slowly changing dimensions to capture changes in data over time, such as player transfers, team mergers, and changes in league rules. 
4. The data warehouse should be capable of extracting data from the operational database daily while minimizing the impact on the operational database's performance. 
5. The data warehouse should be able to transform the extracted data into a format that is compatible with the data warehouse's schema and data model. 
6. The data warehouse should support the incremental loading of data, allowing for the efficient retrieval and insertion of new and updated data since the last ETL run. 
7. The data warehouse should include robust error handling and logging mechanisms, enabling the identification and resolution of data quality issues and other ETL errors. 
8. The data warehouse's ETL process should be designed with maintainability in mind, including clear documentation, modularity, and testability. 
9. The data warehouse's ETL process should be integrated with relevant data governance and metadata management tools to support data lineage and version control. 
10. The data warehouse should provide robust data quality controls, including data profiling, data cleansing, and data validation, to ensure the accuracy and consistency of data. 

## 2 Non-Functional Requirements

### Scalability 

The DWH should be able to handle a reasonable amount of data growth as the sports web portal expands over time. The system should be able to accommodate future data growth without requiring major hardware upgrades or experiencing significant performance degradation. 

### Performance 

The system should be optimized for fast query processing and response times. Queries should be completed within a reasonable time limit, and the system should be able to handle a reasonable volume of queries simultaneously. 

### Availability 

The DWH should be available to users during peak usage hours, and scheduled maintenance windows should be used to perform updates and maintenance. The system should be designed with redundancy and failover mechanisms to minimize downtime and disruptions. 

### Security 

The system should ensure that data is protected from unauthorized access or modification. The DWH should have security measures in place such as access controls and data encryption and should comply with relevant security standards. 

### Reliability 

The system should be designed to operate without major errors or interruptions. The DWH should be thoroughly tested to ensure that it can handle a variety of scenarios without crashing or experiencing other issues. It should have mechanisms in place to detect and recover from errors or failures. 

### Maintainability 

The system should be designed to be easy to maintain and update as needed. The DWH should be modular so that individual components can be updated or replaced without affecting the rest of the system. It should have clear documentation and a change management process to make it easy for developers to maintain and modify. 
