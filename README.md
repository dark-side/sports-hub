## Hands-on learning with real-world tasks with Sports Hub

Your professional development journey with the Sports Hub space can help you to carve out and dedicate more time to learning and practicing software programming, data development, testing, test automation, and software configuration, freeing yourself from tasks like product ideation, platform solution design documentation, and feature requirements documentation.

To become proficient in professional software development, it's crucial to engage associates in accomplishing practical technical tasks focused on reaching a product's development goals and requirements, which are part of real-world projects professionals do regularly.

Software development involves various steps such as conceptualization, specification, design, programming, testing, documentation, release, and maintenance. This covers the creation and maintenance of applications and software components.

During professional growth on real-world projects or preparation to work on real-world projects, there is a lack of practical tasks on which associates can grow. This leads to the need to define a learning project with product requirements to practice specific technical aspects of the role that professionals do according to functional and non-functional requirements based on clearly described product features, with the use cases, mock-ups, demo flows, test cases, and architecture diagrams.

The development process of creating such types of requirements and documentation requires a large amount of time. Usually, such activities take a significant part of the time dedicated to the skill-ups of software engineers, data engineers, infrastructure engineers, or quality engineers. Sometimes the creation of such documents may take 40%-60% of the time you dedicate to learning.

We believe that during learning and professional development, activities will be extremely useful to have pre-defined requirements suitable for practicing task accomplishment. In such cases, the learning process of 80%-90% will be focused on learning activities and practical work activities that the professionals do according to their role on project assignments. It is useful when you are involved in such events as rump-up, skill-up, simulation training, executive coaching, mentorship programs, workshops, boot camps, micro learnings, etc.

This Sports Hub space is aimed at describing a product with distinct business goals and requirements to meet user and customer expectations for the development of a custom platform that covers front-end, mobile, desktop, back-end, API, and data domains for representing the sports news and events related to different types of sports. It allows you to use all the documentation to cover a huge variety of product features' requirements that can be used as development tasks during your practice over your learning journey.

The Sports Hub space documentation includes:

- Product details overview
- Product functional/non-functional requirements
- Test cases for functional requirements
- UI/UX design for functional requirements
- Detailed UI/UX design demo workflows
- Technical Architecture diagrams and specifics
- API specification documentation
- Infrastructure and cloud design
- Deployment details for cloud infrastructure
- Data design, including flows and pipelines
- Requirements for web, mobile, and desktop applications
- Product roadmap with estimation templates
- Technical task examples for Web, Mobile, and Desktop
- Technical task examples for Data and Infrastructure
- Effort estimation templates for Web, Mobile, and Desktop
- Effort estimation templates for Data and Infrastructure

For sure, when you start learning and a professional development journey, it might be difficult to define a point from which you can start working with a bunch of those documents. Therefore, we create GitHub pages and video guides from which you can start your work on familiarization with the Sports Hub portal requirements for your growth.

The information provided in the documentation is sufficient to undertake various technical tasks, allowing you to enhance your skills across development processes within a chosen role, technological stack, or domain. This enables you to dedicate more time to actual programming than to preparing task specifications.

We hope that the space will be useful for software engineers (front-end, back-end, full-stack, API, mobile, and desktop directions), data engineers (databases and data visualization directions), infrastructure engineers (DevOps and Clouds directions), and quality engineers (quality control and test automation directions).

If you find it useful, please encourage us with your stars <img width="55" alt="Screenshot 2021-10-26 at 20 07 09" src="https://user-images.githubusercontent.com/6854044/138927161-8ca50ae4-11cb-4091-bd3d-c50845d07e78.png">, forks, PRs with new suggestions, and comments with propositions. It a valuable and important for us as contributors to this and related spaces. <img width="55" alt="Screenshot 2021-10-26 at 20 07 09" src="https://user-images.githubusercontent.com/6854044/138928380-2d5fe11a-662a-4132-89b7-bfbacdb0cf0c.png">

# Sports Hub - Platform details

- [Problem definition](#problem-definition)
- [Solution details](#solution-details)
- [Goals and objectives](#goals-and-objectives)
- [User personas](#user-personas)
- [User requirements](#user-requirements)
  - [Functional requirements](#functional-requirements)
    - [Website](#website)
    - [Desktop application](#desktop-application)
    - [Mobile application](#mobile-application)
  - [Non-Functional requirements](#non-functional-requirements)
  - [Layout requirements](#layout-requirements)
- [Architecture vision](#architecture-vision)
- [Database Requirements](#database-requirements)
- [User interface and experience](#user-interface-and-experience)
- [Audience](#audience)
- [Future work](#future-work)

## Problem definition

These days, in a world filled with different kinds of news presented on various websites, it’s rather hard and time-consuming to find the information we need. When it comes to sports, fans spend a fair amount of time browsing the web in order to find hot news relevant to their best-loved kind of sports or their favorite league or team.

## Solution details

Creating a sports news site and mobile application focused exclusively on sports activities will allow users to effectively manage the news they want to see, thus helping fans and people interested in sports to address the issue of information overload on the web and save time when looking for the news consistent with their interests.

## Goals and objectives

Specific goals are:
1. To create a web application allowing users:
  - to read news related to different kinds of sports
  - to subscribe to the sports news of their choice
  - to receive the newsletters via email
  - to manage the kind of news they want to see (e.g., news related to the specific kind of sports, league, or team)

2. To create the Content Management System (CMS) allowing users with proper permission to define the structure and content of the web-application

3. To create a mobile application allowing users:
  - to read news related to different kinds of sports
  - to subscribe to the sports news of their choice
  - to receive the newsletters via email

## Audience

1. Sports fans.
2. People in search of the latest sports news.
3. People who want to receive sport news emails.

## User personas

**Unauthorized website user (not logged in to the Sports Hub site)**

    Available actions
      - View sports news (note: the structure of the news pages and the content of the pages (articles) are defined in the CMS)
      - Subscribe to receive sports news (note: there are a few different subscription types: General news, League news, Team news)
      - Share the news via the Social Media (when configured in the CMS)
      - Login/Sign up to the Sports Hub site (including the Login/Sign up with the Social Networks if enabled in CMS)

**Authorised website user (logged in to the Sports Hub site)**

    Available actions:
      - Manage personal info
      - Manage team subscriptions
      - Manage surveys
      - Answer the surveys
      - Comment on an article
      - Actions available for an unauthorized user

**Admin**

    Available actions:
    Can configure the following parts of the site via the CMS on the website and desktop application:
      - Site footer
      - Site menu (including nested menu dropdowns)
      - Site users
      - Structure of the pages
      - Articles
      - Sports Categories (Leagues)
      - Sports Subcategories
      - Teams
      - Relations between Categories, Subcategories, Teams
      - Site Languages
      - Social Networks support
      - Surveys
      - Banners
      - Advertisements

**Unauthorized mobile application user (not logged in to the Sports Hub mobile application)**

    Available actions
      - View sports news (note: the structure of the news pages and the content of the pages (articles) are defined in the CMS)
      - Subscribe to receive sports news (note: there are a few different subscription types: General news, League news, Team news)
      - Share the news via the Social Media (when configured in the CMS)
      - Login/Sign up to the Sports Hub mobile application (including the Login/Sign up with the Social Networks if enabled in CMS)

**Authorised mobile application user (logged in to the Sports Hub mobile application)**

    Available actions:
      - Manage personal info
      - Manage team subscriptions
      - Manage surveys
      - Answer the surveys
      - Comment on an article
      - Actions available for an unauthorized user

## User requirements

### Functional requirements

#### Website:

Please [click here](/web_application_features/web_application_features_list/README.md) to see Website features requirements and development roadmap

#### Desktop application:

Please [click here](/desktop_application_features/desktop_application_features_list/README.md) to see Desktop application features requirements and development roadmap

#### Mobile application:

Please [click here](/mobile_application_features/mobile_application_features_list/README.md) to see Mobile application features requirements and development roadmap

### Non-functional requirements

- The application should use Cloud service for storing images and video files
- The application should be built following the REST principles
- The application must work in all modern browsers
- The application must be able to support 1000 simultaneous users

### Layout requirements

Please follow [the style guides](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) of this product for each feature.

- The site inputs should have validation on the server side as well as on a client side (consider limiting input length, checking the input value format and type)
- The site links should be opened in a new tab
- The site links should be highlighted on hover
- The menu item that is currently active (meaning user is viewing it in the moment) should be highlighted

## Architecture vision

This Architecture Vision elicits the significant architecture drivers such as business, functional, nonfunctional requirements and constraints, defines architecture, and develops a roadmap for Single Entry implementation. The document is intended as a primary technical guidance for solution implementation for the development team.

Please [click here](/architecture_vision/content/README.md) to review the Architecture Vision.

## Database Requirements

The purpose of this document is to define the requirements for the database that will be used to support a sports web portal. 

Please [click here](/db_requirements/content/README.md) to review the Database Requirements.

## User interface and experience

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A2&viewport=592%2C442%2C1&scaling=min-zoom) to see a general clickable prototype.

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sports-Hub-General-Prototype?page-id=0%3A5852&node-id=0%3A5853&viewport=284%2C263%2C0.04008595272898674&scaling=scale-down) to see a mobile application clickable prototype.

Please click [here](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.04&scaling=min-zoom&starting-point-node-id=19%3A5368&show-proto-sidebar=1) to see style guides.

Please click [here](https://www.figma.com/file/0zkkf5WC77OSpvyD6YXpFE/Style-guides?node-id=0%3A1
) to see style guides mockups.

## Future work

1. Page templates list. Build support for admins to choose the page template when creating a new page for the Sports Hub application.
2. Admins with different sets of permissions. Build a possibility for admin users to define permissions for other admins in order to make it possible to create admins with limited access to CMS.


# License

Copyright (c) 2019 Dark Side

Licensed under either of

 * Apache License, Version 2.0
   [LICENSE-APACHE](http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license
   [LICENSE-MIT](http://opensource.org/licenses/MIT)

at your option.

# Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.

**Should you have any suggestions please create an Issue for this repository** 
