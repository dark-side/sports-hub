### Back to [Banners on the portal](../../README.md) feature

# Allow users to view configured banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view banners in the right sidebar of the site
    So that I can see reminders about upcoming sports events, important updates, etc.

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views banners in the right sidebar of the site</i></b>

Given I am site user

When I view a page within the category that has published banner
Then I see a banner photo in the right sidebar

When there are more than one banner configured for the category
Then I see banners are rotating every 3 seconds
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a banner in the right sidebar

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a banner in the right sidebar:**

![Users see a banner in the right sidebar](/sports_hub_portal/web_application_features/banners/images/banners_user_side.png)

</details>

## Test cases

1. Verify that users can view the published banners
2. Verify that banners are rotating

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users can view the published banners**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Banners are published for the category|1) Go to the category</br>2) Examine the right sidebar|2) There are banners with a photo on the right sidebar|

### **#2. Verify that banners are rotating**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Banners are published for the category</br>- There are more than one banner in the category|1) Go to the category</br>2) Wait for 3 seconds</br>3) Examine the right sidebar</br>4) Wait till all banners from the category are shown|3) Banner is changed on the right sidebar</br>4) The first banner is shown again|

</details>
