### Back to [Manage news partners on the portal](../../) feature

# News from configured partners can not be edited by the admin

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I should not see the news from the configured partners on the articles list page

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is viewing the articles list page</i></b>

Given I am logged in as an admin user

When I view the articles list page
Then I don’t see the news from the configured news partner so I cannot edit, delete or publish/unpublish this news
</pre>

## Mockups

1. Admin user sees articles list

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees articles list:**

![Admin user sees articles list](/products/sports_hub_portal/web_application_features/manage_news_partners/images/admin_side_articles_list.png)

</details>

## Test cases

1. Verify that there is no news from the news partner shown on the articles list page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that there is no news from the news partner shown on the articles list page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the articles list page</br>2) Examine the articles available to be configured|2) There is no news from the news partner present|
</details>
