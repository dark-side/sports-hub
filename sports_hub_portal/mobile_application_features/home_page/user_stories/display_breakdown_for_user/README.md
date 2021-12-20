### Back to [Home page in the application](../../) feature

# Display the Breakdown section for users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to see the Breakdown section on the page

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the Breakdown section on the Home page</i></b>

Given I am an user

When I am on the <b>Home</b> page
Then I see a <b>Breakdown</b> section after the <b>Main articles</b> section
  And I see the section contains the heading <b>Breakdown</b>
  And I see 4 newest articles for the category are formed into a group
  And I see each article contains:
    - Photo
    - Headline
    - Caption - for 3 secondary articles

When the <b>Subcategory</b> is selected by admin
Then I see only news from this subcategory

When the <b>Team</b> is selected by admin
Then I see only news from this team

When the <b>Breakdown</b> section is hidden by admin
Then I don't see the <b>Breakdown</b> section

When the <b>Breakdown</b> section is unhidden by admin
Then I see the <b>Breakdown</b> section

When some breakdown is deleted from the <b>Breakdown</b> section
Then I don't see it anymore in the <b>Breakdown</b> section

When I select any of the article photos, headlines, or captions in the <b>Breakdown</b> section
Then I am taken to the right article page
</pre>

## Mockups

1. Users see <b>Home</b> in the navigation menu
2. Full <b>Home</b> page
3. Users see <b>Breakdown</b> section

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Home in the navigation menu:**

![Users see Home in the navigation menu](/sports_hub_portal/mobile_application_features/home_page/images/application_navigation_menu.png)

**2. Full Home page:**

![Full Home page](/sports_hub_portal/mobile_application_features/home_page/images/home_page.png)

**3. Users see Breakdown section**

![Users see Breakdown section](/sports_hub_portal/mobile_application_features/home_page/images/application_breakdown_section.png)

</details>

## Test cases

1. Verify that 4 newest articles from category for the configured breakdown are visible to users
2. Verify that 4 newest articles from subcategory for the configured breakdown are visible to users
3. Verify that 4 newest articles from team for the configured breakdown are visible to users
4. Verify that the user is redirected to the right page by selecting the article photo, headline, or caption in the <b>Breakdown</b> section
5. Verify that the deleted breakdown is not shown
6. Verify that the hidden <b>Breakdown</b> section is not shown
7. Verify that the unhidden <b>Breakdown</b> section is shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that 4 newest articles from category for the configured breakdown are visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section</br>- There is a breakdown for category configured by admin (Subcategory and Team are not selected) |1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected category|

### **#2. Verify that 4 newest articles from subcategory for the configured breakdown are visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section</br>- There is breakdown for subcategory configured by admin (Team is not selected)|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected subcategory|

### **#3. Verify that 4 newest articles from team for the configured breakdown are visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section</br>- There is breakdown configured for team|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected team|

### **#4. Verify that the user is redirected to the right page by selecting the article photo, headline, or caption in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page > <b>Breakdown</b> section|1) Select any article photo</br>2) Select any headline</br>3) Select any caption|1) The user is redirected to the <b>Article</b> page</br>2) The user is redirected to the <b>Article</b> page</br>3) The user is redirected to the <b>Article</b> page|

### **#5. Verify that the deleted breakdown is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin removed some breakdown</br>- Go to the <b>Home</b> page > <b>Breakdown</b> section|1) On the <b>Home</b> page, examine the <b>Breakdown</b> section|1) The removed breakdown is not present|

### **#6. Verify that the hidden Breakdown section is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides the <b>Breakdown</b> section</br>- Go to the <b>Home</b> page > <b>Breakdown</b> section|1) On the <b>Home</b> page, examine the <b>Breakdown</b> section|1) The <b>Breakdown</b> section is not present|

### **#7. Verify that the unhidden Breakdown section is shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin unhides the <b>Breakdown</b> section</br>- Go to the <b>Home</b> page > <b>Breakdown</b> section|1) On the <b>Home</b> page, examine the <b>Breakdown</b> section|1) The <b>Breakdown</b> section is present|
</details>
