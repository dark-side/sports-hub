### Back to [News from Sports Hub partners](../../README.md) feature

# Allow users to view news from configured partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to see news from the configured partners in the appropriate categories

## Acceptance criteria

<pre>
<b><i>Scenario: A user is browsing different category pages and the Home page</i></b>

Given I am a user

When I view the Home page
Then I see the news from the configured news partner
  And this news is shown among the articles created by admin according to the creation date

When I view any category page
Then I see the news from the configured news partner
  And this news is shown among the articles created by admin according to the creation date
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Full articles list page

<details>
  <summary>Click here to see mockups details</summary>

**1. Full articles list page:**

![Full articles list page](/sports_hub_portal/mobile_application_features/news_partners/images/league_articles_page.png)

</details>

## Test cases

1. Verify that news from the news partner is shown according to the creation date

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that news from the news partner is shown according to the creation date**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There is some partner added</br>- There are some categories selected for the news partner|1) Examine the Home page</br>2) Go to the category news partner is configured for</br>3) Go to the category news partner is not configured for|1) There is news from the news partner configured. News from the partner is shown among the articles created by admin according to the creation date</br>2) There is news from the news partner configured which is related to this category. News from the partner is shown among the articles created by admin according to the creation date</br>3) There is no news from the news partner configured|
</details>
