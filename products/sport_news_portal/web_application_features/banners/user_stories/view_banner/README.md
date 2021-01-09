### Back to [Banners on the portal](../../) feature

# Allow users to view configured banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view banners in the right sidebar of the site
    So that I can see reminders about upcoming sport events, important updates, etc

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views banners in the right sidebar of the site</i></b>

Given I am site user

When I view a page within the category that has published banner
Then I see a banner photo in the right sidebar

When there are more than one banner configured for the category
Then I see banners are rotating every 3 seconds
</pre>

## Mockups

1. User sees a banner in the right sidebar

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a banner in the right sidebar:**

![User sees a banner in the right sidebar](/products/sport_news_portal/web_application_features/banners/images/banners_user_side.png)

</details>

## Test cases

1. Verify that a user can view the published banners
2. Verify that banners are rotating

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that a user can view the published banners**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Banners are published for a category|1) Go to a category</br>2) Examine the right sidebar|2) There are banners with a photo on the right sidebar|

### **#2. Verify that banners are rotating**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Banners are published for a category</br>- There are more than one banner in the category|1) Go to a category</br>2) Wait 3 seconds</br>3) Examine the right sidebar</br>4) Wait till all banners from the category are shown|3) Banner is changed on the right sidebar</br>4) The first banner is shown again|

</details>
