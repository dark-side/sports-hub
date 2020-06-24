### Back to [Site Footer of the portal](../../) feature

# Allow users view site footer on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to see a site Footer on the every page of the Sport News site
    So that I can see link to pages to read more about the company, contributors and subscribe to receive latest news

## Acceptance criteria

    Scenario: A site user sees a site Footer on the every page of the Sport News site
    Given I am logged in as a site user

    When I am view any page on the site
    Then I see a footer containing the following:
      - Three columns: COMPANY INFO, CONTRIBUTORS, NEWSLETTER
      - Block with a Sport News logo at the left and a Copyright section with link to  Privacy / Terms page
        And I see the COMPANY INFO column consists of the following links:
          - About Sport News
          - News / In the Press
          - Advertising / Sports Blogger Ad Network
          - Events
          - Contact Us
        And I see the CONTRIBUTORS column consists of the following links:
      - Featured Writers Program
      - Featured Team Writers Program
      - Internship Program
        And I see the NEWSLETTER column consists of the “Sign up to receive the latest in sport news” form containing the input for the email address followed by a Subscribe button and the Facebook or Google+ sign up link
        And I see the pages that appear in the site footer are controlled by admin in the CMS
    When I click on the Sport News logo
    Then I am taken to the site’s home page
    When I click a link in the Company Info, Contributors, or Copyright section
    Then I see the dialog with “Coming Soon“ message and close icon
        And I can type my email in the Email Newsletter signup input and click Subscribe button
        And I see the Facebook or Google+ subscription links

## Mockups

1. User sees Site Footer with Contact Us page
2. User sees Site Footer with About Us page
3. User sees Coming soon popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Site Footer with Contact Us page:**

![Site Footer with Contact Us page Screen](/products/sport_news_portal/web_application_features/site_footer/images/site_footer_contact_us.png)

**2. User sees Site Footer with About Us page:**

![Site Footer with About Us page Screen](/products/sport_news_portal/web_application_features/site_footer/images/site_footer_about_us.png)

**3. User sees Coming soon popup:**

![Coming soon popup](/products/sport_news_portal/web_application_features/site_footer/images/coming_soon_popup.png)

</details>

## Test Scenarios

1. Verify that footer configuration page shows three tabs
2. Verify that COMPANY INFO display required rows (footer links)
3. Verify that the CONTRIBUTORS tab displays required rows
4. Verify the NEWSLETTER tab displays configuration table with a single row

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that footer configuration page shows three tabs**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Examine tabs on footer configuration page|The system shows three tabs:<br>- COMPANY INFO<br>- CONTRIBUTORS<br>- NEWSLETTER

### **#2. Verify that COMPANY INFO display required rows (footer links)**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Examine COMPANY INFO rows (footer links) tab on footer configuration page|The COMPANY INFO displays the following rows (footer links):<br>- About Sport News<br>- News / In the Press<br>- Advertising / Sports Blogger Ad Network<br>- Events<br>- Contact Us

### **#3. Verify that the CONTRIBUTORS tab displays required rows**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Examine rows that are displayed in CONTRIBUTORS tab|The system displays configuration table with the following rows:<br>- Featured Writers Program<br>- Featured Team Writers Program<br>- Internship Program

### **#4. Verify the NEWSLETTER tab displays configuration table with a single row**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Examine NEWSLETTER tab table|The system displays configuration table with a single row:<br>- "Sign up to receive the  latest in sport news"
|4|Verify the input for the email address|"Sign up to receive the latest in sport news" form contains the input for the email address
|5|Verify Subscribe button|Subscribe button is present
|6|Verify the Facebook or Google+ sign up link|The Facebook or Google+ sign up link is present

</details>
