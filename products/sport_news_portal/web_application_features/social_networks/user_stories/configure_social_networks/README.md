### Back to [Social Networks on the portal](../../) feature

# Allow admin user to configure social networks on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to configure which Social Networks are integrated into Sport News site
    So that users can use them to login/sign up/share/follow Sport News site

## Acceptance criteria

    Scenario: An admin user configures which Social Networks are integrated into Sport News site
    Given I am logged in as an admin user

    When I view a social networks configuration page
    Then I see a three tabs available for configuration - Share, Follow, Login/Sign Up
    When I am on the Share tab
    Then I see the following:
      - Facebook, Twitter, Google + social networks list that can be used for sharing a Sport News page
      - A toggle to activate/inactivate specific social network
      - A Show all section toggle
    When I deactivate any of the social network from the list
    Then I see it is no longer shown on the header section of the main site
    When I deactivate the Show all section toggle
    Then I see the whole Share section is no longer shown on the header section of the main site
    When I click on the Follow tab
    Then I see the following:
      - Facebook, Twitter, Google +, Youtube social networks list that can be used for following the Sport News page on the social networks 
      - A toggle to activate/deactivate specific social network 
      - A Show all section toggle
    When I deactivate any of the social network from the list
    Then I see it is no longer shown on the Navigation Menu of the main site
    When I deactivate the Show all section toggle
    Then I see the whole Follow section is no longer shown on the Navigation Menu of the main site
    When I click on the Login/Sign Up tab
    Then I see the following:
      - Facebook and Google + social networks list that can be used for login/sign up
      - A toggle to activate/deactivate specific social network
      - A Show all section toggle
    When I deactivate any of the social network from the list
    Then I see it is no longer shown on the Login/Sign Up page and in the Sign Up to news section in the Footer section of the main site
    When I deactivate the Show all section toggle
    Then I see the whole Follow section is no longer shown on the main site

## Mockups

1. Admin user sees Share configuration page
2. Admin user sees Follow configuration page
3. Admin user sees Login/Sign Up with social networks configuration page
4. User sees Share icons and Follow icons on the regular page of the portal
5. User sees Login page with Sotial Network icons
6. User sees Sign Up page with Sotial Network icons
7. User sees Login by Facebook example

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Share configuration page:**

![Share configuration page](/products/sport_news_portal/web_application_features/social_networks/images/sharing_configuration_page.png)

**2. Admin user sees Follow configuration page:**

![Follow configuration page](/products/sport_news_portal/web_application_features/social_networks/images/following_configuration_page.png)

**3. Admin user sees Login/Sign Up with social networks configuration page:**

![Login/Sign Up with social networks configuration page](/products/sport_news_portal/web_application_features/social_networks/images/login_signup_using_social_networks_configuration_page.png)

**4. User sees Share icons and Follow icons on the regular page of the portal:**

![Share icons and Follow icons on the page](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

**5. User sees Login page with Sotial Network icons:**

![Login page with Sotial Network icons](/products/sport_news_portal/web_application_features/social_networks/images/login_page_with_sotial_network_icons.png)

**6. User sees Sign Up page with Sotial Network icons:**

![Sign Up page with Sotial Network icons](/products/sport_news_portal/web_application_features/social_networks/images/signup_page_with_sotial_network_icons.png)

**7. User sees Login by Facebook example:**

![Login by Facebook example](/products/sport_news_portal/web_application_features/social_networks/images/login_by_facebook_example.png)

</details>

## Test Scenarios

1. Verify the tabs on a Social Network page
2. Verify the content of share tab on a Social Network page
3. Verify deactivating of social network from the list
4. Verify deactivating the Show all section toggle
5. Verify the content of the Follow tab on a Social Network page
6. Verify deactivating of social network from the list on Follow tab
7. Verify deactivating of the Show all section from the list on Follow tab
8. Verify the content of the Login/Sign Up tab on a Social Network page
9. Verify deactivating of social network from the list on the Login/Sign Up tab
10. Verify deactivating of the Show all section from on the Login/Sign Up tab

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the tabs on a Social Network page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Observe the tabs on a page|Three tabs are available for configuration - Share, Follow, Login/Sign Up
The Share tab is open as default


### **#2. Verify the content of share tab on a Social Network page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Observe the content of Share tab|The following is shown:<br> - Facebook, Twitter, Google +, Youtube social networks list that can be used for following the Sport News page on the social networks<br> - A toggle to activate/deactivate specific social network<br> - A Show all section toggle

### **#3. Verify deactivating of social network from the list**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Go to Share tab|
|5|Toggle to deactivate any social network from the list|
|6|Go to Navigation Menu of the main site|The whole Share section is no longer shown on the Navigation Menu of the main site

### **#4. Verify deactivating the Show all section toggle**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Go to Share Tab|
|5|Toggle to deactivate the Show all section toggle|
|6|Go to Navigation Menu of the main site|It is no longer shown on the header section of the main site

### **#5. Verify the content of the Follow tab on a Social Network page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Observe the content of Follow tab|The following is shown:<br> - Facebook, Twitter, Google +, Youtube social networks list that can be used for following the Sport News page on the social networks<br> - A toggle to activate/deactivate specific social network<br> - A Show all section toggle

### **#6. Verify deactivating of social network from the list on Follow tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Go to the Follow tab|
|5|Toggle to deactivate any social network from the list|
|6|Go to Navigation Menu of the main site|It is no longer shown on the Navigation Menu of the main site

### **#7. Verify deactivating of the Show all section from the list on Follow tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Go to the Show all tab|
|5|Toggle to deactivate the Show all section from the list|It is no longer shown on the Navigation Menu of the main site
|6|Go to Navigation Menu of the main site|The whole Follow section is no longer shown on the Navigation Menu of the main site

### **#8. Verify the content of the Login/Sign Up tab on a Social Network page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Observe the content of the Login/Sign Up tab|The following is shown:<br> - Facebook and Google + social networks list that can be used for login/sign up<br> - A toggle to activate/deactivate specific social network<br> - A Show all section toggle

### **#9. Verify deactivating of social network from the list on the Login/Sign Up tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Go to the Login/Sign Up tab|
|5|Toggle to deactivate any social network from the list|
|6|Go to Navigation Menu of the main site|It is no longer shown on the Navigation Menu of the main site

### **#10. Verify deactivating of the Show all section from on the Login/Sign Up tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Social Network Icon in the left sidebar|
|4|Go to the Login/Sign Up tab|
|5|Toggle to deactivate the Show all section from the list|It is no longer shown on the Navigation Menu of the main site
|6|Go to Navigation Menu of the main site|The whole Show all section section is no longer shown on the Navigation Menu of the main site

</details>
