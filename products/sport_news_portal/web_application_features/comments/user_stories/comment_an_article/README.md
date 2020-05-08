### Back to [Comments block on the portal](/../../) feature

# Allow users to comment an article on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to leave the comment regarding article content on the article page

## Acceptance criteria

    Scenario: A site user leaves the comment regarding article content on the article page
    Given I am logged in as a site user

    When I view an article page 
    Then I see a comment block below the article content 
      And I see a form where I can enter a comment about the article or existing comments
    When I enter a comment text to the input
    Then I see Cancel and Submit buttons appear
    When I click Cancel
    Then my comment text discarded
    When I enter a comment text to the input
    When I click Submit button
    Then I see a comment is immediately posted to the site and submitted for moderation
    When I am not logged in
      And I click on comment field or try to comment an existing comment 
    Then I see a popup with a link to log in page that says “Please Log In to Leave a comment”
    When I am logged in and view comment submitted by me
    Then I see a Edit and Delete and Comment buttons 
    When I press the Delete button
    Then I see a confirmation popup
    When I confirm the deletion
    Then I see my comment is removed from the comment list
    When I press the Edit button
    Then I see my comment is moved to the submission form
    When I change the message and post a comment
    Then I see the edited comment is immediately posted to the site in the previous place and submitted for moderation
      And I see my comment has the “Edited” label
    NOTE: Comment section should also work in the same way for videos.

## Mockups

1. Not logged in user sees comments on the Article page 
2. Logged in user sees comments on the Article page
3. User sees comments block with sub-comment
4. User enter a comment text to the input field
5. User sees “Log In to leave comments” popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Not logged in user sees comments on the Article page:**

![Comments on the Article Screen](/products/sport_news_portal/web_application_features/comments/images/comments_for_no_logged_in_user.png)

**2. Logged in user sees comments on the Article page:**

![Comments on the Article Screen](/products/sport_news_portal/web_application_features/comments/images/comments_for_logged_in_user.png)

**3. User sees comments block with sub-comment:**

![Sub-comments on the Article Screen](/products/sport_news_portal/web_application_features/comments/images/sub_comments.png)

**4. User enter a comment text to the input field:**

![Posting in progress](/products/sport_news_portal/web_application_features/comments/images/posting_comments_in_progress.png)

**5. User sees “Log In to leave comments” popup:**

![“Log In to leave comments” popup](/products/sport_news_portal/web_application_features/comments/images/log_in_to_leave_comments_popup.png)

</details>

## Test Scenarios

1. Verify that comment about the article is submitted
2. Verify comment Edit button
3. Verify comment Delete button
4. Verify ‘Edited’ label on the comment

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that comment about the article is submitted**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to user account|
|3|View any article|
|4|Observe comment block below article content|
|5|Enter comment about the article in a form|
|6|Click on submit button|The comment is posted immediately to the site and submitted for admin

### **#2. Verify comment Edit button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|View any article|
|4|Observe comment block below article content|
|5|Enter comment about the article in a form|
|6|Click on submit button|The comment is posted immediately to the site and submitted for admin
|7|Observe Edit button|The Edit buttons is placed at the right bottom corner of the comment
|8|Click on Edit button|Comment is moved to the submission form with ability to change the message and post a comment

### **#3. Verify comment Delete button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|View any article|
|4|Observe comment block below article content|
|5|Enter comment about the article in a form|
|6|Click on Submit button|The comment is posted immediately to the site and submitted for admin
|7|Observe Delete button|The Delete buttons is placed at the right bottom corner of the comment
|8|Click on Delete button|Confirmation popup "Are you really want to delete this comment?"
|9|Confirm deleting|The comment is deleted 

### **#4. Verify ‘Edited’ label on the comment**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|View any article|
|4|Observe comment block below article content|
|5|Enter comment about the article in a form|
|6|Click on Submit button|The comment is posted immediately to the site and submitted for admin
|7|Observe Edit button|The Edit buttons is placed at the right bottom corner of the comment
|8|Click on Edit button|Comment is moved to the submission form with ability to change the message and post a comment
|9|Observe ‘Edited’ label on the comment that was edited|Changed comment has the "Edited" label

</details>

