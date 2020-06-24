# User Management on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the Feature](#prototype-of-the-feature)
- [User Stories](#user-stories)

## Description

We allow users to register for our application. We need a place where we can review and manage a list of users if needed. This should be available on the Admin side. In the list, we can review users’:<br>
  - Avatar
  - Name, and Last Name
  - Their status: Active, Blocked
  - Online/offline availability
  - Role. We need two roles - User and Admin
  - Amount of users and admins
  
The actions we want to do on the user is to Block, Activate, Delete and Make as Admin, Remove from Admin.<br>
Delete - the user should be removed from the system and not have the ability to log in to the system.<br>
Block - the user should be blocked which means the user will not be able to comment on any article or video and review any comment. Users should be notified about this action.<br>
Activate - only blocked users can be activated. Users should be notified about this action.<br>
Make as Admin - the user will receive admin permissions. Users should be notified about this action.<br>
Remove from Admin - removes admin permission from the user.

## Check list:

  - Verify if UI corresponds to prototype
  - Admin should be able to delete user
  - Admin should be able to clock user
  - Admin should be able to activate user that was blocked
  - Admin should be able to give admin permissions to user
  - Admin should be able to remove admin permission from user
  - User should be able to receive mails that inform them about admin’s actions 
  - Confirmation popups and dropdown lists should be not corrupted

## Prototype of the feature

  Please click [here](https://www.figma.com/proto/8nNZGVmkZ2ukXV7NhmawgO/User-Management?node-id=0%3A1075&scaling=min-zoom) to see a clickable prototype for the feature.

## User Stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to view User Management page on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/create_user_management_page_on_the_admin_side)|<pre>As an admin user<br>I want to be able to have a place with the list of users<br>So that I can review and manage them</pre>
2 |[**Allow admin user to delete users on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/delete_user)|<pre>As an admin user<br>I want to be able to have the ability to delete users<br>So that they have not an account to log in to the system</pre>
3 |[**Allow admin user to block users on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/block_user)|<pre>As an admin user<br>I want to be able to have the ability to block users<br>So that they won’t have access to comments</pre>
4 |[**Allow admin user to activate users on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/activate_user)|<pre>As an admin user<br>I want to be able to have the ability to activate users<br>So that they will have access to comments</pre>
5 |[**Allow admin user to give user admin permissions on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/give_user_admin_permissions)|<pre>As an admin user<br>I want to be able to have the ability to give users admin permissions</pre>
6 |[**Allow admin user to remove admin permissions from the user on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/remove_admin_permissions_from_the_user)|<pre>As an admin user<br>I want to be able to have the ability to remove admin permissions from the users</pre>
7 |[**Allow admin user to view online/offline status of the user on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/view_online_offline_status_of_the_users)|<pre>As an admin user<br>I want to be able to have the ability to see if users are online/offline</pre>
8 |[**Allow admin user to filter users on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/filter_users)|<pre>As an admin user<br>I want to be able to have the ability to filter users based on criteria<br>So that I can perform the needed action</pre>
9 |[**Allow admin user to search users on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/search_users)|<pre>As an admin user<br>I want to be able to have the ability to search users by name</pre>
10 |[**Allow admin user to send notification emails to the users on the portal**](/products/sport_news_portal/web_application_features/user_management/user_stories/send_notification_emails_to_the_user)|<pre>As a site user<br>I want to be able to receive notification to my email<br>So that I know if I was blocked, activated, got/lost admin permissions</pre>
