### Back to [Manage news partners on the portal](../../) feature

# Allow admin user to filter a list of news from partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to filter a list of news from partners

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is viewing the partners articles list page</i></b>

Given I am logged in as an admin user

When I view the <b>News Partners</b> page and click <b>News</b> tab
Then I see a list of articles from the partners
  And I see filters above the articles list to:
    - filter by the category
    - filter by the subcategory
    - filter by the team
    - filter by the partner
    - filter by the status (Draft, Ready for processing, Processing, Processed, Published)
    - filter by the date (Oldest, Latest)

When I select needed filter
Then I see the list of articles is updated
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees filters above the articles list

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees filters above the articles list:**

![Admin user sees filters above the articles list](/sports_hub_portal/desktop_application_features/manage_news_partners/images/admin_side_partner_articles_list.png)

</details>

## Test cases

1. Verify that the filters work as expected on the <b>News</b> tab of the <b>News Partners</b>

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the filters work as expected on the News tab of the News Partners**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Examine the articles list</br>4) Select any filter|3) The filters are shown above the articles list</br>4) The arcticles list is updated|
</details>
