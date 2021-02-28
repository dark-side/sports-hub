# Surveys on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

To gather information from sports fans and build statistics, we need to have functionality that will allow us to create questionnaires.

An admin user should be able to create, edit, delete, and close surveys with predefined answers, send them to users and review voting results.

Users should have a separate page for their surveys and should also have the ability to vote while reading the news.

## Check list:

  - Verify if UI corresponds to the prototype
  - Admin should be able to create, edit, delete, and close a survey
  - Admin should be able to send a survey to users
  - Logged-in users should be able to submit a survey 
  - Logged-in users should be able to view all published surveys
  - Logged-in users should be able to sort opened surveys by Newest, Most Popular, and About to Expire
  - Logged-in users should be able to view all closed surveys
  - Logged-in users should be able to filter closed surveys by Voted or All surveys filter
  - Logged-in users should be able to sort closed surveys by the close date
  - Admin should be able to review voting results

## Prototype of the feature

_Admin side_

Please click [here](https://www.figma.com/proto/xtzyZ1sFmeSaKMpHDu0WfH/Surveys?node-id=0%3A1075&viewport=-74%2C435%2C0.06860820204019547&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/xtzyZ1sFmeSaKMpHDu0WfH/Surveys?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

_User side_

Please click [here](https://www.figma.com/proto/xtzyZ1sFmeSaKMpHDu0WfH/Surveys?node-id=0%3A2&viewport=513%2C537%2C0.12442872673273087&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/xtzyZ1sFmeSaKMpHDu0WfH/Surveys?node-id=0%3A1) to see mockups that were included in the prototype and additional style guides.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin to create surveys on the portal**](/products/sport_news_portal/web_application_features/surveys/user_stories/create_surveys)|<pre>As an admin user<br>I want to create surveys on the portal</pre>
2 |[**Allow admin to publish surveys**](/products/sport_news_portal/web_application_features/surveys/user_stories/publish_survey)|<pre>As an admin user<br>I want to be able to publish surveys<br>So that users can see them and vote</pre>
3 |[**Allow admin to close surveys**](/products/sport_news_portal/web_application_features/surveys/user_stories/close_survey)|<pre>As an admin user<br>I want to be able to close surveys</pre>
4 |[**Allow admin to filter surveys**](/products/sport_news_portal/web_application_features/surveys/user_stories/filter_surveys)|<pre>As an admin user<br>I want to be able to filter opened surveys</pre>
5 |[**Allow users to see a list of all surveys**](/products/sport_news_portal/web_application_features/surveys/user_stories/my_surveys_for_user)|<pre>As a site user<br>I want to see a list of all surveys<br>So that I can vote</pre>
6 |[**Allow users to participate in surveys on the My surveys page**](/products/sport_news_portal/web_application_features/surveys/user_stories/form_for_voting)|<pre>As a site user<br>I want to vote on the My surveys page in my personal cabinet</pre>
7 |[**Allow users to participate in surveys on news pages**](/products/sport_news_portal/web_application_features/surveys/user_stories/banner_for_voting)|<pre>As a site user<br>I want to see a survey banner on news pages<br>So that I can vote</pre>
