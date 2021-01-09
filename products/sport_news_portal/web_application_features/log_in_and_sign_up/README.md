# Log in and sign up to the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the Feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

The user should be able to have a personal account on the Sport News site. To create an account, the user can use the sign-up form or sign up via social networks, such as Google+ and Facebook, that are present on the sign-up window. The user should be able to log in with the right username and password or via social network buttons on the login form. The user should be able to restore the password using the "Forgot password?" functionality. Registered users should have a personal cabinet where they can view and update personal information:
- First name
- Last name
- Profile picture
- Password

## Check list:

  - Verify if UI corresponds to prototype
  - User should be able to sign up into Sport News site via email
  - User should be able to sign up into Sport News site via social network accounts
  - User should be able to log into an already created account
  - User should not be able to log in with invalid credentials or empty credential fields (error message should appear)
  - User should be able to restore password
  - Logged-in user should be able to view personal information on the profile page (_do not allow if logged by social network_)
  - Logged-in user should be able to update the personal information on the profile page (_do not allow if logged by social network_)
  - Logged-in user should be able to change a password (_do not allow if logged by social network_)
  - Logged-in user should be able to upload a photo as a profile picture (_do not allow if logged by social network_)

## Prototype of the feature

Please click [here](https://www.figma.com/proto/pGlTwGGnAojQsmcvwEU1o9/Log-In-Sign-Up?node-id=6324%3A4393&viewport=504%2C425%2C0.02521197311580181&scaling=scale-down) and [here](https://www.figma.com/proto/bcp6rKNxQoYrYArsPFJS40/Personal-Cabinet?node-id=6829%3A15676&viewport=-239%2C424%2C0.08385282009840012&scaling=min-zoom) to see clickable prototypes.

Please click [here](https://www.figma.com/file/pGlTwGGnAojQsmcvwEU1o9/Log-In-Sign-Up?node-id=0%3A36) and [here](https://www.figma.com/file/bcp6rKNxQoYrYArsPFJS40/Personal-Cabinet?node-id=0%3A1) to see mockups that were included in the prototypes and additional style guides.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow users to sign up to the portal using an email**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/sign_up_to_the_portal)|<pre>As a new user<br>I want to be able to sign up using my email<br>So that I will be in the site member list</pre>
2 |[**Allow users to log in to the portal using an email**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/log_in_to_the_portal)|<pre>As a site user<br>I want to be able to login with an email and password</pre>
3 |[**Allow users to sign up using a third-party authentication provider**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/sign_up_with_third_party) |<pre>As a new user<br>I want to be able to sign up using a third-party authentication provider<br>So that I will be in the site member list</pre>
4 |[**Allow users to log in to the portal using a third-party authentication provider**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/log_in_with_third_party) |<pre>As a site user<br>I want to be able to login using a third-party authentication provider</pre>
5 |[**Allow users to reset their password**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/forgot_password)|<pre>As a site user<br>I want to be able to reset my password</pre>
6 |[**Allow users to update their personal information**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/personal_information_update)|<pre>As a site user<br>I want to be able to update my personal information</pre>
7 |[**Allow users to change their password via profile**](/products/sport_news_portal/web_application_features/log_in_and_sign_up/user_stories/password_update)|<pre>As a site user<br>I want to be able to update my password</pre>
