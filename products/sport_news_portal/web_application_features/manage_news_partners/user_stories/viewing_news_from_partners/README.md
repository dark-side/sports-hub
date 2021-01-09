### Back to [Manage news partners on the portal](../../) feature

# Allow site user to view news from the configured partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to see the news from the configured partners in the appropriate categories

## Acceptance criteria

<pre>
<b><i>Scenario: An user is browsing different category pages and the Home page</i></b>

Given I am a site user

When I view the <b>Home</b> page
Then I see the news from the configured news partner
  And this news is shown among news created by admin according to the creation date

When I view any category page
Then I see the news from the configured news partner
  And this news is shown among news created by admin according to the creation date
</pre>

## Mockups

1. User sees articles list

<details>
  <summary>Click here to see mockups details</summary>

![User user sees articles list](/products/sport_news_portal/web_application_features/manage_news_partners/images/user_side_articles_list.png)

</details>

## Test cases

1. Verify that news from news partner are shown according to the creation date

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that news from news partner are shown according to the creation date**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There is some partner added</br>- There are some categories selected for the news partner|1) Examine the <b>Home</b> page</br>2) Go to the category for which news partner is configured</br>3) Go to the category for which news partner is not configured|1) There is news from the news partner configured. News from a partner is shown among the created by admin articles according to the creation date</br>2) There is news from the news partner configured which is related to this category. News from a partner is shown among the created by admin articles according to the creation date</br>3) There is no news from the news partner configured|
</details>
