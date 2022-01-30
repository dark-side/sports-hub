### Back to [Mobile application](/sports_hub_portal/mobile_application_features/mobile_application_features_list/) functional requirements

# Log in and sign up in the application

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

Users should be able to have a personal account in the application. To create an account, they can use the sign-up form or sign up via social networks, such as Google+ and Facebook, that are present on the sign-up page. Users should be able to log in with the right username and password or via social network buttons on the log-in form. Users should be able to restore the password using the "Forgot password?" functionality. Registered users should have a personal cabinet where they can view and update personal information:
  - First name
  - Last name
  - Profile picture
  - Password

## Check list:

  - Verify if UI corresponds to the prototype
  - Users should be able to sign up in the Sports Hub application via email
  - Users should be able to sign up in the Sports Hub application via social network accounts
  - Users should be able to log in to an already created account
  - Users should not be able to log in with invalid credentials or empty credential boxed (error message should appear)
  - Users should be able to restore password
  - Logged-in users should be able to view personal information on the profile page (_do not allow if logged-in via social network_)
  - Logged-in users should be able to update the personal information on the profile page (_do not allow if logged-in via social network_)
  - Logged-in users should be able to change the password (_do not allow if logged-in via social network_)
  - Logged-in users should be able to upload a photo as a profile picture (_do not allow if logged-in via social network_)

## Prototype of the feature

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sports-Hub-General-Prototype?page-id=0%3A5852&node-id=0%3A7481&viewport=-1637%2C-969%2C0.37520089745521545&scaling=scale-down) to see a clickable prototype.

Please click [here](https://www.figma.com/file/egXgh8BYD7Xaa0JeMNhv9R/Manage-advertisements?node-id=0%3A1075) to see mockups that were included in the prototype and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow users to sign up in the application using an email**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/sign_up_with_email)|<pre>As a new user<br>I want to be able to sign up using my email<br>So that I will be on the Sports Hub members list</pre>
2 |[**Allow users to log in to the application using an email**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/log_in)|<pre>As a user<br>I want to be able to log in with an email and password</pre>
3 |[**Allow users to sign up using a third-party authentication provider**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/sign_up_with_third_party) |<pre>As a new user<br>I want to be able to sign up using a third-party authentication provider<br>So that I will be on the Sports Hub members list</pre>
4 |[**llow users to log in the application using a third-party authentication provider**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/log_in_with_third_party) |<pre>As a user<br>I want to be able to log in using a third-party authentication provider</pre>
5 |[**Allow users to reset their password**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/forgot_password)|<pre>As a user<br>I want to be able to reset my password</pre>
6 |[**Allow users to update their personal information**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/personal_information_update)|<pre>As a user<br>I want to be able to update my personal information</pre>
7 |[**Allow users to change their password via profile**](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/user_stories/password_update)|<pre>As a user<br>I want to be able to update my password</pre>
