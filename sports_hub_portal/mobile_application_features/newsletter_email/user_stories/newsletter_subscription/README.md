### Back to [Newsletter subscription](../../) feature

# Allow users to subscribe to newsletter

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to subscribe to the Sports Hub
    So that I can receive an email with the latest sports news

## Acceptance criteria

<pre>
<b><i>Scenario: A user subscribes to the Sports Hub</i></b>

Given I am a user

When I view the page and the Newsletter subscription section in the footer
Then I see the following:
  - Newsletter heading
  - <b>Sign up to receive the latest sports news</b> label
  - Input for an email address
  - The <b>Subscribe</b> button

When I enter an email address and tap <b>Subscribe</b>
Then I see the pop-up window with notification about the subscribed news category

<i>NOTE: The subscription depends on the section of the application you are currently on, for example:
  - Home page – subscription to all general sports news
  - NBA sport category page – subscription to NBA news
  - Los Angeles Lakers team page – subscription to Los Angeles Lakers team news</i>
</pre>
</pre>

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

1. Verify the <b>Subscribe</b> button functionality on the <b>Home</b> page
2. Verify the <b>Subscribe</b> button functionality on any opened page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the Subscribe button functionality on the Home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the application footer > <b>Newsletter</b>|1) In the <b>Your email address</b> field, enter an email address</br>2) Tap <b>Subscribe</b></br>3) Verify that the user is subscribed to all general sports news|2) The pop-up window appears with a notification that the user is subscribed to all general sports news</br>3) The user receives an email with the latest news from all categories on a daily basis|

### **#2. Verify the Subscribe button functionality on any opened page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the <b>NBA</b> league page/<b>Los Angeles Lakers</b> team page</br>- On the application footer > <b>Newsletter</b>|1) In the <b>Your email address</b> field, enter the user email address</br>2) Tap <b>Subscribe</b></br>3) Verify that the user is subscribed to <b>NBA</b> league/<b>Los Angeles Lakers</b> team news|2) The pop-up window appears with a notification that the user is subscribed to <b>NBA</b> league/<b>Los Angeles Lakers</b> team news</br>3) The user receives an email with the latest news from the appropriate category/team page on a daily basis|

</details>
