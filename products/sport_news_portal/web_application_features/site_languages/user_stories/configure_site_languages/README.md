### Back to [Site Languages on the portal](/../../) feature

# Allow admin user to configure site languages on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to configure list of available site languages 
    So user can select prefered language for the Sport News site

## Acceptance criteria

    Scenario: An admin user configures list of available site languages
    Given I am logged in as an admin user

    When I view Language configuration page
    Then I see a table with list of languages available for the Sport News site and a language status toggle
    When I hover over some language 
    Then I see a Delete language icon
    When I click on Delete language icon
    ThenI see the language is deleted from the list
    When I click on language status toggle
    Then I see the language is activated/deactivated
    Note: when language is in deactivated state, it’s not shown in the Site Languages Dropdown in the site Header
    When I view Language configuration page
    Then I see a New Language button right to the Languages page title
    When I click on New Language button
    Then I see the system opens an Add Language modal with a Select Language multi select input And Add and Cancel buttons for the modal
    When I select list of the languages I want to make available on the site and click the Add button
    Then I see the new languages are displayed on the languages table
    When I click on Cancel button on the Add Language modal
    Then I see the Add Language modal is closed and no new languages appear on the table

## Mockups

1. Admin user sees configaration site languages page
2. Admin user sees "Add Language" popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees configaration site languages page:**

![Configaration site languages page](/products/sport_news_portal/web_application_features/site_languages/images/configaration_site_languages.png)

**2. Admin user sees "Add Language" popup:**

!["Add Language" popup](/products/sport_news_portal/web_application_features/site_languages/images/add_language_popup.png)

</details>

## Test Scenarios

1. Verify content of Language configuration page
2. Verify deleting the language
3. Verify the language being activated/deactivated
4. Verify the New Language button
5. Verify the Add Language button
6. Verify the Cancel Language button

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify content of Language configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to the Language configuration page|
|4|Observe the content of Language configuration page|A table with list of languages available for the Sport News site and a language status toggle are present on the Language configuration page

### **#2. Verify deleting the language**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to the Language configuration page|
|4|Hover over some language|Delete language icon appears
|5|Click on Delete language icon|The language is deleted from the list

### **#3. Verify the language being activated/deactivated**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to the Language configuration page|
|4|Click on language status toggle|The language is activated/deactivated

### **#4. Verify the New Language button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Language configuration page|
|4|Click on New Language button|Add Language modal with a Select Language multi select input is opened

### **#5. Verify the Add Language button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Language configuration page|
|4|Click on New Language button|
|5|Select list of the languages to make available on the site| 
|6|Click the Add button|The new languages are displayed on the languages table

### **#6. Verify the Cancel Language button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Language configuration page|
|4|Click on New Language button|
|5|Select list of the languages to make available on the site|
|6|Click on Cancel button|The Add Language modal is closed and no new languages appear on the table

</details>
