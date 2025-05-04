### Back to [Desktop application](/desktop_application_features/desktop_application_features_list/README.md) functional requirements

# Log in and sign up to the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

Admin user data should be seeded to the database and the admin user should successfully log in to the portal using those data. Admin user should be able to restore the password using the "Forgot password?" functionality.

## Check list:

  - Verify if UI corresponds to the prototype
  - Admin user should not be able to log in with invalid credentials or empty credential fields (error message should appear)
  - Admin user should be able to restore password
  - Admin user should be able to log in using seeded data

## Prototype of the feature

Please click to see the clickable prototypes:
  - [Windows/Linux](https://www.figma.com/proto/QCIqFV0yxhumAMtf5HWvGo/Log-in_admin?page-id=14%3A968&node-id=14-969&viewport=1459%2C603%2C0.34&t=L58eQbws0KnhW4hI-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=14%3A969)
  - [MacOS](https://www.figma.com/proto/QCIqFV0yxhumAMtf5HWvGo/Log-in_admin?page-id=0%3A1&node-id=3-512&viewport=890%2C3047%2C0.45&t=1xz2yosmVdQ5xYcH-1&scaling=min-zoom&content-scaling=fixed)

Please click [here](https://www.figma.com/file/QCIqFV0yxhumAMtf5HWvGo/Log-in_admin?node-id=0%3A1) to see mockups that were included in the prototypes and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Add admin account to the portal**](/desktop_application_features/log_in_and_sign_up/user_stories/admin_account_registration/README.md)|<pre>I want to have an admin account created on the portal</pre>
2 |[**Allow admin user to log in to the portal using an email**](/desktop_application_features/log_in_and_sign_up/user_stories/admin_account_log_in/README.md)|<pre>As an admin user<br>I want to be able to log in with an email and password</pre>
3 |[**Allow admin user to reset their password**](/desktop_application_features/log_in_and_sign_up/user_stories/forgot_password/README.md)|<pre>As an admin user<br>I want to be able to reset my password</pre>
