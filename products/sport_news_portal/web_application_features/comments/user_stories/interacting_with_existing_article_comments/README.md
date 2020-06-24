### Back to [Comments block on the portal](../../) feature

# Allow users to interacting with existing article comments on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to sort comments and I want to be able to put like/dislike mark to the comment 

## Acceptance criteria

    Scenario: A site user  sorts comments and wants to be able to put like/dislike mark to the comments block
    Given I am logged in as a site user

    When I view an article page 
    Then I see an indicator for the number of existing comments, a list of existing comments with 10 the most recent comments at the top, and "Show more" at the bottom
      And I see a dropdown selection field with options to sort by most popular, oldest first, or newest first
    When I change the dropdown selection 
    Then I see a comments list is updated based on my selection
    When I click “Show more” button
    Then I see more comments is loaded (20 comments)
    When I am a logged-in user 
      And I view an existing comment
    Then I see a Like and Dislike icons with numbers
    When I click on the icon
    Then I see a corresponding number increases
    When I click on the same icon 
    Then I see a corresponding number decreases
    When I click an opposite icon
    Then I see my vote is moved to the corresponding number
    When I am logged out and click on the Like/Dislike icon
    Then I see a popup with a link to log in page that says “Please Log In to Like/Dislike comment”
    NOTE: Comment section should also work in the same way for videos.


## Mockups

1. Logged in user sees comments on the Article page
2. Before delete user sees warning popup
3. User sees popup with confirmation that comment is deleted
4. User sees comments after clicking “Show more” button

<details>
  <summary>Click here to see mockups details</summary>

**1. Logged in user sees comments on the Article page:**

![Comments on the Article Screen](/products/sport_news_portal/web_application_features/comments/images/comments_for_logged_in_user.png)

**2. Before delete user sees warning popup:**

![Warning popup](/products/sport_news_portal/web_application_features/comments/images/before_delete_warning_popup.png)

**3. User sees popup with confirmation that comment is deleted:**

![Confirmation popup](/products/sport_news_portal/web_application_features/comments/images/comment_deleted_popup.png)

**4. User sees comments after clicking “Show more” button:**

![Expanded comments](/products/sport_news_portal/web_application_features/comments/images/expanded_comments.png)

</details>

## Test Scenarios

1. Verify Article comment block
2. Verify changing dropdown selection field
3. Verify clicking on “Show more” button
4. Verify clicking on the Like and Dislike icon
5. Verify clicking on the Like and Dislike icon if user is not log in

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify Article comment block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe Article comment block|Article comment block consists of:<br> - An indicator for the number of existing comments<br> - A list of existing comments with the 10 most recent comments at the top<br> - “Show more” at the bottom<br> - Dropdown selection field

### **#2. Verify changing dropdown selection field**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Verify dropdown selection field|Dropdown selection field contains options to sort by<br> - Most popular<br> - Oldest first<br> - Newest first
|4|Change dropdown selection field|The comments list is updated based on my selection

### **#3. Verify clicking on “Show more” button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe Article comment block|
|4|Click on “Show more”|All comments are loaded (20 comments)

### **#4. Verify clicking on the Like and Dislike icon**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe Article comment block|
|4|Click on “Show more”|
|5|Observe Like and Dislike icons|The Like and Dislike icons with numbers is present at the right top corner
|6|Click on the icon|The corresponding number is increased
|7|Click on the icon again|The corresponding number is decreased

### **#5. Verify clicking on the Like and Dislike icon if user is not log in**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Do not log in your user account|
|3|Observe Article comment block|
|4|Click on “Show more”|
|5|Observe Like and Dislike icons|The Like and Dislike icons with numbers is present at the right top corner
|6|Click on the icon|Popup with a link to log in page that says “Please Log In to Like/Dislike comment”

</details>
