### Back to [Database Requirements](/db_requirements/content/README.md#3-database-implementation)

- [ Database Implementation](#database-implementation)
  - [1 Functional Requirements](#1-functional-requirements)
  - [2 Non-Functional Requirements](#2-non-functional-requirements)

# Database Implementation

This section outlines the functional requirements for manipulating and managing data, including both business entities and service information such as logs and configurations.

## 1 Functional Requirements

### Article 

1. When an article is being added to the Sports Hub Portal, it should be stored in appropriate DB tables, including article metadata such as ID, author, categories (sport, league, team), date of publication, status, and user who added the article. The article’s title and content can be stored in different languages.
2. When an article is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including the article’s metadata.
3. When an article is deleted from the Sports Hub Portal, it should be deleted from DB, including article-related data, such as information about article views, comments, and user reactions. The fact of deletion should be captured in the log table.
4. When the ability to comment on a particular article is enabled in the Sports Hub Portal, appropriate changes should be captured by DB. 

### Video 

1. When a video is being added to the Sports Hub Portal, it should be stored in appropriate DB tables, including video metadata such as ID, author, URL, categories (sport, league, team), date of publication, status, and user who added the article. The video’s title and description can be stored in different languages. 
2. When video-related data is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including the video’s metadata.  
3. When the video is deleted from the Sports Hub Portal, it should be deleted from DB, including video-related data, such as information about video views, comments, user reactions, etc. The fact of deletion should be captured in the log table. 
4. When the ability to comment on a particular video is enabled in the Sports Hub Portal, appropriate changes should be captured by DB. 
5. When the ability to share a particular video is enabled in the Sports Hub Portal, appropriate changes should be captured by DB.

### Sport (as a category) 

1. When a sport is being added to the Sports Hub Portal, it should be stored in the appropriate DB table, including its metadata such as ID, and name.
2. When a sport is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including the sport’s metadata.
3. When sport is being deleted from the Sports Hub Portal, it should be deleted from DB, including sport-related data, such as leagues and teams. The fact of deletion should be captured in the log table. The article’s metadata related to deleted sports should be replaced with NULL values, as well as related league and team. 

### League (as a subcategory) 

1. When a league is being added to the Sports Hub Portal, it should be stored in the appropriate DB table, including its metadata such as ID, name, and sport ID it’s referred to. 
2. When the league is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including its metadata.  
3. When the league is being deleted from the Sports Hub Portal, it should be deleted from DB, including league-related data, such as teams. The fact of deletion should be captured in the log table. The article’s metadata related to the deleted league should be replaced with NULL values, as well as a related team. 

### Team

1. When a team is being added to the Sports Hub Portal, it should be stored in an appropriate DB table, including its metadata such as ID, name, as well as sport ID, and league ID it’s referred to. 
2. When a team is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including its metadata.
3. When a team is being deleted from the Sports Hub Portal, it should be deleted from DB. The fact of deletion should be captured in the log table. The article’s metadata related to the deleted team should be replaced with NULL values. 

### User 

1. When a new user is being added to the Sports Hub Portal, information about his user should be stored in appropriate DB tables. 
2. When user data is being updated in the Sports Hub Portal, appropriate changes should be captured by DB. 
3. When the user is being deleted from the Sports Hub Portal, it should be deleted from DB, including the data associated with this user, such as comments, article views, etc. 
4. All user activities within the platform, including login/logout events, page views, publication commenting, content creation and modification, and any other relevant actions should be tracked in a dedicated database table for easy querying and reporting. 
5. The system should be able to notify administrators of any suspicious or unusual user activity, such as multiple failed login attempts. 
6. The system should provide the ability to export user activity data in a common format, such as CSV or Excel, for further analysis or integration with other systems. 
7. The system should allow users to view their own activity history, including past logins, content creation and modification, and any other relevant actions. 
8. The user activity data should be purged once in 90 days to ensure that the database does not become too large and slow down the system's performance.
9. The system should provide appropriate access controls to ensure that only authorized users have access to user activity data. 

### Author 

1. When a new author is being added to the Sports Hub Portal, information about it should be stored in the appropriate DB table, including the author’s metadata such as ID, and user ID. 
2. When information about the author is being edited in the Sports Hub Portal, appropriate changes should be captured by DB.  
3. When the author is being deleted from the Sports Hub Portal, it should be deleted from DB. The fact of deletion should be captured in the log table. The article’s metadata related to the deleted author should be replaced with NULL values. 

### Survey 

1. When a new survey is being added to the Sports Hub Portal, information about it should be stored in appropriate DB tables, including the survey’s metadata such as ID, survey’s start and end dates, and ID of the user who created a survey. The survey can be stored in different languages.
2. When the answer to a particular survey is given by the user, it should be stored in a particular table, including metadata such as ID, answer date, and ID of the user who answered the survey question. 
3. When the survey is being edited in the Sports Hub Portal, appropriate changes should be captured by DB.  
4. When the survey is deleted from the Sports Hub Portal, it should be deleted from DB, including users' answers associated with the survey. The fact of deletion should be captured in the log table.

### Social Network Data 

1. When a user is being signed up to the Sports Hub Portal using a social network, a token should be stored in an appropriate DB table. 
2. When a user is using social networks to follow the Sports Hub Portal or viewing/sharing/liking its posts or videos, the information about such activities should be captured by DB. 
3. The user’s social network activity data should be purged once in 90 days to ensure that the database does not become too large and slow down the system’s performance. 

### Event (banner) 

1. When a new event is being added to the Sports Hub Portal, information about it should be stored in appropriate DB tables, including event metadata such as ID, categories (sport, league, team), date of event, status (active/inactive), event’s photo URL. The event can be stored in different languages. 
2. When event-related data is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including its metadata.  
3. When an event is being deleted from the Sports Hub Portal, it should be deleted from DB. The fact of deletion should be captured in the log table. 

### Advertisement 

1. When a new advertisement is being added to the Sports Hub Portal, information about it should be stored in appropriate DB tables, including its metadata such as ID, type, categories (sport, league, team) if applicable, status (active/inactive), URL, advertisement media. The advertisement can be stored in different languages. 
2. When advertisement-related data is being edited in the Sports Hub Portal, appropriate changes should be captured by DB, including its metadata.  
3. When the advertisement is being deleted from the Sports Hub Portal, it should be deleted from DB. The fact of deletion should be captured in the log table. 
4. When a user views the advertisement or clicks on it to follow the URL, the activity should be captured by DB. 
5. The history of advertisement views should be purged once in 90 days to ensure that the database does not become too large and slow down the system's performance. 

### Comment 

1. When a user is commenting on an article, video, or another comment on the Sports Hub Portal, information about this action should be stored in appropriate DB tables, including the comment’s content and its metadata such as ID, date when the comment was created, date when the comment was edited, ID of the user who put a comment. 
2. When a comment is being deleted from the Sports Hub Portal, it should be deleted from DB. The fact of deletion should be captured in the log table. 

### Reaction 

1. When a user likes or dislikes an article, video, or comments on the Sports Hub Portal, information about this action should be stored in appropriate DB tables, including its metadata such as ID, date when the reaction was made, ID of the user who reacted, type of publication which was liked/disliked. 
2. When a reaction is removed from the Sports Hub Portal, the data about it should be deleted from DB. The fact of deletion should be captured in the log table. 

### Subscription 

1. When a user subscribes to the news of Sports Hub Portal, information about this action should be stored in appropriate DB tables, including the type of subscription and its metadata such as ID, date when the subscription was created, date of subscription, and status (active/inactive). 

### Partner 

1. When a news partner is being added to the Sports Hub Portal, information about it should be stored in appropriate tables of Raw DB and Operational DB, including the partner’s metadata such as ID, and status (active/inactive). The partner’s data in Raw DB should be extended with API configuration details. 
2. When information about partners is being edited in the Sports Hub Portal, appropriate changes should be captured by Raw and Operational DBs.  
3. When the partner is being deleted from the Sports Hub Portal, it should be deleted from Raw and Operational DBs. The fact of deletion should be captured in the log table. The article’s metadata related to deleted partners should be replaced with NULL values.
4. Test Data Generation 
5. It is required to generate a test data set for the Sports Hub Portal that can be used for testing and development purposes. 
6. The test data set must include a representative amount of data for each entity type to facilitate efficient testing and debugging. 
7. For each entity type, the test data set must include a variety of data points to simulate different scenarios and usage patterns. 
8. For entities with fact data such as user activities, article/video views, etc., the test data set must contain a representative amount of data to simulate realistic usage patterns. 
9. The specific amount and distribution of test data for each entity will depend on the specific requirements and usage patterns of the Sports Hub Portal. 
10. To ensure data integrity, the test data set must include appropriate relationships and constraints between entities. 

### Usage Metrics Tracking 

It is required to gather statistical data for our sports web portal in order to better understand our users and their behaviors. This data will allow us to make informed decisions about how to improve the user experience and increase engagement with our site. To achieve this goal, we have identified several key metrics that we want to track and analyze, including usage patterns, user engagement, and content popularity. Here is the list of requirements for statistical gathering: 

1. We need to know which publications are the most popular among our users. 
2. We want to track the number of shares for each article and video on different social networks. 
3. We want to track the ratio of positive to negative comments for each article. 
4. We want to see which articles have been published in the last 24 hours. 
5. We want to understand which categories are generating the most interest among our readers, so we can focus our content strategy accordingly. 
6. We need to know which comments are generating the most replies, so we can engage with our users more effectively. 
7. We want to know the percentage of users who have read an article and then shared it on social media. 
8. We want to track the percentage of users who have created an account but have never logged in. 
9. We want to track which articles are generating the most comments, so we can focus on those topics in our content strategy. 
10. We want to know how many new users sign up on our website each week. 
11. We want to recognize our most active users by seeing who has made the most comments on our website. 
12. We want to understand how long our users typically stay logged in to our website, so we can optimize our session timeout settings. 
13. We need to track which users have logged in for more than 1 hour, so we can ensure their account security. 
14. We need to understand which languages our users prefer to use on our website, so we can optimize our localization strategy. 
15. We want to see which users have not logged in to our website in the last 30 days, so we can send them a reminder about the Sport Hub Portal 
16. We want to recognize our most active users on our social network by seeing who has posted the most content. 
17. We want to recognize the most popular social networks used to share articles and videos. 
18. We want to identify which posts are being shared the most, so we can tailor our content strategy accordingly. 
19. We need to know which survey questions are generating the most responses, so we can focus on those topics. 
20. We want to track which users are the most active in responding to surveys. 
21. We want to track which advertisements have the most views, so we can optimize our advertising strategy. 

## 2 Non-Functional Requirements

### Performance 

1. The database should have a response time of less than 1 second for common queries. 
2. The database should support at least 500 concurrent users without significant performance degradation. 
3. The database should be designed to handle at least 1 million records without any significant performance degradation. 
4. The database should have a read throughput of at least 1000 queries per second. 
5. The database should be designed to prevent deadlocks by using appropriate locking mechanisms, such as row-level locking or snapshot isolation. 
6. The database should be monitored for deadlocks, and any occurrences should be logged and investigated to identify the root cause. 

### Scalability 

1. The database should be able to handle at least a 50% increase in data volume or user traffic without any significant performance degradation. 
2. The database should be designed to scale horizontally by adding additional nodes or clusters as necessary. 
3. The database should be designed to support vertical scaling by adding additional hardware resources as necessary. 

### Backup and Recovery 

1. The database should be backed up every day at midnight using a full backup. Differential backups should be done every 6 hours during business hours (9 AM to 5 PM) to reduce the amount of time required for a restore operation. 
2. The recovery process should include the ability to restore data to a point in time up to 1 hour before a failure occurs. 
3. The backup and recovery process should be documented and kept up-to-date, and the documentation should be stored in a secure location. 

### Security 

1. All sensitive user data in the database, such as passwords, should be encrypted using industry-standard encryption algorithms. 
2. Access to sensitive data should be restricted to authorized personnel only, and user accounts should be set up with the principle of least privilege in mind. 
3. The database should be designed with security in mind, using techniques such as data masking, row-level security, and encrypted connections. 
