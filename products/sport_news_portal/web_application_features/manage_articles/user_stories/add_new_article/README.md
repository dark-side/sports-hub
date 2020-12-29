### Back to [Manage Articles of the portal](../../) feature

# Allow admin users to add a new article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to add a new article

## Acceptance criteria

    Scenario: An admin user creates a new article
    Given I am logged in as an admin user

    When I view New Article page
    Then I see the next elements:
      - Preview link in a top-right corner of the screen
      - Drag-and-drop field for image upload
      - Three dropdowns fields, where I can select Conference, Team, and Location
      - Three fields, where I can add details of the article: Alt, Article Headline, Caption
      - WYSIWYG HTML editor for content where I can format text (create a header, paragraph or list, manage font style and text aligning)
      - Switch button for turning on or off comments for the article
      - Block, where I can manage the type and number of articles that will be shown in More Articles block that contains next dropdown fields:
        - The Category – category of articles that will be shown in More Articles block
        - The Conference – articles regarding for specific conference that will be shown in More Articles block
        - The Team – articles regarding specific team that will be shown in More Articles block
        Stored From
        - Amount – amount of the articles in More Articles block
      - Save (disabled until all fields are filled) and Cancel buttons in the top of the page
    When I click on Preview link
    Then I see how this article is shown in the new tab
    When I click on +Add picture inside the form for image upload
    Then I see the file explorer window where I can select the needed image
    When I complete the form
    Then I see Save button is enabled
    When I click on Save button
    Then I see viewing articles page
      And I see that my article is added at the top of the list
    When I click on the Cancel button
    Then I see confirmation popup, where I should confirm that I want to leave the form without saving changes
    When I click on Confirm button I see the page with a list of the articles
      And I change the state of the Switch button
    Then the comments block is shown or hidden

## Mockups

1. User sees add new article form
2. User sees add new article filled in form
3. User sees article is saved popup
4. User sees cancel article creation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees add new article form:**

![Add new article form Screen](/products/sport_news_portal/web_application_features/manage_articles/images/add_new_article_form.png)

**2. User sees add new article filled in form:**

![Add new article filled in form Screen](/products/sport_news_portal/web_application_features/manage_articles/images/add_new_article_filled_in_form.png)

**3. User sees article is saved popup:**

![Article is saved popup](/products/sport_news_portal/web_application_features/manage_articles/images/article_saved_popup.png)

**4. User sees cancel article creation popup:**

![Cancel article creation popup](/products/sport_news_portal/web_application_features/manage_articles/images/cancel_article_create_popup.png)

</details>

## Test Scenarios

1. Verify click on the +New Article button
2. Verify dropdown fields in More Articles block
3. Verify Preview button on Create Article page
4. Verify Save button on Create Article Page
5. Verify clicking on Cancel button on Create Article Page
6. Verify switch button functionality on Create Article Page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify click on the +New Article button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page
|5|Observe the elements on Create Article page|The next elements are present:<br>- Preview link in a top-right corner of the screen<br>- Drag-and-drop field for image upload<br>- Three dropdowns fields<br>- Three fields, where I can add details of the article: Alt, Article Headline, Caption<br>- WYSIWYG HTML editor for content where I can format text<br>- Switch button for turning on or off comments for the article<br>- Block, where I can manage the type and number of articles that will be shown in More Articles block<br>- Save (disabled until all fields are filled) and Cancel buttons in the top of the page

### **#2. Verify dropdown fields in More Articles block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page
|5|Observe the elements on Create Article page|
|6|Check what dropdown fields and buttons contain More Article block|More Articles block that contains next dropdown fields:<br>- The Category<br>- The Conference<br>- The Team<br>- Stored From<br>- Amount

### **#3. Verify Preview button on Create Article page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page
|5|Complete the needed fields for new Article on the Create Article page|
|6|Click on a Preview link button|Admin will see in the new tab how this article will be shown

### **#4. Verify Save button on Create Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page
|5|Complete the needed fields for new Article on the Create Article page|
|6|Click Save button|New article is added at the top of the list

### **#5. Verify clicking on Cancel button on Create Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page
|5|Complete the needed fields for new Article on the Create Article page|
|6|Click cancel button|Confirmation popup appears, where admin could confirm leaving the form without saving changes
|7|Click on Confirm button|The page with a list of the articles appears

### **#6. Verify switch button functionality on Create Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page
|5|Change the state of the Switch button|The comments block will be shown or hidden

</details>

