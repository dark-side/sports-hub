### Back to [Application languages](../../README.md) feature

# Allow users to view the application in supported languages

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an application user
    I want to be able to view the application in supported languages

## Acceptance criteria

<pre>
<b><i>Scenario: A user changes a language</i></b>

Given I am logged in as a user

When I view any page of the application
Then I see the application content is translated into the language that is selected on my phone

When the application does not support the language of my phone
Then I see the application in English

<i>Note: A list of supported languages is configured and managed by admin via the CMS</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a list of avaliable languages

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a list of avaliable languages:**

![Users see a list of avaliable languages](/sports_hub_portal/mobile_application_features/application_languages/images/application_languages_list.png)

</details>

## Test cases

1. Verify the content gets translated
2. Verify selecting the phone language that is supported in the application

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content gets translated**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- Go to any page</br>- The application supports EN, UA, DE, FR languages|1) Select phone lagnuage as one of the supported list</br>2) Examine the app content|1) The application content is translated into the language that is selected on my phone|

### **#2. Verify selecting the phone language that is supported in the application**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The application supports EN, UA, DE, FR languages|1) Select phone lagnuage that is NOT present in the supported list</br>2) Examine the app content</br>3) Tap the preferred language icon|The application content is translated into English|
</details>
