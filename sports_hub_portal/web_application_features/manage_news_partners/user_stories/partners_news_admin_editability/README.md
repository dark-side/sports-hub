### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to see articles from configured partners on the articles list page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to see articles from the news partners on the articles list page after they are processed

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is viewing the articles list page</i></b>

Given I am logged in as an admin user

When I view the articles list page
Then I see the news from the configured news partner in <b>Published</b> status after the background job processed them
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees articles list

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees articles list:**

![Admin user sees articles list](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_side_articles_list.png)

</details>

## Test cases

1. Verify that the articles from the news partner shown on the articles list page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the articles from the news partner shown on the articles list page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Have some articles from the news partner processed by the background job </br>2) Go to the articles list page</br>3) Examine the articles list|3) The article from the news partner present in <b>Published</b> status|
</details>
