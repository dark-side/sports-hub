### Back to [Log in and sign up to the portal](../../) feature

# Allow admin user to log in to the portal using an email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to log in with an email and password

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user logs in to the portal</i></b>

Given I have an account on the Sports Hub site (seeded to the datatabase)

When I visit any page on the site
Then I see the <b>Log in</b> button in the upper-right corner of the page

When I click <b>Log in</b>
Then I am taken to the <b>Log in</b> page

When I enter all the fields with the seeded admin data and click <b>Log in</b>
Then I am authenticated at the website
  And I am taken to the home configuration page
  And the log in link is replaced with my name
  And I see <b>Administrator</b> label under my name
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Sign Up</b> button
2. Users see the log-in form
3. Admin user sees home configuration page and <b>Administrator</b> label under their name after successful logging in

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Sign Up button:**

![Users see the Sign Up button](/sports_hub_portal/desktop_application_features/log_in_and_sign_up/images/home_page_logged_out_user.png)

**2. Users see the log-in form:**

![Users see the log-in form](/sports_hub_portal/desktop_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**3. Admin user sees home configuration page and Administrator label under their name after successful logging in :**

![Admin user sees home configuration page and Administrator label under their name after successful logging in](/sports_hub_portal/desktop_application_features/log_in_and_sign_up/images/home_page_logged_in_admin.png)

</details>

## Test cases

1. Verify that the admin user is able to log in to the Sports Hub site with valid credentials and sees <b>Administrator</b> label under their name
2. Verify that the admin user is landed on the home configuration page after successful log in

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the admin user is able to log in to the Sports Hub site with valid credentials and sees Administrator label under their name**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Have an admin user account seeded|1) Click **Log in** in the upper-right corner of the page</br>2) Enter valid data in the **Email address** and **Password** fields</br>3) Click **Log in**|3) The admin user is successfully logged in</br>4) The admin user sees <b>Administrator</b> label under their name|

### **#2. Verify that the admin user is landed on the home configuration page after successful log in**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Have an admin user account seeded|1) Click **Log in** in the upper-right corner of the page</br>2) Enter valid data in the **Email address** and **Password** fields</br>3) Click **Log in**|3) The admin user is successfully logged in</br>3) The admin user is landed on the home configuration page</br>|
</details>
