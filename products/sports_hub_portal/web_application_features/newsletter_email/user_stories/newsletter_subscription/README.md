### Back to [Newsletter subscription](../../) feature

# Allow users to subscribe to newsletter

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to subscribe to the Sports Hub site
    So that I can receive an email with the latest sports news

## Acceptance criteria

<pre>
<b><i>Scenario: A site user subscribes to the Sports Hub site</i></b>

Given I am a site user

When I view the page and the <b>Newsletter</b> subscription section in the site footer
Then I see the following:
  - Newsletter heading
  - <b>Sign up to receive the latest sports news</b> label
  - Input for an email address
  - The <b>Subscribe</b> button

When I enter an email address and click <b>Subscribe</b>
Then I see the pop-up window with notification about the subscribed news category

When I receive newsletter email about sports news
Then I see the <b>Go To Read</b> button

When I click <b>Go To Read</b> button in the general news email
Then I am taken to the <b>Home</b> page of the Sports Hub site 

When I click <b>Go To Read</b> button in the sports category/subcategory/team news email
Then I am taken to a sports category, subcategory, or team page of the Sports Hub site

<i>NOTE: The subscription depends on the section of the site you are currently on, for example:
  - Home page – subscription to all general sports news
  - NBA sport category page – subscription to NBA news
  - Los Angeles Lakers team page – subscription to Los Angeles Lakers team news</i>
</pre>

## Mockups

1. Users see a newsletter section in the site footer
2. Users see a successful subscription pop-up window with details
3. Users see an email after newsletter subscribe

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a newsletter section in the site footer:**

![Users see a newsletter section in the site footer](/products/sports_hub_portal/web_application_features/newsletter_email/images/site_footer.png)

**2. Users see a successful subscription pop-up window with details:**

![Users see a successful subscription pop-up window with details](/products/sports_hub_portal/web_application_features/newsletter_email/images/successful_subscription.png)

**3. Users see an email after newsletter subscribe:**

![Users see an email after newsletter subscribe](/products/sports_hub_portal/web_application_features/newsletter_email/images/news_email.png)

</details>

## Test cases

1. Verify the <b>Subscribe</b> button functionality on the <b>Home</b> page
2. Verify the <b>Subscribe</b> button functionality on any opened page
3. Verify that the user is redirected to the appropriate page by clicking the <b>Go To Read</b> button in the email

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the Subscribe button functionality on the Home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the site footer > <b>Newsletter</b>|1) In the <b>Your email address</b> field, enter an email address</br>2) Click <b>Subscribe</b></br>3) Verify that the user is subscribed to all general sports news|2) The pop-up window appears with a notification that the user is subscribed to all general sports news</br>3) The user receives an email with the latest news from all categories on a daily basis|

### **#2. Verify the Subscribe button functionality on any opened page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the <b>NBA</b> league page/<b>Los Angeles Lakers</b> team page</br>- On the site footer > <b>Newsletter</b>|1) In the <b>Your email address</b> field, enter the user email address</br>2) Click <b>Subscribe</b></br>3) Verify that the user is subscribed to <b>NBA</b> league/<b>Los Angeles Lakers</b> team news|2) The pop-up window appears with a notification that the user is subscribed to <b>NBA</b> league/<b>Los Angeles Lakers</b> team news</br>3) The user receives an email with the latest news from the appropriate category/team page on a daily basis|

### **#3. Verify that the user is redirected to the appropriate page by clicking the Go To Read button in the email**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is subscribed and receives an email with general news</br>- The user is subscribed and receives an email with category, subcategory, or team news|1) Open an email with general news</br>2) Click <b>Go to read</b></br>3) Open an email with category, subcategory, or team news</br>4) Click <b>Go to read</b>|2) The page with general news (<b>Home</b>) is opened</br>4) The page with category, subcategory, or team news is opened|

</details>
