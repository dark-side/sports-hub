### Back to [Site Footer of the portal](../../) feature

# Allow admin users to configure site footer

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to configure the columns of a site Footer and the content of these columns
    So that I have control over the links/columns visible by the site users

## Acceptance criteria

    Scenario: An admin user configures the columns of a site Footer and the content of these columns
    Given I am logged in as an admin user

    When I am on Footer configuration page
    Then I see a three tabs - COMPANY INFO, CONTRIBUTORS, NEWSLETTER with a list of a configurable tab links and a Show All Section toggle
        And I see the COMPANY INFO tab is active by default
        And I see the active tab name is highlighted
    When I view the COMPANY INFO tab
    Then I see the configuration table with the following columns:
      - FOOTER MENU NAMES
      - HIDE/SHOW
      - ACTIONS
        And I see the table contains the following rows (footer links):
          - About Sport News
          - News / In the Press
          - Advertising / Sports Blogger Ad Network
          - Events
          - Contact Us
        And I can configure which links are visible to the site users by clicking Hide/Show toggle
    When I hover over the table row (footer link)
    Then I see it is highlighted
        And I see a Delete icon for the hovered table row (footer link)
    When I click the Delete icon
    Then I see the appropriate item is deleted
        And I see it is no longer available for Admin configuration
        And I see it is not visible for the site users
    When I disable the Show All Section toggle
    Then I see the whole COMPANY INFO tab is not visible for the site users
    When I enable the Show All Section toggle
    Then I see the COMPANY INFO tab is visible for the site users
        And I see it contains links listed in the configuration table that are in the Show state
    When I view the CONTRIBUTORS tab
    Then I see the configuration table with the following rows:
      - Featured Writers Program
      - Featured Team Writers Program
      - Internship Program
        And I can configure this tab the same way as the COMPANY INFO tab
    When I view the NEWSLETTER tab
    Then I see the configuration table with a single row:
      - Sign up to receive the latest in sport news
    When I enable the Show/Hide toggle in the configuration table
    Then I see the “Sign up to receive the latest in sport news” form is visible for a site users
    When I disable the Show/Hide toggle in the configuration table
    Then I see the “Sign up to receive the latest in sport news” form is not visible for a site users
    When I disable the Show All Section toggle
    Then I see the whole NEWSLETTER tab is not visible for the site users
    When I enable the Show All Section toggle
    Then I see the NEWSLETTER is visible for the site users
        And I see it contains the “Sign up to receive the latest in sport news” form if it has Show state in the configuration table
    When I hover over the table row
    Then I see it is highlighted
        And I see a Delete icon for the hovered table row
    When I click the Delete icon
    Then I see the appropriate item is deleted
        And I see it is no longer available for Admin configuration
        And I see it is not visible for the site users

## Mockups

1. User sees Company Info -> About Sport News configuration page
2. User sees Company Info -> Contact Us configuration page
3. User sees Contributors configuration page
4. User sees Newsletter subscription configuration page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Company Info -> About Sport News configuration page:**

![Company Info -> About Sport News configuration page Screen](/products/sport_news_portal/web_application_features/site_footer/images/configure_sport_news_about_us.png)

**2. User sees Company Info -> Contact Us configuration page:**

![Company Info -> Contact Us configuration page Screen](/products/sport_news_portal/web_application_features/site_footer/images/configure_sport_news_contact_us.png)

**3. User sees Contributors configuration page:**

![Contributors configuration page Screen](/products/sport_news_portal/web_application_features/site_footer/images/configure_sport_news_contributors.png)

**4. User sees Newsletter subscription configuration page:**

![Newsletter subscription configuration page Screen](/products/sport_news_portal/web_application_features/site_footer/images/configure_sport_newsletter.png)

</details>

## Test Scenarios

1. Verify that footer configuration page shows three tabs
2. Verify the COMPANY INFO tab is active by default
3. Verify that COMPANY INFO display required columns
4. Verify that COMPANY INFO display required rows (footer links)
5. Verify admin can сonfigure which links are visible to the site user
6. Verify that admin can enable the Show All Section in COMPANY INFO tab
7. Verify that admin can disable the Show All Section in COMPANY INFO tab
8. Verify that the CONTRIBUTORS tab displays required rows
9. Verify that admin can enable the Show All Section in CONTRIBUTORS tab
10. Verify that admin can disable the Show All Section in CONTRIBUTORS tab
11. Verify the NEWSLETTER tab displays configuration table with a single row
12. Verify that admin can enable the Show/Hide toggle in the NEWSLETTER tab configuration table
13. Verify that admin can disable the Show/Hide toggle in the NEWSLETTER tab configuration table
14. Verify that admin can Delete icon for the hovered table row

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that footer configuration page shows three tabs**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Examine tabs on footer configuration page|The system shows three tabs:<br>- COMPANY INFO<br>- CONTRIBUTORS<br>- NEWSLETTER

### **#2. Verify the COMPANY INFO tab is active by default**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Examine COMPANY INFO tab on footer configuration page|The COMPANY INFO tab is active by default and the active tab name is highlighted

### **#3. Verify that COMPANY INFO display required columns**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Examine COMPANY INFO tab on footer configuration page|The COMPANY INFO displays the following columns:<br>- FOOTER MENU NAMES<br>- HIDE/SHOW<br>- ACTIONS

### **#4. Verify that COMPANY INFO display required rows (footer links)**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Examine COMPANY INFO rows (footer links) tab on footer configuration page|The COMPANY INFO displays the following rows (footer links):<br>- About Sport News<br>- News / In the Press<br>- Advertising / Sports Blogger Ad Network<br>- Events<br>- Contact Us

### **#5. Verify admin can сonfigure which links are visible to the site user**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Hover over the table row (footer link)|Table row (footer link) becomes highlighted
|4|Click on Delete icon for the hovered table row (footer link)|The appropriate item is deleted and no longer available for Admin configuration
|5|Log out from your admin account|
|6|Log in to test user account|
|7|Examine if deleted footer link is visible for site user|The appropriate item is not visible for the site user

### **#6. Verify that admin can enable the Show All Section in COMPANY INFO tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to COMPANY INFO tab|
|4|Disable the Show All Section toggle|
|5|Log out from admin account|
|6|Log in to user account|
|7|Examine if the Show All Section toggle works correctly|The whole COMPANY INFO tab is not visible for the site users

### **#7. Verify that admin can disable the Show All Section in COMPANY INFO tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to COMPANY INFO tab|
|4|Enable the Show All Section toggle|
|5|Log out from admin account|
|6|Log in to user account|
|7|Examine if the Show All Section toggle works correctly|The whole COMPANY INFO tab is visible for the site users contains links listed in the configuration table that are in the Show state

### **#8. Verify that the CONTRIBUTORS tab displays required rows**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Examine rows that are displayed in CONTRIBUTORS tab|The system displays configuration table with the following rows:<br>- Featured Writers Program<br>- Featured Team Writers Program<br>- Internship Program

### **#9. Verify that admin can enable the Show All Section in CONTRIBUTORS tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to CONTRIBUTORS tab|
|4|Disable the Show All Section toggle|
|5|Log out from admin account|
|6|Log in to user account|
|7|Examine if the Show All Section toggle works correctly|The whole CONTRIBUTORS tab is not visible for the site users

### **#10. Verify that admin can disable the Show All Section in CONTRIBUTORS tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to CONTRIBUTORS tab|
|4|Disable the Show All Section toggle|
|5|Log out from admin account|
|6|Log in to user account|
|7|Examine if the Show All Section toggle works correctly|The whole CONTRIBUTORS tab is not visible for the site users contains links listed in the configuration table that are in the Show state

### **#11. Verify the NEWSLETTER tab displays configuration table with a single row**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Examine NEWSLETTER tab table|The system displays configuration table with a single row:<br>- Sign up to receive the latest in sport news

### **#12. Verify that admin can enable the Show/Hide toggle in the NEWSLETTER tab configuration table**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to the NEWSLETTER tab|
|4|Disable the Show/Hide toggle|
|5|Log out from admin account|
|6|Log in to user account|
|7|Examine if the the "Sign up to receive the latest in sport news" form is visible for a site users|The "Sign up to receive the latest in sport news" form is visible for a site users

### **#13. Verify that admin can disable the Show/Hide toggle in the NEWSLETTER tab configuration table**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to the NEWSLETTER tab|
|4|Disable the Show/Hide toggle|
|5|Log out from admin account|
|6|Log in to user account|
|7|Examine if the Show All Section toggle works correctly|The whole NEWSLETTER tab is not visible for the site users contains links listed in the configuration table that are in the Show state

### **#14. Verify that admin can Delete icon for the hovered table row**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Go to any footer’s table row|
|4|Hover over the table row|Table row becomes highlighted and Delete icon for the hovered table row appears
|5|Click Delete Item|The appropriate item is deleted and it is no longer available for Admin configuration
|6|Log out from your admin account|
|7|Log in to the user account|
|8|Examine if table row is visible for the site user|Deleted appropriate item is not visible for the site users

</details>
