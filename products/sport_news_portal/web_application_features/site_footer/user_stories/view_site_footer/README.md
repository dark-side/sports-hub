### Back to [Site footer of the portal](../../) feature

# Allow users view site footer on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to see a site footer on every page of the Sports Hub site with the links configured by admin

## Acceptance criteria

<pre>
<b><i>Scenario: A site user sees the site footer on every page of the Sports Hub site</i></b>

Given I am a site user

When I view any page on the site 
Then I see a footer containing the following: 
  - Three columns: Company info, Contributors, Newsletter
  - Sports Hub logo on the left and the copyright section with the links to <b>Privacy Policy</b> and <b>Terms and Conditions</b> pages

When I view the <b>Company info</b> column
Then I see the table containing the following links:
  - About Sports Hub
  - News / In the Press
  - Advertising / Sports Blogger Ad Network
  - Events
  - Contact Us

When I view the <b>Contributors</b> tab
Then I see the configuration table with the following links:
  - Featured Writers Program
  - Featured Team Writers Program
  - Internship Program

When I select the <b>Sports Hub</b> logo
Then I am taken to the home page

When I select the <b>Privacy Policy / Terms and Conditions</b> links
Then I am taken to the appropriate pages

When I click a link on the <b>Company info</b>, <b>Contributors</b> tabs
Then I am taken to the appropriate pages
</pre>

  <i>The <b>Newsletter</b> is described [in separate feature](/products/sport_news_portal/web_application_features/newsletter_email)</i>

## Mockups

1. Users see site footer in the Sports Hub site
2. Users see the <b>Contact Us</b> page
3. Users see the <b>About Sports Hub</b> page
4. Users see the <b>Privacy Policy</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see site footer in the Sports Hub site:**

![Users see site footer in the Sports Hub site](/products/sport_news_portal/web_application_features/site_footer/images/site_footer.png)

**2. Users see the Contact Us page:**

![Users see the Contact Us page](/products/sport_news_portal/web_application_features/site_footer/images/contact_us.png)

**3. Users see the About Sports Hub page:**

![Users see the About Sports Hub page](/products/sport_news_portal/web_application_features/site_footer/images/about_sport_news.png)

**4. Users see the Privacy Policy page:**

![Users see the Privacy Policy page](/products/sport_news_portal/web_application_features/site_footer/images/privacy_policy.png)

</details>

## Test cases

1. Verify that footer section is visible from any page for users
2. Verify that users can click on the links in the <b>Company info</b> and <b>Contributors</b> columns
3. Verify that users can read Privacy Policy / Terms and Conditions information by clicking the <b>Privacy / Terms</b>
4. Verify that users are redirected to the home page by selecting the Sports Hub logo

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that footer section is visible from any page for users**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Browse through different pages|1) The footer section is present on every page|

### **#2. Verify that users can click on the links in the Company info and Contributors columns**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the site footer</br>2) In the <b>Company info</b> and <b>Contributors</b> columns, select the links one by one|2) Links show appropriate info or redirect to appropriate pages|

### **#3. Verify that users can read Privacy Policy / Terms and Conditions information by clicking the Privacy / Terms**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the site footer</br>2) Select the <b>Privacy Policy</b> link</br>3) Select the <b>Terms and Conditions</b> link|2) The <b>Privacy Policy</b> page opens</br>3) The <b>Terms and Conditions</b> page opens|

### **#4. Verify that users are redirected to the home page by selecting the Sports Hub logo**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to any page except <b>Home</b></br>2) Go to the site footer</br>3) Select the <b>Sports Hub</b> logo|3) The user is redirected to the home page|

</details>
