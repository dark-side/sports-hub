### Back to [Manage Articles of the portal](../../) feature

# Allow admin users to edit existing article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to edit the existing article

## Acceptance criteria

    Scenario: An admin user edits the existing article
    Given I am logged in as an admin user

    When I view Edit Article page
    Then I see the next elements:
      - Path to the article
      - Preview link in a top-right corner of the screen
      - Drag-and-drop field with pre-populated image
      - Three pre-populated dropdowns fields, where I can change Conference, Team, and Location
      - Three pre-populated fields, where I can change details of the article: Alt, Article Headline, Caption
      - WYSIWYG HTML pre-populated editor for content where I can change the style of the text (make a header, paragraph or list, manage font style and text aligning)
      - Switch button for turning on or off comments for the article
      - Block, where I can manage the type and number of articles that will be shown in More Articles block that contains next dropdown fields:
        - The Category – category of articles that will be shown in More Articles block
        - The Conference – articles regarding for specific conference that will be shown in More Articles block
        - The Team – articles regarding specific team that will be shown in More Articles block
        Stored From
        - Amount – amount of the articles in More Articles block
      - Save (disabled until I make any changes) and Cancel buttons in the top of the page
    When I click on Preview link
    Then I see how this article is shown in the new tab
    When I hover on the field with the image
    Then I see the icons for uploading a new image or editing the existing that is described in story “Editing the image of the article”
    When I make any changes in the form
    Then I see a Save button is enabled
    When I click on Save button
    Then I see a confirmation popup that article is added
    When I close it
    Then I see viewing articles page
    When I click on the Cancel button
    Then I see confirmation popup, where I should confirm that I want to leave the form without saving changes
    When I click on Confirm button
    Then I see the page with a list of the articles

## Mockups

1. User sees edit article form
2. User sees cancel edit article popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees edit article form:**

![Add edit article form Screen](/products/sport_news_portal/web_application_features/manage_articles/images/edit_article.png)

**2. User sees cancel edit article popup:**

![Cancel edit article popup](/products/sport_news_portal/web_application_features/manage_articles/images/cancel_edit_article_popup.png)

</details>

## Test Scenarios

1. Verify the content of Edit Article page
2. Verify dropdown fields in More Articles block on Edit Article Page
3. Verify Preview button on Edit Article page
4. Verify choosing file for uploading on Edit Article Page
5. Verify Save button on Edit Article Page
6. Verify clicking on Cancel button on Edit Article Page
7. Verify switch button functionality on Edit Article Page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of Edit Article page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|
|5|Observe content of Edit Article Page|There are such elements:<br>- Drag-and-drop field for image upload<br>- Three dropdowns fields<br>- Three fields, where I can add details of the article: Alt, Article Headline, Caption<br>- WYSIWYG HTML editor for content where I can format text<br>- Switch button for turning on or off comments for the article<br>- Block, where I can manage the type and number of articles that will be shown in More Articles block<br>- Save (disabled until all fields are filled) and Cancel buttons in the top of the page

### **#2. Verify dropdown fields in More Articles block on Edit Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|Admin is redirected to Edit Article page
|5|Check what dropdown fields and buttons contain More Article block|More Articles block that contains next dropdown fields:<br>- The Category<br>- The Conference<br>- The Team<br>- Stored From<br>- Amount

### **#3. Verify Preview button on Edit Article page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|Admin is redirected to Edit Article page
|5|Click on a Preview link button|Admin will see in the new tab how this article will be shown

### **#4. Verify choosing file for uploading on Edit Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|Admin is redirected to Edit Article page
|5|Click on +Add picture|File explorer window where needed image can be selected

### **#5. Verify Save button on Edit Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|Admin is redirected to Edit Article page
|5|Edit article|
|6|Click Save button|New article is edited and shown at the top of the list

### **#6. Verify clicking on Cancel button on Edit Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|Admin is redirected to Edit Article page
|5|Edit article|
|6|Click cancel button|Confirmation popup appears, where admin could confirm leaving the form without saving changes
|7|Click on Confirm button|The page with a list of the articles appears

### **#7. Verify switch button functionality on Edit Article Page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on any Article -> Edit|Admin is redirected to Edit Article page
|5|Change the state of the Switch button|The comments block will be shown or hidden

</details>

