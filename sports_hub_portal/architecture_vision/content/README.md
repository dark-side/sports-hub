### Back to [Sports Hub portal product map](../../README.md)

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
    - [4.1.1 Solution Context](#411-solution-context)
    - [4.1.2 Solution Decomposition](#412-solution-decomposition)
  - [4.2 Development Technology Stack](#42-development-technology-stack)
- [5 Operation Plan](#5-operation-plan)

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

![Business level view of Sports Hub Portal](/sports_hub_portal/architecture_vision/images/figure_1_business_level_view.png)

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

![Solution Context](/sports_hub_portal/architecture_vision/images/figure_2_solution_context.png)

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

![Basic Cloud Solution Decomposition](/sports_hub_portal/architecture_vision/images/figure_3_basic_cloud_solution.jpg)

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

![Medium Cloud Solution Decomposition](/sports_hub_portal/architecture_vision/images/figure_4_basic_cloud_solution.jpg)

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

![Hard Cloud Solution Decomposition](/sports_hub_portal/architecture_vision/images/figure_5_basic_cloud_solution.png)

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

![Dedployment Diagram GCP - basic complexity](/sports_hub_portal/architecture_vision/images/gcp_basic.png)

<p align="center"><i>Figure 6. Dedployment Diagram GCP - basic complexity</i></p>

![Dedployment Diagram GCP - medium complexity](/sports_hub_portal/architecture_vision/images/gcp_medium.png)

<p align="center"><i>Figure 7. Dedployment Diagram GCP - medium complexity</i></p>

![Dedployment Diagram GCP - hard complexity](/sports_hub_portal/architecture_vision/images/gcp_hard.png)

<p align="center"><i>Figure 8. Dedployment Diagram GCP - hard complexity</i></p>


<ins><b>Infrastructure Azure:</b></ins> Azure is used as main and single cloud provider. Services that is used by solution are WebApps, Azure CDN, Azure Storage, Azure Functions, Azure SQL, Azure Cognitive Search, Azure Redis, Azure Scheduler. Azure Service Bus.

![Dedployment Diagram Azure - basic complexity](/sports_hub_portal/architecture_vision/images/azure_basic.png)

<p align="center"><i>Figure 9. Dedployment Diagram Azure - basic complexity</i></p>

![Dedployment Diagram Azure - medium complexity](/sports_hub_portal/architecture_vision/images/azure_medium.png)

<p align="center"><i>Figure 10. Dedployment Diagram Azure - medium complexity</i></p>

![Dedployment Diagram Azure - hard complexity](/sports_hub_portal/architecture_vision/images/azure_hard.png)

<p align="center"><i>Figure 11. Dedployment Diagram Azure - hard complexity</i></p>


<ins><b>Infrastructure AWS:</b></ins> AWS is used as main and single cloud provider. Services that is used by solution are Elastic Beanstalk, AWS Lambdas, AWS S3, Elasticsearch, Amazon SQS, AWS Batch Scheduler, AWS ElastiCache, Amazon RDS, Amazon CloudFront, AWS API Gateway.

![Dedployment Diagram AWS - basic complexity](/sports_hub_portal/architecture_vision/images/aws_basic.png)

<p align="center"><i>Figure 12. Dedployment Diagram AWS - basic complexity</i></p>

![Dedployment Diagram AWS - medium complexity](/sports_hub_portal/architecture_vision/images/aws_medium.png)

<p align="center"><i>Figure 13. Dedployment Diagram AWS - medium complexity</i></p>

![Dedployment Diagram AWS - hard complexity](/sports_hub_portal/architecture_vision/images/aws_hard.png)

<p align="center"><i>Figure 14. Dedployment Diagram AWS - hard complexity</i></p>



<ins><b>Environments:</b></ins> For transitional phase there will be four environments: development, testing, staging and production. Development environment use minimal cloud resources but similar architecture. Testing environment use intermediate resource allocation for full QA testing. Staging environment is a copy of production environment and is used for load, performance and user acceptance testing. Production environment is scalable and fault tolerant.
