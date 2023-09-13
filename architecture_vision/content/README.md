### Back to [Sports Hub portal product map](../../README.md#sports-hub-portal)

- [1 Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Scope](#12-scope)
- [2 Executive Summary](#2-executive-summary)
  - [2.1 Key Decisions](#21-key-decisions)
  - [2.2 Key Risks and Open Issues](#22-key-risks-and-open-issues)
- [3 Architectural Drivers](#3-architectural-drivers)
  - [3.1 Business Case](#31-business-case)
    - [3.1.1 Business Goals](#311-business-goals)
    - [3.1.2 Major Features](#312-major-features)
  - [3.2 Design Constraints](#32-design-constraints)
  - [3.3 Quality Attribute Scenarios](#33-quality-attribute-scenarios)
- [4 Solution Architecture](#4-solution-architecture)
  - [4.1 Big Picture](#41-big-picture)
  - [4.2 Solution Decomposition – Basic Complexity](#42-solution-decomposition--basic-complexity)
  - [4.3 Solution Decomposition – Medium Complexity](#43-solution-decomposition--medium-complexity)
  - [4.4 Solution Decomposition – Hard Complexity](#44-solution-decomposition--hard-complexity)
  - [4.5 Development Technology Stack](#45-development-technology-stack)
- [5 Operation Plan](#5-operation-plan)
- [6 Database Diagrams](#6-database-diagrams)

# 1 Introduction

## 1.1 Purpose

This Architecture Vision elicits the significant architecture drivers such as business, functional, nonfunctional requirements and constraints, defines architecture, and develops a roadmap for Single Entry implementation. The document is intended as a primary technical guidance into solution implementation for the development team.

## 1.2 Scope

The document describes the proposed Single Entry architecture towards development of the solution that will satisfy business, functional, non-functional requirements and constraints provided by the Client. This Architecture Vision covers the following information:

- Significant architectural drivers for the Solution
- Proposed software architecture of the solution based on these drivers
- Technology stack and environment definitions
- Operations specific perspectives
- Development road map and high level estimates for effort, team size and skill sets.

# 2 Executive Summary

The section Executive Summary highlights key architectural decisions made for the solution described in [3.1 Business Case](#31-business-case). These decisions are defined and discussed in depth in [4 Solution Architecture](#4-solution-architecture) while Implementation Roadmap lays out the proposed milestones, estimates, and team to implement the provided architecture vision.
This section also summarizes the key business and technical risks related to the solution implementation. These risks are uncovered in depth in the rest of the document.

## 2.1 Key decisions

The section outlines key design decisions about the solution including the architecture big picture and most essential technologies and external services to rely on.
The solution will be implemented as a cloud based web service and deployed to the Cloud Platform Provider (GCP, Azure, AWS) using it’s managed services capabilities. The structured data will be stored in the scalable cloud RDBMS storage provided by the Cloud Platform Provider with multy-AZ replication to ensure data availability and backup as required by the solution’s SLA. The solution will be integrated as a REST-ful client with the third-party service New Aggregator to get news and store it the local datastorages.

## 2.2 Key risks and open issues

The section lists the key risks related to the solution design and implementation. It also lists key open issues where architectural decisions have not been made yet or are likely to change.

Risk description|Mitigation strategy|
--------------- | ----------------- |
There is a risk of failure of news aggregator, but it should now affect end users on our portal|Store all the data within platform instead of linking to original sources|


# 3 Architectural Drivers

The section captures significant requirements driving the solution architecture and road map. The requirements which are not influencing the solution architecture are typically excluded from this section and can be found in the product backlogs.

## 3.1 Business Case

The section lays out the business case for the solution Sports Hub Portal.

![Business level view of Sports Hub Portal](/architecture_vision/images/figure_1_business_level_view.png)

<p align="center"><i>Figure 1. Business level view of Sports Hub Portal</i></p>

The solution will enable the users to review all news using web/mobile devices, manage news preferencese, subsribe to interested topics & receive the newsletters on regular bases. The solution will be deployed on the GPC/AWS/Azure cloud as web application.

### 3.1.1 Business Goals

The section enumerates essential business goals for the solution

#|Description|
--------------- | ----------------- |
BG-1|Create sports news platform to provide more flexibility to users: newsletters subsriptions, news personalizations, news review using web/mobile devices|

### 3.1.2 Major Features

The section enumerates solution major features.

#|Description|
--------------- | ----------------- |
F-1|Endusers can read news related to different kinds of sports|
F-2|Endusers can subscribe to the sports news of their choice|
F-3|Endusers can receive the newsletters via email|
F-4|Endusers can manage the kind of news they want to see (e.g. news related to the specific kind of sports,league or team)|
F-5|Admins can define/modify the structure and content of the portal|

## 3.2 Design Constraints

The section lists the constraints accounted for in the designed solution.

#|Description|
--------------- | ----------------- |
CON-1|A minimum of 1000 simultanious users must be supported|
CON-2|Solution should be cloud agnostic as much as possible to simplify migration to another cloud provider|
CON-3|The application must work in all modern browsers|
CON-4|The application should be built following the REST principles|
CON-5|The application should use Cloud service for storing images and video files instead of previewing this data from original news aggregator|

## 3.3 Quality Attribute Scenarios

A Quality Attribute Scenario is an unambiguous and testable requirement for one or more Solution Quality Attributes such as Performance, Usability, Maintainability and others. This section lists and prioritizes the scenarios pertinent to the designed solution.

#|QA|Scenario|Priority|
--|--|--------|--------|
QA-1|Security|Credentials always entered by the user during log-in are transferred to the server over encrypted, secure channel without the chance of sniffing by third party.|H|
QA-2|Performance|UI max response time (includes API endpoints max response time) < 10 sec|M|
QA-3|Performance|UI average response time (Includes API endpoints average response time) < 3 sec|M|
QA-4|Performance|Application first Page upload time < 2 SEC|M|
QA-5|Scalability|Application should support at least 100 simultaneous  users at same time |M|
QA-6|Compatibility|Solution co-exists and interoperates with the existing news providers.|H|
QA-7|Security|Audit events & logs: should always provide info about what has happened, who did it and when & retention policy for that data should be 365days|M|
QA-8|Availability|Solution should be available 95% of total hours|H|


# 4 Solution Architecture

The section Solution Architecture is primary for the Architecture Vision document. It defines and reasons about the solution architecture design based on the architecturally significant requirements and constraints identified in the section [3 Architectural Drivers](#3-architectural-drivers).

## 4.1 Big Picture

The section includes a list of architectural views covering the designed solution along with the context it runs in on the high level.
The view defines the primary solution components collaborating with the external systems and services. It is driven by the [3.1 Business Case](#31-business-case).

![Solution Context](/architecture_vision/images/figure_2_solution_context.png)

<p align="center"><i>Figure 2. Solution Context</i></p>

Table of annotated elements:

Name|Description|
--------------- | ----------------- |
Sports News Solution|Responsible for implementation of all business logic|
Identity Provider|Responsible for authentication functionality|
Cloud Provider|Responsible for hosting of deployed solution|
Email Provider|Responsible for newsletters mailing|
Push Notifications|Responsible for push notification functionality|
News Aggregator|Responsible for providing content to portal|

## 4.2 Solution Decomposition – Basic Complexity

The view defines the runtime decomposition of the server-side part of the solution. It is driven by the [3.1 Business Case](#31-business-case) and the architecture best practices applicable to the cloud-based applications. The view context is defined by the view [4.1.1 Solution Context](#411-solution-context) where this section represents decomposition of Cloud Based Solution component.

![Basic Cloud Solution Decomposition](/architecture_vision/images/figure_3_basic_cloud_solution.jpg)

<p align="center"><i>Figure 3. Basic Cloud Solution Decomposition</i></p>

The solution is decomposed into several parts documented below combining several standard architectural patterns.

#|Description|
--------------- | ----------------- |
Portal UI|Responsible for Web UI representation of solution|
Desktop App|Responsible for desktop representation of solution for admins|
Mobile App|Hybrid application, responsible for Mobile representation of solution|
Static Files|Responsible for storage of unstructured data e.g. images, video etc|
Portal API|Responsible for business logic related to communication with frontend and database|
Operational DB|Responsible for storage of all structured info: users & their details, news, configurations info etc|
RawData|Responsible for storage of all nonprocessed data|
PushNotification Sender|Responsible for push notification functionality|
Mail Sender|Responsible for send emails logic|
Identity Provider|Responsible for authenticatino of users using social networks|
News Aggregator|Responsible for news provisionining|
News Processor|Responsible for moving ready news to Operational DB|

## 4.3 Solution Decomposition – Medium Complexity

The view defines the runtime decomposition of the server-side part of the solution. It is driven by the [3.1 Business Case](#31-business-case) and the architecture best practices applicable to the cloud-based applications. The view context is defined by the view [4.1.1 Solution Context](#411-solution-context) where this section represents decomposition of Cloud Based Solution component.

![Medium Cloud Solution Decomposition](/architecture_vision/images/figure_4_basic_cloud_solution.jpg)

<p align="center"><i>Figure 4. Medium Cloud Solution Decomposition</i></p>

The cloud based part of the solution is decomposed into several parts documented below combining several standard architectural patterns.

#|Description|
--------------- | ----------------- |
Portal UI|Responsible for Web UI representation of solution|
Mobile App|Hybrid application, responsible for Mobile representation of solution|
Desktop App|Responsible for desktop representation of solution for admins|
Static Files|Responsible for storage of unstructured data e.g. images, video etc|
Portal API|Responsible for business logic related to communication with frontend and database|
Notification Service|Responsible for encapsulation of logic related to push notifications. Service might have a few different implementation which depends on each push notification provider|
Mail Service|Responsible for encapsulation of logic related to emails. Service might have a few different implementation which depends on each mail provider|
Auth Service|Responsible for encapsulation of logic related to users authentication|
Operational DB|Responsible for storage of all structured info: users & their details, news, configurations info etc|
RawData|Responsible for storage of all nonprocessed data|
Cache DB|Responsible for caching logic for data which are accessed frequently|
Search Engine|Responsible for optimization and preparation of data in format which is suitable for search and indexes related tasks|
PushNotification Sender|Responsible for push notification functionality|
Mail Sender|Responsible for send emails logic|
Identity Provider|Responsible for authenticatino of users using social networks|
News Aggregator|Responsible for news provisionining|
News Processor|Responsible for moving ready news to Operational DB|

## 4.4 Solution Decomposition – Hard Complexity

The view defines the runtime decomposition of the server-side part of the solution. It is driven by the [3.1 Business Case](#31-business-case) and the architecture best practices applicable to the cloud-based applications. The view context is defined by the view [4.1.1 Solution Context](#411-solution-context) where this section represents decomposition of Cloud Based Solution component

![Hard Cloud Solution Decomposition](/architecture_vision/images/figure_5_basic_cloud_solution.png)

<p align="center"><i>Figure 5. Hard Cloud Solution Decomposition</i></p>

The cloud based part of the solution is decomposed into several parts documented below combining several standard architectural patterns.

#|Description|
--------------- | ----------------- |
Portal UI|Responsible for Web UI representation of solution|
Mobile App|Hybrid application, responsible for Mobile representation of solution|
Desktop App|Responsible for desktop representation of solution for admins|
Static Files|Responsible for storage of unstructured data e.g. images, video etc|
CDN|Responsible for edge caching of UI assets to improve performance|
API Management|Responsible for API management and versionining within solution|
Portal API|Responsible for business logic related to communication with frontend and database|
Sockets|Responsible for two way communication with end users devices|
Queue|Responsible for communication between news injector and sockets|
Notification Service|Responsible for encapsulation of logic related to push notifications. Service might have a few different implementation which depends on each push notification provider|
Mail Service|Responsible for encapsulation of logic related to emails. Service might have a few different implementation which depends on each mail provider|
Auth Service|Responsible for encapsulation of logic related to users authentication|
Operational DB|Responsible for storage of all structured info: users & their details, news, configurations info etc|
RawData|Responsible for storage of all nonprocessed data|
Cache DB|Responsible for caching logic for data which are accessed frequently|
Search Engine|Responsible for optimization and preparation of data in format which is suitable for search and indexes related tasks|
PushNotification Sender|Responsible for push notification functionality|
Mail Sender|Responsible for send emails logic|
Identity Provider|Responsible for authenticatino of users using social networks|
News Aggregator|Responsible for news provisionining|
News Processor|Responsible for moving ready news to Operational DB|


## 4.5 Development Technology Stack

Technology stack may vary on your choice:

Name|Version|Description
--------------- | ----------------- | -----|
Framework1|x.x|Responsible for a, b, c|
Library2|3.0-RC1|Responsible for a, b, c|
Library3|x.x.x.x|Responsible for a, b, c|
<name>|<version>|<description and responsibilities>|


# 5 Operation Plan

<ins><b>Infrastructure GCP:</b></ins> GCP is used as main and single cloud provider. Services that is used by solution are App Engine, Cloud Storage, Cloud Functions, Cloud SQL for MySQL, Memorystore, Cloud BigQuery, Stackdrive, Cloud Pub/Sub, Cloud Scheduler, Cloud CDN.

![Dedployment Diagram GCP - basic complexity](/architecture_vision/images/gcp_basic.png)

<p align="center"><i>Figure 6. Dedployment Diagram GCP - basic complexity</i></p>

![Dedployment Diagram GCP - medium complexity](/architecture_vision/images/gcp_medium.png)

<p align="center"><i>Figure 7. Dedployment Diagram GCP - medium complexity</i></p>

![Dedployment Diagram GCP - hard complexity](/architecture_vision/images/gcp_hard.png)

<p align="center"><i>Figure 8. Dedployment Diagram GCP - hard complexity</i></p>


<ins><b>Infrastructure Azure:</b></ins> Azure is used as main and single cloud provider. Services that is used by solution are WebApps, Azure CDN, Azure Storage, Azure Functions, Azure SQL, Azure Cognitive Search, Azure Redis, Azure Scheduler. Azure Service Bus.

![Dedployment Diagram Azure - basic complexity](/architecture_vision/images/azure_basic.png)

<p align="center"><i>Figure 9. Dedployment Diagram Azure - basic complexity</i></p>

![Dedployment Diagram Azure - medium complexity](/architecture_vision/images/azure_medium.png)

<p align="center"><i>Figure 10. Dedployment Diagram Azure - medium complexity</i></p>

![Dedployment Diagram Azure - hard complexity](/architecture_vision/images/azure_hard.png)

<p align="center"><i>Figure 11. Dedployment Diagram Azure - hard complexity</i></p>


<ins><b>Infrastructure AWS:</b></ins> AWS is used as main and single cloud provider. Services that is used by solution are Elastic Beanstalk, AWS Lambdas, AWS S3, Elasticsearch, Amazon SQS, AWS Batch Scheduler, AWS ElastiCache, Amazon RDS, Amazon CloudFront, AWS API Gateway.

![Dedployment Diagram AWS - basic complexity](/architecture_vision/images/aws_basic.png)

<p align="center"><i>Figure 12. Dedployment Diagram AWS - basic complexity</i></p>

![Dedployment Diagram AWS - medium complexity](/architecture_vision/images/aws_medium.png)

<p align="center"><i>Figure 13. Dedployment Diagram AWS - medium complexity</i></p>

![Dedployment Diagram AWS - hard complexity](/architecture_vision/images/aws_hard.png)

<p align="center"><i>Figure 14. Dedployment Diagram AWS - hard complexity</i></p>



<ins><b>Environments:</b></ins> For transitional phase there will be four environments: development, testing, staging and production. Development environment use minimal cloud resources but similar architecture. Testing environment use intermediate resource allocation for full QA testing. Staging environment is a copy of production environment and is used for load, performance and user acceptance testing. Production environment is scalable and fault tolerant.


# 6 Database Diagrams

![Operational DB](/architecture_vision/images/OperationalDB_ERD.png)

<p align="center"><i>Figure 15. Operational DB</i></p>

![RawData DB](/architecture_vision/images/RawDB_ERD.png)

<p align="center"><i>Figure 16. RawData DB</i></p>

<details>
  <summary>Database ERD Anotation:</summary>

### [Article]

Stores information on articles that have been posted on the portal.

Attribute        |      Description
---------------- | --------------------
ArticleID | Record identifier
LanguageID | Refers to language in [Language] table. The article can be stored in different languages
Title | Article title name
Headline | Article headline
Content | The body of article

### [ArticleDetail]

Contains additional article details.

Attribute        |      Description
---------------- | --------------------
ArticleDetailID | Record identifier
ArticleID | Refers to article in [Article] table
ArticleType | Represents article type (Lifestyle, Dealbook)
AuthorID | Refers to the author of the article in [Author] table
PartnerID | If article was provided by partner, the value refers to the partner name in [Partner] table
SportID | Refers to the first level of article categorization in [Sport] table
LeagueID | Refers to the second level of article categorization in [League] table
TeamID | Refers to the third level of article categorization in [Team] table
LocationID | Refers to the location in [Location] table
StatusID | Refers to the status of article (Published, Pending, etc.) in [Status] table
CommentsOn | Indicates if comments are allowed for the article
CreatedAt | Indicates date and time when article was added
CreatedBy | Refers to the user in [User] table, who added article

### [ArticleView]  

Stores information about the number of times that individual users have viewed particular articles. 

Attribute        |      Description
---------------- | --------------------
ArticleViewID | Unique record identifier
ArticleID | Refers to article in [Article] table
UserID | Refers to the user in [User] table, who viewed the article
ViewDate | Indicates date and time when user viewed the article

### [MainArticle] 

Stores configuration of ‘Main article’ publications. 

Attribute        |      Description
---------------- | --------------------
MainArticleID | Unique record identifier
ArticleID | Refers to article in [Article] table
IsActive | Indicates if article is shown on the main page
CreatedAt | Indicates date and time when configuration was created
Created By | Refers to the user in [User] table, who configured main articles

### [Sport]  

Contains information about the first level of article categorization. 

Attribute        |      Description
---------------- | --------------------
SportID | Unique record identifier
SportName | Category (sport) name
LanguageID | Refers to language in [Language] table. Category (sport) name can be stored in different languages

### [League]  

Contains information about the second level of article categorization (sub-category). 

Attribute        |      Description
---------------- | --------------------
LeagueID | Unique record identifier
LeagueName | Sub-category (league) name
SportID | Refers to sport in [Sport] table, which league belongs to
LanguageID | Refers to language in [Language] table. Sub-category (league) name can be stored in different languages

### [Team]  

Contains information about the third level of article categorization (sub-category). 

Attribute        |      Description
---------------- | --------------------
TeamID | Unique record identifier
TeamName | Sub-category (team) name
LeagueID | Refers to league in [League] table, which team belongs to
SportID | Refers to sport in [Sport] table, which team belongs to
LocationID | Refers to location in [Location] table, which team is located in
LanguageID | Refers to language in [Language] table. Sub-category (team) name can be stored in different languages

### [BreakdownNews]  

Stores data on the breakdown news setup, indicating which categories and subcategories are selected for display. 

Attribute        |      Description
---------------- | --------------------
BreakdownNewsID | Unique record identifier
SportID | Refers to sport (category) in [Sport] table
LeagueID | Refers to league (sub-category) in [League] table
TeamID | Refers to team (sub-category) in [Team] table
IsActive | Indicates if breakdown news configuration is enabled
CreatedAt | Indicates date and time when breakdown news configuration was created
CreatedBy | Refers to the user in [User] table, who configured breakdown news

### [Partner]  

Stores basic information about partners who provide articles. More detailed information about partners is stored in RawDB. 

Attribute        |      Description
---------------- | --------------------
PartnerID | Unique record identifier
PartnerName | Represents partner name

### [Video]  

Contains information about video publications posted in the portal. 

Attribute        |      Description
---------------- | --------------------
VideoID | Record identifier
LanguageID | Refers to language in [Language] table. The video title and description can be stored in different languages
Title | Video title name
Description | Video description

### [VideoDetail]  

Contains additional details on video publication. 

Attribute        |      Description
---------------- | --------------------
VideoDetailID | Record identifier
VideoID | Refers to video in [Video] table
AuthorID | Refers to the author of the video in [Author] table
CommentsOn | Indicates if comments are allowed for the video
SharingOn | Indicates if video is allowed to be shared in social networks
CreatedAt | Represents date and time when video was added
CreatedBy | Refers to the user in User table, who added video

### [MediaFile]  

Contains information about media files (photos, videos) that are used on the portal. 

Attribute        |      Description
---------------- | --------------------
MediaFileID | Record identifier
ArticleID | Refers to article where media file is used
PhotoOfTheDayID | Refers to ‘Photo of the day’ publication in [PhotoOfTheDay] table where media file is used
VideoID | Refers to video publication in [Video] table where media file is used
AdID | Refers to advertisement in [Advertisement] table where media file is used
EventID | Refers to event (banner) in [Banner] table where media file is used
MediaFileURL | Stores URL of media file
CreatedAt | Indicates date and time when media file was created
CreatedBy | Refers to the user in User table, who added media file

### [Banner]  

Stores information about banners (events) that are displayed on the portal. 

Attribute        |      Description
---------------- | --------------------
BannerID | Record identifier
LanguageID | Refers to language in [Language] table. The banner name and description can be stored in different languages
Name | Banner title name
Description | Banner description

### [BannerDetail]  

Contains additional details on banner (event). 

Attribute        |      Description
---------------- | --------------------
BannerDetailID | Record identifier
BannerID | Refers to banner in [Banner] table
EventDate | Displays the event date
SportID | Refers to sport (category) in [Sport] table which the event is related to
LeagueID | Refers to league (sub-category) in [League] table which the event is related to
TeamID | Refers to team (sub-category) in Team table which the event is related to
IsActive | Indicates if event is active
CreatedAt | Indicates date and time when event was added
CreatedBy | Refers to the user in [User] table, who added event

### [Advertisement]  

Stores information about advertisement on the portal. 

Attribute        |      Description
---------------- | --------------------
AdID | Record identifier
LanguageID | Refers to language in [Language] table. Advertisement can be stored in different languages
Title | Advertisement title
ContentURL | URL to the website of advertiser

### [AdvertisementDetail]  

Stores additional information on advertisement. 

Attribute        |      Description
---------------- | --------------------
AdDetailID | Record identifier
AdID | Refers to advertisement in [Advertisement] table
IsActive | Represents if advertisement is active
CreatedAt | Represents date and time when advertisement was added
CreatedBy | Refers to the user in User table, who added advertisement

### [AdvertisementCategory]  

Stores information about categories that advertisement is assigned to. 

Attribute        |      Description
---------------- | --------------------
AdCategoryID | Record identifier
AdID | Refers to advertisement in [Advertisement] table
LeagueID | Refers to league (sub-category) in [League] table which advertisement belongs to

### [AdvertisementActivity]  

Contains data related to advertisement activities, including information on when ads were viewed or opened. 

Attribute        |      Description
---------------- | --------------------
AdActivityID | Record identifier
AdID | Refers to advertisement in [Advertisement] table
ActivityType | Indicates activity types (‘Opened’, ‘Displayed’)
ActivityDate | Indicates date and time when activity occurred

### [Language]  

Stores information about languages that are used on the portal. 

Attribute        |      Description
---------------- | --------------------
LanguageID | Record identifier
Language | Language name
IsDefault | Indicates default language on the portal
IsActive | Represents if language is active

### [PhotoOfTheDay]  

Stores information about ‘Photo of the day’ publications. 

Attribute        |      Description
---------------- | --------------------
PhotoOfTheDayID | Record identifier
LanguageID | Refers to language in [Language] table. Title, description and alternative text can be stored in different languages
Title | Title of publication
Description | Description of publication
AlternativeText | Alternative text of publication

### [PhotoOfTheDayDetail]  

Stores additional information about ‘Photo of the day’ publications. 

Attribute        |      Description
---------------- | --------------------
PhotoOfTheDayDetailID | Record identifier
PhotoOfTheDayID | Refers to publication in [PhotoOfTheDay] table
AuthorID | Refers to the author of publication in [Author] table
IsActive | Indicates if publication is active
CreatedAt | Represents date and time when publication was added
CreatedBy | Refers to the user in [User] table, who added publication

### [Status]  

Keeps track of the status history of articles, videos, and surveys. The corresponding ID for each type of content is recorded in the table when its status is changed. 

Attribute        |      Description
---------------- | --------------------
StatusID | Record identifier
ArticleID | Refers to article in [Article] table
VideoID | Refers to video in [Video] table
SurveyID | Refers to survey in [Survey] table
StatusDescID | Refers to status description in [StatusDecription] table
StatusDate | Indicates date and time when status was changed

### [StatusDescription]  

Stores list of statuses for each type of publication (article, video, survey). 

Attribute        |      Description
---------------- | --------------------
StatusDescID | Record identifier
PublicationType | Type of publication (article, video, survey)
StatusDesc | Status description (e.g. ‘Pending’, ‘Published’, etc.)

### [Comment]  

Stores information about comments that users left on articles and other comments. 

Attribute        |      Description
---------------- | --------------------
CommentID | Record identifier
ArticleID | Refers to the articles in the [Article] table on which a comment was posted
ReplyToCommentID | If a comment was left on another comment, this refers to the CommentID within the current table
UserID | Refers to user in [User] table, who posted the comment
Comment | Text of the comment
CreatedAt | Indicates a date and time when comment was left

### [Reaction]  

Stores information on user reactions such as likes and dislikes, which are associated with both articles and comments. 

Attribute        |      Description
---------------- | --------------------
ReactionID | Record identifier
ArticleID | Refers to articles in [Article] table on which the reaction was left
VideoID | Refers to video in [Video] table on which the reaction was left
CommentID | Refers to comment in [Comment] table on which the reaction was left
UserID | Refers to user in [User] table, who left the reaction
ReactionType | Represents reaction type (like, dislike)
ReactionDate | Indicates a date and time when reaction was left

### [Survey]  

Stores information about surveys on the portal. 

Attribute        |      Description
---------------- | --------------------
SurveyID | Record identifier
LanguageID | Refers to language in [Language] table. Title can be stored in different languages
Title | Survey’s title
CreatedAt | Indicates a date and time when survey was created
CreatedBy | Refers to the user in [User] table, who added survey
StartDate | Indicates the date when survey starts
EndDate | Indicates the date when survey ends

### [SurveyOption]  

Stores information about answer options for each survey. 

Attribute        |      Description
---------------- | --------------------
OptionID | Record identifier
LanguageID | Refers to language in [Language] table. Options can be stored in different languages
SurveyID | Refers to survey in [Survey] table that option belongs to
OptionDesc | Text of the option

### [SurveyAnswer]  

Stores user answers on the surveys.  

Attribute        |      Description
---------------- | --------------------
AnswerID | Record identifier
SurveyID | Refers to the survey within the [Survey] table to which a given answer belongs
UserID | Refers to the user in [User] table, who answered to survey
OptionID | Refers to the option within the [SurveyOption] table that was selected by the user
AnswerDate | Indicates date and time when answer was given

### [SocialNetwork]  

Contains list of social networks. 

Attribute        |      Description
---------------- | --------------------
SocialNetworkID | Record identifier
Name | Name of social network

### [SocialNetworkActivityType]  

Lists the various social network activities that are available on the portal, such as sharing, following, and logging. 

Attribute        |      Description
---------------- | --------------------
ActivityTypeID | Record identifier
ActivityType | Type of activity (e.g. sharing, following, logging)
SocialNetworkID | Refers to social network in [SocialNetwork] table
IsActive | Indicates if activity is enabled on the portal

### [SocialNetworkActivity]  

Contains information on social network activities that have occurred on the portal, such as article and video sharing, user logging, and following. 

Attribute        |      Description
---------------- | --------------------
SocialNetworkActivityID | Record identifier
ActivityTypeID | Type of activity (logging, sharing, following)
SocialNetworkID | Refers to social network in [SocialNetwork] table
UserID | Refers to the user in [User] table, who performed an action
ArticleID | Refers to articles in [Article] table on which the action was performed
VideoID | Refers to video in [Video] table on which the action was performed
ActivityDate | Indicate a date and time when action was performed

### [SocialNetworkToken]  

Stores information about token that are used for logging user to the portal using social networks. 

Attribute        |      Description
---------------- | --------------------
TokenID | Record identifier
UserID | Refers to the user in the [User] table to whom a given token belongs
SocialNetworkID | Refers to social network in [SocialNetwork] table to which given token belongs
Token | Token string
CreatedAt | Indicates a date and time when token was created

### [User]  

Stores information about users on the portal. 

Attribute        |      Description
---------------- | --------------------
UserID | Record identifier
Username | Unique username
RoleID | Refers to user role in [Role] table
FirstName | First name of user
LastName | Last name of user
LocationID | Refers to location in [Location] table, where user is based
Email | User’s email
EncryptedPassword | Encrypted password which is used to log in to portal
RegistrationDate | Indicates data and time when user was registered on the portal
LanguageID | Indicate user’s preferred language
IsActive | Indicates if user is active

### [UserActivity]  

Stores information about the sessions of users on the portal. 

Attribute        |      Description
---------------- | --------------------
SessionID | Record identifier
UserID | Refers to the user in the [User] table to whom a given session belongs
StartDate | Indicates a date and time when session started
EndDate | Indicates a date and time when session ended
IPAddress | IP address of device which user used to log in

### [UserRole]  

Stores list of user roles on the portal. 

Attribute        |      Description
---------------- | --------------------
RoleId | Record identifier
RoleName | Role name
RoleDescription | Role description

### [Author]  

Stores information about authors of publications. 

Attribute        |      Description
---------------- | --------------------
AuthorID | Record identifier
UserID | Refers to user in [User] table if author of publication is a registered user
Name | Author’s name

### [Subscription]  

Stores information about users subscription on the portal. 

Attribute        |      Description
---------------- | --------------------
SubscriptionID | Record identifier
UserID | Refers to user in [User] table who subscribed to the news
SportID | If user is subscribed to the news about some sport, the attribute refers to this sport in [Sport] table
LeagueID | If user is subscribed to the news about some league, the attribute refers to this league in [League] table
TeamID | If user is subscribed to the news about some team, the attribute refers to this team in [Team] table
HomePage | Indicates if user is subscribed to the Home page
IsActive | Indicates if subscription is active
CreatedAt | Indicates a date and time when subscription was created

### [Location]  

Stores information about physical locations. 

Attribute        |      Description
---------------- | --------------------
LocationID | Record identifier
LocationName | Name of location
CityID | Refers to a city in [City] table to which location belongs
StateID | Refers to a state in [State] table to which location belongs
CountryID | Refers to a country in [Country] table to which location belongs
PostalCode | Postal code of the location
Latitude | Latitude of location
Longitude | Longitude of location

### [City]  

Stores list of cities. 

Attribute        |      Description
---------------- | --------------------
CityID | Record identifier
CityName | Name of the city

### [State]  

Stores list of states. 

Attribute        |      Description
---------------- | --------------------
StateID | Record identifier
StateName | Name of the state

### [Country]  

Stores list of countries. 

Attribute        |      Description
---------------- | --------------------
CountryID | Record identifier
CountryName | Name of the country

### [TeamHub]  

Stores information about team hubs assigned to a user.  

Attribute        |      Description
---------------- | --------------------
HubID | Record identifier
UserID | Refers to user in [User] table to whom hub is assigned

### [TeamHubDetail]  

Stores information about teams assigned to a hub.  

Attribute        |      Description
---------------- | --------------------
HubID | Hub identifier
TeamID | Refers to a team in [Team] table which belongs to a hub

### [FooterTab]  

Contains information about footer sections, such as ‘Company Info’, ‘Contributors’, ‘Newsletter’. 

Attribute        |      Description
---------------- | --------------------
FooterTabID | Record identifier
Tab | Tab name (Company Info’, ‘Contributors’, ‘Newsletter’)
LanguageID | Refers to language in [Language] table. Section names can be stored in different languages
IsActive | Indicates if section is enabled
IsDeletable | Indicates if section can be deleted by admin

### [FooterPage]  

Stores information about footer menus, such as ‘About Sport Hub’, ‘News/In the press’, ‘Contact Us’, etc. 

Attribute        |      Description
---------------- | --------------------
FooterPageID | Record identifier
Page | Page name (‘About Sport Hub’, ‘News/In the press’, ‘Contact Us’, etc.)
FooterTabID | Refers to tab in [FooterTab] table, which menu belongs to
Content | Content of the section, if it’s possible to store as a single value (for example, ‘About Sport Hub’)
LanguageID | Refers to language in [Language] table. Menu names and description can be stored in different languages
IsActive | Indicates if menu is enabled
IsDeletable | Indicates if menu can be deleted by admin

### [ContactUs]  

Stores content of ‘Contact Us’ menu, since it can’t be stored as a single value. 

Attribute        |      Description
---------------- | --------------------
FooterPageID | Footer page identifier
Adress | Address
Telephone | Telephone number
Email | Email

### [HomePageSection]  

Stores information about configuration of home page related to ‘Most Popular’ and ‘Most Commented’ sections. 

Attribute        |      Description
---------------- | --------------------
HomePageSectionID | Record identifier
Section | Section to configure (‘Most Popular’, ‘Most Commented’)
IsActive | Indicates if section is displayed
FromPeriod | Indicates period for which to display publications

</details>
