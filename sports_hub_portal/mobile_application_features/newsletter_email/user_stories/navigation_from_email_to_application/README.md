### Back to [Newsletter subscription](../../) feature

# Allow users to navigate from the email to the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to receive a newsletter email and navigate to the appropriate page
    So that I can read the latest sports news in the application

## Acceptance criteria

<pre>
<b><i>Scenario: A user receives a newsletter email and taps the Go To Read button</i></b>

Given I am a user

When I receive a newsletter email about sports news
Then I see the <b>Go To Read</b> button

When I tap the <b>Go To Read</b> button in the general news email
Then I am taken to the Home page of Sports Hub

When I tap the <b>Go To Read</b> button in the sports category/subcategory/team news email
Then I am taken to a sports category, subcategory, or team page in Sports Hub application
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a newsletter section in the footer
2. Users see a successful subscription pop-up window with details
3. Users see an email after newsletter subscribe

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a newsletter section in the footer:**

![Users see a newsletter section in the footer](/sports_hub_portal/mobile_application_features/newsletter_email/images/application_newsletter_footer.png)

**2. Users see a successful subscription pop-up window with details:**

![Users see a successful subscription pop-up window with details](/sports_hub_portal/mobile_application_features/newsletter_email/images/application_successful_subscription.png)

**3. Users see an email after newsletter subscribe:**

![Users see an email after newsletter subscribe](/sports_hub_portal/mobile_application_features/newsletter_email/images/newsletter_email.png)

</details>

## Test cases

1. Verify that the user is redirected to the appropriate page in the application by tapping the <b>Go To Read</b> button in the email

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is redirected to the appropriate page in the application by tapping the Go To Read button in the email**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is subscribed and receives an email with general news</br>- The user is subscribed and receives an email with category, subcategory, or team news|1) Open an email with general news</br>2) Tap <b>Go to read</b></br>3) Open an email with category, subcategory, or team news</br>4) Tap <b>Go to read</b>|2) The page with general news (<b>Home</b>) is opened in the application</br>4) The page with category, subcategory, or team news is opened in the application|

</details>
