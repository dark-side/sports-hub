### Back to [Website](/web_application_features/web_application_features_list/README.md) functional requirements

# Log in and sign up to the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

Users should be able to have a personal account on the Sports Hub site. To create an account, they can use the sign-up form. Users should be able to log in with the right username and password. Users should be able to restore the password using the "Forgot password?" functionality.
Admin user data should be seeded to the database and the admin user should successfully log in to the portal using those data.

## Check list:

  - Verify if UI corresponds to the prototype
  - Users should be able to sign up on the Sports Hub site via email
  - Users should be able to log in to an already created account
  - Users should not be able to log in with invalid credentials or empty credential fields (error message should appear)
  - Users should be able to restore password
  - Logged-in users should be able to change the password
  - Admin user should be able to log in using seeded data

## Prototype of the feature

Please click [here](https://www.figma.com/proto/pGlTwGGnAojQsmcvwEU1o9/Log-In-Sign-Up?node-id=6324%3A4393&viewport=504%2C425%2C0.02521197311580181&scaling=scale-down) and [here](https://www.figma.com/proto/bcp6rKNxQoYrYArsPFJS40/Personal-Cabinet?node-id=6829%3A15676&viewport=-239%2C424%2C0.08385282009840012&scaling=min-zoom) to see clickable prototypes.

Please click [here](https://www.figma.com/file/pGlTwGGnAojQsmcvwEU1o9/Log-In-Sign-Up?node-id=0%3A36) and [here](https://www.figma.com/file/bcp6rKNxQoYrYArsPFJS40/Personal-Cabinet?node-id=0%3A1) to see mockups that were included in the prototypes and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow users to sign up on the portal using an email**](/web_application_features/log_in_and_sign_up/user_stories/sign_up_to_the_portal/README.md)|<pre>As a new user<br>I want to be able to sign up using my email<br>So that I will be on the site member list</pre>
2 |[**Allow users to log in to the portal using an email**](/web_application_features/log_in_and_sign_up/user_stories/log_in_to_the_portal/README.md)|<pre>As a site user<br>I want to be able to log in with an email and password</pre>
3 |[**Allow users to reset their password**](/web_application_features/log_in_and_sign_up/user_stories/forgot_password/README.md)|<pre>As a site user<br>I want to be able to reset my password</pre>
4 |[**Add admin account to the portal**](/web_application_features/log_in_and_sign_up/user_stories/admin_account_registration/README.md)|<pre>I want to have an admin account created on the portal</pre>
5 |[**Allow admin user to log in to the portal using an email**](/web_application_features/log_in_and_sign_up/user_stories/admin_account_log_in/README.md)|<pre>As an admin user<br>I want to be able to log in with an email and password</pre>
