### Back to [Newsletter subscription](../../) feature

# Allow users to subcribe to newsletter

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to subscribe to a Sport News site
    So that I can receive an email with the latest sports news

## Acceptance criteria

<pre>
Scenario: A site user subscribes to a Sport News site
Given I am a site user

When I view the page and the <b>Newsletter</b> subscription section in the site footer
Then I see the following:
  - Newsletter heading
  - <b>Sign up to receive the latest in sport news</b> label
  - Input for an email address
  - <b>Subscribe</b> button

When I enter an email address and click <b>Subscribe</b>
Then I see the popup with notification about the subscribed news category

When I receive newsletter email about sport news
Then I see the <b>Go To Read</b> button

When I click the <b>Go To Read</b> button in the general news email
Then I am taken to the <b>Home</b> page of the Sport News site 

When I click the <b>Go To Read</b> button in the sports category/subcategory/team news email
Then I am taken to a sports category, subcategory, or team page of the Sport News site

<i>NOTE: The subscription depends on the section of the site you are currenntly on, for example:
  - Home page – subscription to all general sports news
  - NBA sport category page – subscription to NBA news
  - Los Angeles Lakers team page – subscription to Los Angeles Lakers team news</i>
</pre>

## Mockups

1. User sees a newsletter section in the site footer
2. User sees a successful subscription popup with details
3. User sees an email after newsletter subscribe

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a newsletter section in the site footer:**

![User sees a newsletter section in the site footer](/products/sport_news_portal/web_application_features/newsletter_email/images/site_footer.png)

**2. User sees a successful subscription popup with details:**

![User sees a successful subscription popup with details](/products/sport_news_portal/web_application_features/newsletter_email/images/successful_subscription.png)

**3. User sees an email after newsletter subscribe:**

![User sees an email after newsletter subscribe](/products/sport_news_portal/web_application_features/newsletter_email/images/news_email.png)

</details>

## Test cases

1. Verify the Subscribe button functionality for the Home page
2. Verify the Subscribe button functionality on any opened page
3. Verify that the user is redirected to the appropriate page by click on the Go To Read button in the email

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the Subscribe button functionality for the Home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the site footer -> <b>Newsletter</b>|1) In the <b>Your email address</b> field, enter an email address</br>2) Click <b>Subscribe</b></br>3) Verify that the user is subscribed to all general sports news|2) The popup appears with a notification that the user is subscribed to all general sports news</br>3) User receives an email with the latest news from all categories on a daily basis|

### **#2. Verify the Subscribe button functionality on any opened page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the <b>NBA</b> league page/<b>Los Angeles Lakers</b> team page</br>- On the site footer -> <b>Newsletter</b>|1) In the <b>Your email address</b> field, enter the user email address</br>2) Click <b>Subscribe</b></br>3) Verify that the user is subscribed to <b>NBA</b> league/<b>Los Angeles Lakers</b> team news|2) The popup appears with a notification that the user is subscribed to <b>NBA</b> league/<b>Los Angeles Lakers</b> team news</br>3) User receives an email with the latest news from the appropriate category/team page on a daily basis|

### **#3. Verify that the user is redirected to the appropriate page by click on the Go To Read button in the email**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is subscribed and received an email with general news</br>- The user is subscribed and received an email with category, subcategory, or team news|1) Open an email with general news</br>2) Click <b>Go to read</b></br>3) Open an email with category, subcategory, or team news</br>4) Click <b>Go to read</b>|2) The page with general news (<b>Home</b>) is opened</br>4) The page with category, subcategory, or team news is opened|

</details>
