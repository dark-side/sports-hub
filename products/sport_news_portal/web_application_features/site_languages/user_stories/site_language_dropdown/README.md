### Back to [Site Languages on the portal](../../) feature

# Allow users to change a site language on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to change a site language 
    So that I can view site pages translated to a prefered language

## Acceptance criteria

    Scenario: A site user changes a site language
    Given I am logged in as a site user

    When I view any page of the site
    Then I see a Site Language dropdown at the top of the page with a list of available languages
    Note: English (EN) language should be selected by default
    When I click on dropdown and select the prefered language
    Then I see the system translates site to it
    Note: A list of available languages is configured and managed by Admin via the CMS

## Mockups

1. User sees collapsed language dropdown
2. User sees expanded language dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees collapsed language dropdown:**

![Collapsed language dropdown](/products/sport_news_portal/web_application_features/site_languages/images/collapsed_language_dropdown.png)

**2. User sees expanded language dropdown:**

![Expanded language dropdown](/products/sport_news_portal/web_application_features/site_languages/images/expanded_language_dropdown.png)

</details>

## Test Scenarios

1. Verify Site Language dropdown
2. Verify list of available languages in Site Language dropdown
3. Verify default languages in Site Language dropdown
4. Verify selecting the prefered language

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify Site Language dropdown**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe Site Language dropdown|A Site Language dropdown at the top of the page

### **#2. Verify list of available languages in Site Language dropdown**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe Site Language dropdown|A Site Language dropdown at the top of the page
|4|Check the list of available languages in Site Language dropdown|Languages set by admin are available:<br> - EN<br> - UA<br> - DU<br> - FR

### **#3. Verify default languages in Site Language dropdown**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe Site Language dropdown|A Site Language dropdown at the top of the page
|4|Check the list of available languages in Site Language dropdown|Languages set by admin are available:<br> - EN<br> - UA<br> - DU<br> - FR
|5|Observe what language is set by default|English language is set by default

### **#4. Verify selecting the prefered language**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe Site Language dropdown|A Site Language dropdown at the top of the page
|4|Check the list of available languages in Site Language dropdown|Languages set by admin are available:<br> - EN<br> - UA<br> - DU<br> - FR
|5|Select the prefered language|The system translates site to prefered language

</details>
