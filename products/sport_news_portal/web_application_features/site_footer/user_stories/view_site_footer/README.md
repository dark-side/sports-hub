### Back to [Site footer of the portal](../../) feature

# Allow users view site footer on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to see a site footer on the every page of the Sport News site with the configured by admin links

## Acceptance criteria

<pre>
<b><i>Scenario: A site user sees the site footer on every page of the Sport News site</i></b>

Given I am a site user

When I view any page on the site 
Then I see a footer containing the following: 
  - Three columns: Company info, Contributors, Newsletter
  - Sport News logo on the left and the copyright section with the links to Privacy Policy / Terms and Conditions pages

When I view the <b>Company info</b> column
Then I see the table contains the following links:
  - About Sport News
  - News / In the Press
  - Advertising / Sports Blogger Ad Network
  - Events
  - Contact Us

When I view the <b>Contributors</b> tab
Then I see the configuration table with the following links:
  - Featured Writers Program
  - Featured Team Writers Program
  - Internship Program

When I click on the <b>Sport News</b> logo
Then I am taken to the home page

When I click on the <b>Privacy Policy / Terms and Conditions</b> links
Then I am taken to the appropriate pages

When I click a link in the <b>Company info</b>, <b>Contributors</b>
Then I am taken to the appropriate pages
</pre>

  <i>The <b>Newsletter</b> is described [in separate feature](/products/sport_news_portal/web_application_features/newsletter_email)</i>

## Mockups

1. User sees site footer in the Sport News site
2. User sees Contact Us page
3. User sees About Sport News page
4. User sees Privacy Policy page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees site footer in the Sport News site:**

![User sees site footer in the Sport News site](/products/sport_news_portal/web_application_features/site_footer/images/site_footer.png)

**2. User sees Contact Us page:**

![User sees Contact Us page](/products/sport_news_portal/web_application_features/site_footer/images/contact_us.png)

**3. User sees About Sport News page:**

![User sees About Sport News page](/products/sport_news_portal/web_application_features/site_footer/images/about_sport_news.png)

**4. User sees Privacy Policy page:**

![User sees Privacy Policy page](/products/sport_news_portal/web_application_features/site_footer/images/privacy_policy.png)

</details>

## Test cases

1. Verify the footer section is visible from any page for users
2. Verify that user can click on the links in the Company info and Contributors columns
3. Verify that user can read Privacy Policy / Terms and Conditions information by click on the Privacy Policy / Terms and Condition
4. Verify that user is redirected to the Home page by click on the Sports News logo

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the footer section is visible from any page for users**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Browse through different pages|1) The footer section is present on every page|

### **#2. Verify that user can click on the links in the Company info and Contributors columns**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the site footer</br>2) In the <b>Company info</b> and <b>Contributors</b> columns, click on the links one by one|2) Links show appropriate info or redirect to appropriate pages|

### **#3. Verify that user can read Privacy Policy / Terms and Conditions information by click on the Privacy Policy / Terms and Conditions links**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the site footer</br>2) Click on the <b>Privacy Policy</b> link</br>3) Click on the <b>Terms and Conditions</b> link|2) The <b>Privacy Policy</b> page opens</br>3) The <b>Terms and Conditions</b> page opens|

### **#4. Verify that user is redirected to the Home page by click on the Sports News logo**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to any page except <b>Home</b></br>2) Go to the site footer</br>3) Click on the <b>Sport News</b> logo|3) User is redirected to the <b>Home</b> page|

</details>
