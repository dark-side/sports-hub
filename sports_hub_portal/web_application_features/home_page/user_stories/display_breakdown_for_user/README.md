### Back to [Home page of the portal](../../README.md) feature

# Display the Breakdown section for site users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see the Breakdown section on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the Breakdown section on the Home page</i></b>

Given I am a site user

When I am on the <b>Home</b> page
Then I see the <b>Breakdown</b> section after the <b>Main articles</b>
  And I see the section contains the heading <b>Breakdown</b>
  And I see 4 newest articles for the category are formed into a group
  And I see each article contains:
    - Photo
    - Headline
    - Caption - for the 3 secondary articles

When the <b>Subcategory</b> is selected by admin
Then I see only news from this subcategory

When the <b>Team</b> is selected by admin
Then I see only news from this team

When the <b>Breakdown</b> section is hidden by admin
Then I do not see the <b>Breakdown</b> section

When the <b>Breakdown</b> section is shown by admin
Then I see the <b>Breakdown</b> section

When some breakdown is deleted from the <b>Breakdown</b> section
Then I do not see it anymore in the <b>Breakdown</b> section

When I select any article photos, headlines, or captions in the <b>Breakdown</b> section
Then I am taken to the article view page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Home</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Home page:**

![Users see the Home page](/sports_hub_portal/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test cases

1. Verify that 4 newest articles from the <b>Category</b> for the configured breakdown are visible to users
2. Verify that 4 newest articles from the <b>Subcategory</b> for the configured breakdown are visible to users
3. Verify that 4 newest articles from the <b>Team</b> for the configured breakdown are visible to users
4. Verify that the user is redirected to the right page by selecting the article photo, headline, or caption in the <b>Breakdown</b> section
5. Verify that the deleted breakdown is not shown
6. Verify that the hidden <b>Breakdown</b> section is not shown
7. Verify that the unhidden <b>Breakdown</b> section is shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that 4 newest articles from the Category for the configured breakdown are visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section</br>- There is breakdown configured for <b>Category</b> (<b>Subcategory</b> and <b>Team</b> are not selected)|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected category|

### **#2. Verify that 4 newest articles from the Subcategory for the configured breakdown are visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section</br>- There is a breakdown configured for the subcategory (<b>Team</b> is not selected)|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected subcategory|

### **#3. Verify that 4 newest articles from the Team for the configured breakdown are visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section</br>- There is a breakdown configured for a team|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected team|

### **#4. Verify that the user is redirected to the right page by selecting the article photo, headline, or caption in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section|1) Select any article photo</br>2) Select any headline</br>3) Select any caption|1) The user is redirected to the article page</br>2) The user is redirected to the article page</br>3) The user is redirected to the article page|

### **#5. Verify that the deleted breakdown is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin removed some breakdown</br>- Go to the <b>Home</b> page > <b>Breakdown</b> section|1) On the <b>Home</b> page, examine the <b>Breakdown</b> section|1) The removed breakdown is not present|

### **#6. Verify that the hidden Breakdown section is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides <b>Breakdown</b> section</br>- Go to the Sports Hub home page|1) On the <b>Home</b> page, examine the <b>Breakdown</b> section|1) The <b>Breakdown</b> section is not present|

### **#7. Verify that the unhidden Breakdown section is shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin shows <b>Breakdown</b> section</br>- Go to the Sports Hub home page|1) On the <b>Home</b> page, examine the <b>Breakdown</b> section|1) The <b>Breakdown</b> section is present|

</details>
