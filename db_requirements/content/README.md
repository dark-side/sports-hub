### Back to [Sports Hub portal product map](../../README.md#sports-hub-platform-details)

- [1 Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Scope](#12-scope)
  - [1.3 Estimations](#12-estimations)
- [2 Database Design and Data Modeling](#2-database-design-and-data-modeling)
- [3 Database Implementation](#3-database-implementation)
- [4 Data Integration](#4-data-integration)
- [5 Datawarehouse](#5-datawarehouse)

# 1 Introduction

## 1.1 Purpose

The purpose of this document is to define the requirements for the database, which will underpin a sports web portal, alongside enumerating the technical tasks.

## 1.2 Scope 

The database will be responsible for storing and managing data related to sports, including articles, videos, surveys, advertisements, etc. 

## 1.3 Estimations

You can find estimations for all the tasks here:
- [database development estimations](/db_requirements/content/database_estimations.xlsx)

# 2 Database Design and Data Modeling

Follow [this link](/db_requirements/database_design_and_data_modeling/README.md) to review requirements for this section.

**In scope of those requirements, implement the next tasks:**

<details>
  <summary>1. Environment setup and configuration:</summary>

  1. Install and configure RDBMS. 
  2. Install and configure DB management tool. 
  3. Install and configure data integration tool. 
  4. Git configuration. 

</details>

<details>
  <summary>2. Create an Entity-Relationship Diagram (ERD) for operational DB based on the identified entities and relationships:</summary>

  1. Identify the entities that need to be represented in the database. 
  2. Analyze the relationships between the entities. 
  3. Identify the attributes associated with each entity. 
  4. Choose data types for entities. 
  5. Determine primary key for each entity. 
  6. Normalize the data model to minimize redundancy and improve efficiency.  

</details>

<details>
  <summary>3. Create an Entity-Relationship Diagram (ERD) for raw data DB based on the identified entities and relationships:</summary>

  1. Identify the entities that need to be represented in the database. 
  2. Analyze the relationships between the entities. 
  3. Identify the attributes associated with each entity. 
  4. Choose data types for entities. 
  5. Determine primary key for each entity. 
  6. Normalize the data model to minimize redundancy and improve efficiency.  

</details>

<details>
  <summary>4. Create data dictionary for operational DB according to ERD:</summary>

  1. Describe entities related to articles. 
  2. Describe entities related to videos. 
  3. Describe entities related to comments. 
  4. Describe entities related to publication categories. 
  5. Describe entities related to users’ data. 
  6. Describe entities related to authors of publications. 
  7. Describe entities related to publication partners. 
  8. Describe entities related to surveys. 
  9. Describe entities related to social network data. 
  10. Describe entities related to banners. 
  11. Describe entities related to advertisement.  
  12. Describe entities related to users’ subscription. 
  13. Describe entities related to additional entities that were identified during DB modeling. 

</details>

<details>
  <summary>5. Create data dictionary for raw data DB according to ERD:</summary>

  1. Describe entities related to articles. 
  2. Describe entities related to article categories. 
  3. Describe entities related to users’ data. 
  4. Describe entities related to partners. 
  5. Describe entities related to additional entities that were identified during DB modeling. 

</details>

<details>
  <summary>6. Create operational DB according to ERD and data dictionary:</summary>

  1. Create Operational DB. 
  2. Create entities related to articles. 
  3. Create entities related to videos. 
  4. Create entities related to comments. 
  5. Create entities related to publication categories. 
  6. Create entities related to users’ data. 
  7. Create entities related to authors of publications. 
  8. Create entities related to publication partners. 
  9. Create entities related to surveys. 
  10. Create entities related to social network data. 
  11. Create entities related to banners. 
  12. Create entities related to advertisement.  
  13. Create entities related to users’ subscription. 
  14. Create entities related to additional entities that were identified during DB modeling. 

</details>

<details>
  <summary>7. Create raw data DB according to ERD and data dictionary:</summary>

  1. Create Raw DB. 
  2. Create entities related to articles. 
  3. Create entities related to article categories. 
  4. Create entities related to users’ data. 
  5. Create entities related to partners. 
  6. Create entities related to additional entities that were identified during DB modeling. 

</details>

# 3 Database Implementation

Follow [this link](/db_requirements/database_implementation/README.md) to review requirements for this section.

**In scope of those requirements, implement the next tasks:**

<details>
  <summary>1. Generate test data set for operational DB:</summary>

1. Generate data related to articles. 
2. Generate data related to videos. 
3. Generate data related to comments. 
4. Generate data related to publication categories. 
5. Generate data related to users. 
6. Generate data related to authors of publications. 
7. Generate data related to publication partners. 
8. Generate data related to surveys. 
9. Generate data related to social networks. 
10. Generate data related to banners. 
11. Generate data related to advertisement.  
12. Generate data related to users’ subscription. 
13. Generate data related to additional entities that were identified during DB modeling. 

</details>

<details>
  <summary>2. Implement functional requirements for manipulating and managing data in operational DB:</summary>

1. Implement functionality to log any data changes into a specific DB table. 
2. Implement functionality to log any errors and failures into a specific DB table. 
3. Implement functionality to add/edit/delete data related to articles. 
4. Implement functionality to enable/disable ability to comment on an article. 
5. Implement functionality to add/edit/delete data related to videos. 
6. Implement functionality to enable/disable ability to comment on a video. 
7. Implement functionality to enable/disable ability to share a video. 
8. Implement functionality to add/edit/delete data related to publication categories (sports, leagues, teams). 
9. Implement functionality to add/edit/delete data related to users. 
10. Implement functionality to store users’ activity. 
11. Implement functionality to notify administrators of any suspicious or unusual user activity. 
12. Implement functionality to export users’ activity data for requested period in CSV or Excel file. 
13. Implement functionality to allow users viewing their own activity history, including past logins, content creation and modification. 
14. Implement functionality to purge users’ activity data once in 90 days. 
15. Implement functionality to add/edit/delete data related to authors. 
16. Implement functionality to add/edit/delete data related to surveys. 
17. Implement functionality to store surveys answers in the appropriate DB tables. 
18. Implement functionality to store social networks tokens. 
19. Implement functionality to purge social network activity history once in 90 days. 
20. Implement functionality to add/edit/delete data related to banners. 
21. Implement functionality to add/edit/delete data related to advertisement. 
22. Implement functionality to store data about users’ views of advertisements. 
23. Implement functionality to purge history of advertisement views once in 90 days. 
24. Implement functionality to add/edit/delete data related to comments. 
25. Implement functionality to add/edit/delete data related to reactions. 
26. Implement functionality to add/edit/delete data related to subscriptions. 
27. Implement functionality to add/edit/delete data related to partners. 

</details>

<details>
  <summary>3. Prepare usage metrics for web-portal analytics using operational DB:</summary>

1. Retrieve the number of views of each article and video per day/week/month. 
2. Retrieve the number of comments for each article and video. 
3. Retrieve the number of shares for each article and video on social networks. 
4. Retrieve the ratio of positive to negative comments for each article. 
5. Retrieve the articles that have been published in the last 24 hours. 
6. Retrieve number of views of articles and videos per categories. 
7. Retrieve the number of replies for each comment of each article and video. 
8. Retrieve the percentage of users who shared publications on social media. 
9. Retrieve the percentage of users who have created an account but have never logged in. 
10. Retrieve information about how many new users sign up on website each week. 
11. Retrieve the number of comments left by each user. 
12. Retrieve duration of each session of each user on the website. 
13. Retrieve information about users who have logged in for more than 1 hour. 
14. Retrieve information about users’ preferable languages. 
15. Retrieve users who have not logged in to website in the last 30 days. 
16. Retrieve number of publications shared on social networks by each user. 
17. Retrieve total number of each publication shared on social networks. 
18. Retrieve number of articles and videos shares per each social network. 
19. Retrieve number of responses per survey. 
20. Retrieve number of surveys completed by each user. 
21. Retrieve number of advertisements’ views per day/week/month. 

</details>

<details>
  <summary>4. Implement non-functional requirements for operational DB:</summary>

1. Analyze query execution plans and optimize queries for better response time. 
2. Implement indexing strategies to enhance query performance. 
3. Fine-tune database configuration settings for optimal performance. 
4. Implement data archiving or purging mechanisms to manage data growth and optimize performance. 
5. Set up comprehensive monitoring for the database, including deadlocks, performance metrics, resource utilization, and workload patterns. 
6. Implement backup strategy. 
7. Implement role-based access control and user management. 
8. Identify sensitive data. 
9. Protect sensitive data with encryption a row-level security. 

</details>

# 4 Data Integration

Follow [this link](/db_requirements/data_integration/README.md) to review requirements for this section.

**In scope of those requirements, implement the next tasks:**

<details>
  <summary>1. Implement processing of partner’s data:</summary>

1. Create ETL workflow to process data from partner’s source. 
2. Create ETL workflow to migrate data from Raw DB to the Operational DB. 
3. Create error handling and alerting strategy for ETL solutions. 
4. Implement data quality checks and validation processes. 
5. Set up automatic execution of ETL processes according to schedules. 

</details>

# 5 Datawarehouse

Follow [this link](/db_requirements/datawarehouse/README.md) to review requirements for this section.

**In scope of those requirements, implement the next tasks:**

<details>
  <summary>1. Implement data warehouse solution:</summary>

1. Determine the appropriate architecture for the data warehouse, such as a star schema, snowflake schema, or hybrid approach. 
2. Define the dimensions, facts, and hierarchies that will structure the data warehouse. 
3. Create ERD for DWH according to the chosen architecture. 
4. Create DWH objects according to ERD. 
5. Design Slowly Changing Dimension (SCD) strategies. 
6. Design and implement the incremental load process to load only the changes since the last update. 
7. Develop the full load process to load the entire dataset from the source systems into the data warehouse when needed. 
8. Design and develop the ETL processes to extract data from source systems. 
9. Implement indexes strategy. 
10. Implement partitioning strategy. 

</details>
