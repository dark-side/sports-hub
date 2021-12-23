### Back to [Site languages on the portal](../../) feature

# Allow admin user to change a site language on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to change a site language
    So that I can view site pages translated to the preferred language

## Acceptance criteria

<pre>
<b><i>Scenario: Any type of site user (regular or admin) changes a site language</i></b>

Given I am logged in as an admin user

When I view any page on the site
Then I see the site language drop-down icon at the top of the page that opens a list of available languages
<i>Note: English (EN) language should be selected by default</i>

When I click the drop-down icon, and from the drop-down list select the preferred language
Then I see the system translates the site to this language
<i>Note: A list of available languages is configured and managed by admin via the CMS</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see collapsed language drop-down list
2. Users see expanded language drop-down list

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see collapsed language drop-down list:**

![Users see collapsed language drop-down list](/sports_hub_portal/web_application_features/site_languages/images/collapsed_language_dropdown.png)

**2. Users see expanded language drop-down list:**

![Users see expanded language drop-down list](/sports_hub_portal/web_application_features/site_languages/images/expanded_language_dropdown_user_side.png)

</details>

## Test cases

1. Verify the list of available languages in the site language drop-down list for admin
2. Verify selecting the preferred language by admin

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the list of available languages in the site language drop-down list for admin**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Admin configures the <b>UA, DE, FR</b> languages to be shown</br>- Log in with admin account|1) Examine the site language drop-down section</br>2) Check the list of available languages in the site language drop-down list|1) The site language drop-down list is located at the top of the page</br>2) The following languages set by admin are available: <b>EN, UA, DE, FR</b> (English language is selected by default)|

### **#2. Verify selecting the preferred language by admin**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Admin configures the <b>UA, DE, FR</b> languages to be shown</br>- Log in with admin account|1) Examine the site language drop-down section</br>2) Check the list of available languages in the site language drop-down list</br>3) Select the preferred language|1) The site language drop-down list is located at the top of the page</br>2) The following languages set by admin are available: <b>EN, UA, DE, FR</b></br>3) The site is translated into the preferred language|
</details>
