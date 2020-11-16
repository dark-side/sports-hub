### Back to [Newsletter subscription](../../) feature

# Allow users to receive newsletter email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to receive a newsletter email and navigate to the appropriate site page
    So that I can read the latest sports news on the site

## Acceptance criteria

<pre>
Scenario: A site user receives a newsletter email and clicks the Go To Read button
Given I am logged in as a site user

When I receive newsletter email about sport news
Then I see the <b>Go To Read</b> button

When I click the <b>Go To Read</b> button in the general news email
Then I am taken to the <b>Home</b> page of the Sport News site 

When I click the <b>Go To Read</b> button in the sports category/subcategory/team news email
Then I am taken to a sports category, subcategory, or team page of the Sport News site
</pre>

## Mockups

1. User sees an email after newsletter subscribe

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees an email after newsletter subscribe:**

![User sees an email after newsletter subscribe](/products/sport_news_portal/web_application_features/newsletter_email/images/news_email.png)

</details>

## Test cases

1. Verify that the user is redirected to the appropriate page by click on the Go To Read button in the email

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is redirected to the appropriate page by click on the Go To Read button in the email**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is subscribed and received an email with general news</br>- The user is subscribed and received an email with category, subcategory, or team news|1) Open an email with general news</br>2) Click <b>Go to read</b></br>3) Open an email with category, subcategory, or team news</br>4) Click <b>Go to read</b>|2) The page with general news (<b>Home</b>) is opened</br>4) The page with category, subcategory, or team news is opened|
</details>
