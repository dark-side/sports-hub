### Back to [Application languages](../../) feature

# Allow users to change a language in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an application user
    I want to be able to change an application language
    So that I can view all application content translated to a preferred language

## Acceptance criteria

<pre>
<b><i>Scenario: A user changes a language</i></b>

Given I am logged in as a user

When I view any page of the application
Then I see the Main menu

When I tap Main menu icon
Then I see the languages list in the right bottom corner
<i>Note: English (EN) language should be selected by default</i>

When I tap any preferred language icon
Then I see the application content is translated into this language

<i>Note: A list of available languages is configured and managed by admin via the CMS</i>
</pre>

## Mockups

1. Users see a list of avaliable languages

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a list of avaliable languages:**

![Users see a list of avaliable languages](/products/sports_hub_portal/mobile_application_features/application_languages/images/application_languages_list.png)

</details>

## Test cases

1. Verify the list of available languages in the Main menu
2. Verify selecting the preferred language by users

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the list of available languages in the Main menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- Go to any page</br>- There are configured EN, UA, DE, FR languages to be shown</br>- The user has never changed the language|1) Tap the Main menu icon</br>2) Examine the list of available languages|1) The languages list is placed in the right bottom corner</br>2) The following languages are available: EN, UA, DE, FR. English language is selected by default|

### **#2. Verify selecting the preferred language by users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are configured EN, UA, DE, FR languages to be shown|1) Tap the Main menu icon</br>2) Examine the list of available languages</br>3) Tap the preferred language icon|1) The languages list is placed in the right bottom corner</br>2) The following languages are available: EN, UA, DE, FR</br>3) The application content is translated into a preferred language|
</details>
