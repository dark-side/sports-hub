### Back to [Site languages on the portal](../../README.md) feature

# Allow admin to configure content in multiple languages

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to configure content in multiple languages
    So that users can translate the site to valaiable languages

## Acceptance criteria

<pre>
<b><i>Scenario: Admin user configures any content in multiple languages</i></b>

Given I am logged in as admin user

When I view configuration page with any content (articles, videos, home page, surveys, banners, footer)
Then I see a list of added languages at the top of the working area (They are configured on the <b>Site languages</b> tab)
  And <b>English</b> is listed first and selected by default

When language is added but not enabled
Then I see <b>hidden</b> label for that language

When I hover over the <b>hidden</b> label
Then I see the text: "This language is turned off. Go to the <b>Language page</b> to turn it on"
  And <b>Language page</b> text is a link to language configuration page

When I enter all content details (for articles, videos, home page, surveys, banners, footer) and click <b>Save</b>
Then the corresponding translation is saved to the database

When I go to edit any content (articles, videos, home page, surveys, banners, footer) and switch between different languages
Then I see the content is translated to the selected language
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees a list of added languages on the <b>Home</b> configuration page
2. Admin user sees a big list of added languages on the surveys configuration page
3. Admin user sees hovers over the hidded language and sees a popup
4. Admin user sees a list of added languages on any article configuration page
5. Admin user sees a list of added languages on the banners configuration page
6. Admin user sees a list of added languages on the videos configuration page
7. Admin user sees a list of added languages on the surveys configuration page
8. Admin user sees a list of added languages on the footer configuration page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a list of added languages on the <b>Home</b> configuration page:**

![Admin user sees a list of added languages on the <b>Home</b> configuration page](/web_application_features/site_languages/images/list_of_languages_home_page.png)

**2. Admin user sees a big list of added languages on the surveys configuration page:**

![Admin user sees a big list of added languages on the surveys configuration page](/web_application_features/site_languages/images/lots_of_languages.png)

**3. Admin user sees hovers over the hidded language and sees a popup:**

![Admin user sees hovers over the hidded language and sees a popup](/web_application_features/site_languages/images/hover_over_hidden_language.png)

**4. Admin user sees a list of added languages on any article configuration page:**

![Admin user sees a list of added languages on any article configuration page](/web_application_features/site_languages/images/list_of_languages_articles_page.png)

**5. Admin user sees a list of added languages on the banners configuration page:**

![Admin user sees a list of added languages on the banners configuration page](/web_application_features/site_languages/images/list_of_languages_banners_page.png)

**6. Admin user sees a list of added languages on the videos configuration page:**

![Admin user sees a list of added languages on the videos configuration page](/web_application_features/site_languages/images/list_of_languages_videos_page.png)

**7. Admin user sees a list of added languages on the surveys configuration page:**

![Admin user sees a list of added languages on the surveys configuration page](/web_application_features/site_languages/images/list_of_languages_surveys_page.png)

**8. Admin user sees a list of added languages on the footer configuration page:**

![Admin user sees a list of added languages on the footer configuration page](/web_application_features/site_languages/images/list_of_languages_footer_page.png)

</details>

## Test cases

1. Verify the list of added languages on the articles, videos, home page, surveys, banners, footer configuration pages
2. Verify the hover text for the hidded language
3. Verify the configuration context is changing when select a different language

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the list of added languages on the articles, videos, home page, surveys, banners, footer configuration pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Admin configured the <b>French</b> language to be shown and <b>German</b> to be hidden</br>|1) Examine the context of the articles, videos, home page, surveys, banners, footer configuration pages|1) The list of added languages <b>EN, DE, FR</b> is rendeed at the top of the working area. <b>English</b> language is selected by default|

### **#2. Verify the hover text for the hidded language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Admin configured the <b>German</b> language to be hidden</br>|1) Hover over the hidden language|1) The popup with the valid text appear|

### **#3. Verify the configuration context is changing when select a different language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Admin configured the <b>French</b> language to be shown|1) Switch between <b>EN</b> and <b>FR</b>|1) The content form is translated into a selected language|
</details>
