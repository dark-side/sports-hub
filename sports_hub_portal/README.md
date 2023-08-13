## Sports Hub - Programming and Development Tasks Assistant 

To become proficient in professional programming, it's crucial to engage with technical tasks linked to a product's development. This product should serve a distinct business goal and meet user requirements. Programming is just one aspect of the broader field known as software development.

Software development involves various steps such as conceptualization, specification, design, programming, documentation, testing, and resolving errors. This encompasses the creation and maintenance of applications and software components. Initially, as you embark on your programming journey, there might be limitations on dedicating ample time to curate an effective set of technical tasks. These tasks are essential for honing programming skills by working on intricate software applications. During the early stages of programming education, allocating time to formulate and define a robust idea for your practice project can be exceptionally challenging.

Therefore, we created the sample product *Sports Hub* portal which includes:

- Product details overview
- Product functional/non-functional requirements
- Test cases for functional requirements
- UI/UX design for functional requirements
- Detailed UI/UX design demo workflows
- Technical Architecture diagrams and specifics
- API specification documentation
- Infrastructure and cloud design
- Deployment details for cloud infrastructure
- Data design including flows and pipelines
- Requirements for web, mobile, and desktop applications
- Product roadmap with estimation templates
- Technical task examples for Web, Mobile, and Desktop
- Technical task examples for Data and Infrastructure
- Effort estimation templates for Web, Mobile, and Desktop
- Effort estimation templates for Data and Infrastructure

The information provided in the documentation is sufficient to undertake various technical tasks, allowing you to enhance your skills across development processes within a chosen technological stack or domain. This enables you to dedicate more time to actual programming as opposed to preparing task specifications.

Through *Sports Hub*, you have the chance to devote additional time to learning and practicing programming, rather than being occupied with ideation, documentation, and architectural design aspects of a product.

 Please put a star <img width="55" alt="Screenshot 2021-10-26 at 20 07 09" src="https://user-images.githubusercontent.com/6854044/138927161-8ca50ae4-11cb-4091-bd3d-c50845d07e78.png"> if you like an idea or find this space useful <img width="55" alt="Screenshot 2021-10-26 at 20 07 09" src="https://user-images.githubusercontent.com/6854044/138928380-2d5fe11a-662a-4132-89b7-bfbacdb0cf0c.png">


# Sports Hub portal

- [Problem](#problem)
- [Solution](#solution)
- [Goals and objectives](#goals-and-objectives)
- [User personas](#user-personas)
- [Requirements](#requirements)
  - [Functional requirements](#functional-requirements)
    - [Website](#website)
    - [Desktop application](#desktop-application)
    - [Mobile application](#mobile-application)
  - [Non-Functional requirements](#non-functional-requirements)
  - [Layout requirements](#layout-requirements)
- [Architecture vision](#architecture-vision)
- [User interface](#user-interface)
- [Audience](#audience)
- [Future work](#future-work)

## Problem

These days in the world filled with different kinds of news presented on various websites it’s rather hard and time consuming to find the information we need. When it comes to sports, fans spend a fair amount of time browsing the web in order to find hot news relevant to their best-loved kind of sports or their favorite league or team.

## Solution

Creating a sports news site and mobile application focused exclusively on the sports activities will allow users to effectively manage the news they want to see thus helping fans and people interested in sports to address the issue of information overdose on the web and save time when looking for the news consistent with their interests.

## Goals and objectives

Specific goals are:
1. To create a web-application allowing users:
  - to read news related to different kinds of sports
  - to subscribe to the sports news of their choice
  - to receive the newsletters via email
  - to manage the kind of news they want to see (e.g. news related to the specific kind of sports,league or team)

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

## Requirements

### Functional requirements

#### Website:

Please [click here](/sports_hub_portal/web_application_features/web_application_features_list/README.md) to see Website features requirements and development roadmap

#### Desktop application:

Please [click here](/sports_hub_portal/desktop_application_features/desktop_application_features_list/README.md) to see Desktop application features requirements and development roadmap

#### Mobile application:

Please [click here](/sports_hub_portal/mobile_application_features/mobile_application_features_list/README.md) to see Mobile application features requirements and development roadmap

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

This Architecture Vision elicits the significant architecture drivers such as business, functional, nonfunctional requirements and constraints, defines architecture, and develops a roadmap for Single Entry implementation. The document is intended as a primary technical guidance into solution implementation for the development team.

Please [click here](/sports_hub_portal/architecture_vision/content/README.md) to review the Architecture Vision.

## User interface

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
