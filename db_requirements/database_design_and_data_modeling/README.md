### Back to [Database Requirements](/db_requirements/content/README.md#2-database-design-and-data-modeling)

- [ Database Design and Data Modeling](#database-design-and-data-modeling)
  - [1 Overview](#1-overview)
  - [2 Required Entities](#2-required-entities)
  - [3 Entity Distribution Matrix](#3-entity-distribution-matrix)
  - [4 Data Types Requirements](#4-data-types-requirements)
  - [5 Normalization Requirements](#5-normalization-requirements)
  - [6 DB Constraints Requirements](#6-db-constraints-requirements)
  - [7 Naming Convention](#7-naming-convention)
  - [8 ERD and Data Dictionary Guidelines](#8-erd-and-data-dictionary-guidelines)

# Database Design and Data Modeling

## 1 Overview

This section provides an overview of the data modeling requirements for the sports hub portal project. The data modeling and database design will be critical to ensuring that the system is efficient, reliable, and scalable. The goal of this section is to provide a detailed description of the data to be stored in the system, the relationships between the entities, and the rules and constraints that will govern the database. In addition, it also includes a comprehensive naming convention for the databases, ensuring consistency and clarity throughout the project. Additionally, the system must support multilingual content, as articles, videos, and other types of data may be published in different languages. The data modeling must take this into account to ensure that the system can efficiently store and retrieve content in multiple languages. 

The project will utilize two databases: the Operational Database and the Raw Data Database. The Operational Database is the primary database used to store critical information for the sports hub portal project. It should store not only article-related data but also other essential data, including surveys, events, advertisements, and statistical data such as article or video views. Additionally, it should contain configuration and service-related tables, such as log tables, to ensure efficient and reliable system operation. 

On the other hand, the Raw Data Database should serve as a temporary storage for articles that are received from news partners but have not yet been approved by admin. This database will be less complex and streamlined compared to the Operational Database and will only contain the necessary tables and columns to store and manage raw data. Once the data has been approved, it will be transferred to the Operational Database for further use.

![Data flow diagram](/db_requirements/images/data_flow.png)

## 2 Required Entities

The following entities have been identified as the primary components that will be stored in the Operational Database for the sports hub portal project:

_**Article**:_ represents the articles published on the website, which may be available in different languages.
Each article contains a title, a body, categories, and metadata such as author, date of publication, and the user who added the video.

_**Video**:_ represents information related to the videos published on the website. This includes the video title, description, categories, author, URL, date of publication, and the user who added the video. Additionally, statistical information such as video views and user reactions (like/dislike) should be stored in the database. Accompanying information about the video may be available in different languages.

_**Category**:_ represents information related to the categories on the website. This includes categories for sports, leagues, and teams. Category names may be available in different languages. 

_**User**:_ represents information related to the users of the website. This includes user login information, user role, profile information, and user activity history on the website. 

_**Author**:_ represents information related to the authors of articles on the website. This includes author name, and user ID (if exists).

_**Partner**:_ represents information related to news partners. This includes partner name, API configuration, and articles received from partners.

_**Survey**:_ represents information related to surveys on the website. This includes survey title, description, questions, and response data.

_**Social Network Data**:_ represents information related to social network activities on articles and videos. This includes data on sharing and liking activities by users.

_**Event (banner)**:_ represents information related to upcoming sports events. This includes the event title, description, date and time, and location. This entity also includes banner images for events.

_**Advertisement**:_ represents information related to advertisements on the website. This includes the advertisement title, description, image, and click-through URL.

_**Comment**:_ responsible for storing comments left by users on articles, videos, and other comments. It should contain information such as the content of the comment, the author of the comment, the date/time it was posted, and the article/video or other comment it is associated with. 

_**Subscription**:_ responsible for storing information about user subscriptions to different categories of articles. This entity will be important for managing user preferences and delivering targeted content to users.


_**NOTE: There are special types of publications such as ‘Main Article’, ‘Breakdown News’, and ‘Photo Of The Day’, that must be considered when designing a database. Please, refer to the web application features document to get additional details about such kinds of entities.**_


Additionally, there must be entities created to store statistical information such as: 
  - article views
  - article status changes 
  - user reactions on the publications (like/dislike) 
  - advertisement views 
  - social network user activities on articles (sharing and reactions). 

In addition to the business-related entities required for the Sports Hub portal project, there is also a need for service entities that will be used to store configuration information, logs, and other system-related data. These entities may include tables for storing web portal configurations, system logs, user activity logs, error logs, and more. The information stored in these entities will be critical for monitoring and maintaining the system, as well as for troubleshooting issues that may arise. 

_**NOTE: The list of entities and their attributes provided above is not exhaustive and may be subject to extension based on normalization or other project requirements.**_


## 3 Entity Distribution Matrix

Entity           |      Raw Data DB     |   Operational DB
---------------- | -------------------- | -----------------
Articles |Y|Y|
Videos |N|Y|
Categories |Y|Y|
Users |Y|Y|
Authors |N|Y|
Partners |Y|Y|
Surveys |N|Y|
Social Network Data  |N|Y|
Events |N|Y|
Advertisements |N|Y|
Comments |N|Y|
Subscriptions |N|Y|
Statistical data |N|Y|

## 4 Data Types Requirements

When selecting data types for the sports hub portal database, it is important to consider not only the compatibility with the application and the data being stored but also the storage efficiency.
The chosen data types should be optimized to reduce the amount of storage space required while still maintaining data integrity and accuracy. 

## 5 Normalization Requirements

The sports hub portal project requires that the database is normalized up to the third normal form (3NF).
This means that each table in the database should have a primary key and that all non-key attributes should be dependent on the primary key. 

## 6 DB Constraints Requirements

The proper use of database constraints is essential to ensure data consistency and integrity in any web application. In the case of the Sports Hub Portal, where multiple entities are used to store various types of data, it is crucial to define and apply constraints correctly to avoid errors, inconsistencies, and other issues. Therefore, the following requirements are required for database constraints for the Sports Hub Portal:

	- Each record in each business entity should be uniquely identified. 
	- Referential integrity between tables should be enforced. 
	- All attributes that are essential for the entity to have a valid record shouldn’t allow NULL values. 
	- The values, which require validation before inserting into DB need to be validated. 
	- Use the DEFAULT constraint for columns that have default values, such as the CreatedAt and UpdatedAt columns in various tables. 
	- Use the CHECK constraint to validate the data entered into an attribute, such as ensuring that a user's age is greater than 18 or that the email is valid. 

## 7 Naming Convention

Naming conventions are important for consistency and clarity in database development. By using a consistent naming convention, we can easily identify and understand the purpose of different database objects such as tables, columns, and keys. In the case of the Sports Hub portal, we recommend using specific naming conventions for primary keys, tables, columns, stored procedures, views, user-defined functions, and triggers. Following these conventions will help ensure that the database is organized and easy to understand, even as it grows and becomes more complex: 

	- Use descriptive and meaningful names for tables, columns, and other database objects.
	- Tables should be named in singular form and use CamelCase. For example, the table for storing article view information can be named "ArticleView".
	- Columns should be named in singular form and use CamelCase. For example, the column for storing the user's first name can be named "FirstName".
	- Primary key columns should be named in the format of EntityName + ID, such as UserID.
	- Foreign key columns should be named using the name of the referenced table and "ID". For example, if the "User" table has a foreign key referencing the "Role" table, the foreign key column can be named "RoleID".
	- Stored procedures should be named as "sprActionEntity", where "Entity" is the name of the entity that the procedure is related to, and "Action" is the purpose of the procedure. For example, "sprInsertUser" or "sprUpdateArticle".
	- Views should be named as "vEntity", where "Entity" is the name of the entity that the view represents. For example, "vUser" or "vArticleComments".
	- User-defined functions should be named as "fnPurpose", where "purpose" is the function's purpose. For example, "fnGetUserFullName" or "fnCalculateArticleRating".
	- Triggers should be named as "trActionEntity", where "entity" is the name of the entity that the trigger is related to, and "action" is the purpose of the trigger. For example, "trDeleteUser" or "trUpdateArticle".
	- Avoid using reserved words as object names.

## 8 ERD and Data Dictionary Guidelines

This section outlines the requirements for the entity-relationship diagram (ERD) and data dictionary for the Sports Hub Portal database. By adhering to these requirements, the database design will be more maintainable, scalable, and understandable for all stakeholders involved in the development and management of the system: 

	- The ERD should include all the entities and relationships between them.
	- Each entity in the ERD should have a unique name that reflects the purpose of the entity.
	- Each attribute in the ERD should have a name that reflects the purpose of the attribute.
	- Each relationship in the ERD should be properly defined and labeled.
	- The ERD should follow the rules of normalization up to the 3rd Normal Form.
	- The data dictionary should contain a description of each entity and its attributes. 
	- The data dictionary should also contain information about the data type, length, and format for each attribute.
	- Each attribute in the data dictionary should be properly labeled and defined.
	- The data dictionary should contain information about any constraints applied to each attribute.
	- The data dictionary should be kept up to date with any changes made to the ERD or the database schema.
