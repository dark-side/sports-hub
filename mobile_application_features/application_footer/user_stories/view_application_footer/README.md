### Back to [Application footer](../../README.md) feature

# Allow users view footer in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to see the footer on every page of the application
    So that I can see the links to pages to read more about the company, contributors, and subscribe to receive the latest news

## Acceptance criteria

<pre>
<b><i>Scenario: A user sees the footer on every page of the application</i></b>

Given I am a user

When I view any page
Then I see a footer containing the following:
  - Three sections: <b>Company info</b>, <b>Contributors</b>, <b>Newsletter</b>
  - Bottom block with a Sports Hub logo and the copyright sign at the left and the link to the Privacy / Terms page
  And I see the <b>Company info</b> section consists of the following links:
    - About Sports Hub
    - News / In the Press
    - Advertising / Sports Blogger Ad Network
    - Events
    - Contact Us
  And I see the <b>Contributors</b> section consists of the following links:
    - Featured Writers Program
    - Featured Team Writers Program
    - Internship Program
  And I see the Contributors section has the <b>Sign up to receive the latest sports news</b> option containing the input for the email address followed by the <b>Subscribe</b> button
  And I see the Sports Hub logo and the copyright sign at the left and the <b>Privacy / Terms</b> link at the right of bottom section

When I tap the Sports Hub logo
Then I am taken to the <b>Home</b> page

When I select the <b>Privacy / Terms</b> link
Then I am taken to the appropriate page

When I select a link in the <b>Company info</b>, <b>Contributors</b>, or <b>Copyright</b> section
Then I am taken to the appropriate page

When I enter my email newsletter box and tap <b>Subscribe</b>
Then I see the pop-up window with confirmation about subscription
  And I see which category of news I have subscribed to
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Full page
2. Users see footer in the Sports Hub application
3. <b>Contact Us</b> full page
4. <b>About Sports Hub</b> full page
5. Users see the <b>About Sports Hub</b> page
6. Users see the <b>Privacy Policy</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Full page:**

![Full page](/mobile_application_features/application_footer/images/footer.png)

**2. Users see footer in the Sports Hub application:**

![Users see footer in the Sports Hub application](/mobile_application_features/application_footer/images/application_footer.png)

**3. Contact Us full page:**

![Contact Us full page](/mobile_application_features/application_footer/images/contact_us.png)

**4. About Sports Hub full page:**

![About Sports Hub full page](/mobile_application_features/application_footer/images/about_sports_hub.png)

**5. Users see the About Sports Hub page:**

![Users see the About Sports Hub page](/mobile_application_features/application_footer/images/application_about_sports_hub.png)

**6. Users see the Privacy Policy page:**

![Users see the Privacy Policy page](/mobile_application_features/application_footer/images/application_privacy_policy.png)

</details>

## Test cases

1. Verify that footer section is visible from any page for users
2. Verify that users can select the links in the <b>Company info</b> and <b>Contributors</b> columns
3. Verify that users can read Privacy Policy / Terms and Conditions information by selecting the <b>Privacy / Terms</b> link
4. Verify that users are redirected to the <b>Home</b> page by tapping the Sports Hub logo

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that footer section is visible from any page for users**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Browse through different pages|1) The footer section is present on every page|

### **#2. Verify that users can select the links in the Company info and Contributors columns**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the footer</br>2) In the <b>Company info</b> and <b>Contributors</b> columns, select the links one by one|2) Links show appropriate info or redirect to appropriate pages|

### **#3. Verify that users can read Privacy Policy / Terms and Conditions information by selecting the Privacy / Terms link**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the footer</br>2) Select the <b>Privacy</b> link</br>3) Select the <b>Terms</b> link|2) The <b>Privacy Policy</b> page opens</br>3) The <b>Terms and Conditions</b> page opens|

### **#4. Verify that users are redirected to the Home page by tapping the Sports Hub logo**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to any page except <b>Home</b></br>2) Go to the footer</br>3) Tap the <b>Sports Hub</b> logo|3) The user is redirected to the home page|
</details>
