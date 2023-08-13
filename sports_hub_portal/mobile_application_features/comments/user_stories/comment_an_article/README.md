### Back to [Comments block](../../README.md) feature

# Allow users to comment an article in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to leave a comment on the article page

## Acceptance criteria

<pre>
<b><i>Scenario: A user leaves a comment on the article page</i></b>

Given I am logged in as a user

When I view an article page and comments are enabled by the admin
Then I see a comments section below the article content
  And I see the input where I can enter a comment or reply to existing comments

When I enter text into the comment input and submit
Then I see a comment is immediately posted

When I am not logged in and tap a comment input or try to reply to a comment
Then I see the message "Please log in to leave a comment" with the link to the log-in page

When I am logged in and view comment submitted by me
Then I see the <b>Edit</b>, <b>Delete</b>, and <b>Comment</b> icons

When I tap <b>Delete</b>
Then I see the confirmation pop-up window

When I confirm deletion
Then I see my comment is removed from the comment list

When I tap <b>Edit</b>
Then I see my comment is moved to the submission form

When I change my text and post a comment
Then I see the edited comment is immediately posted in the right place
  And I see my comment has the <b>Edited</b> label

<i>NOTE: Comment section should also work in the same way for video page</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Not logged-in users see comments on the article page
2. Not logged-in users see "Please log in to leave a comment" pop-up window
3. Logged-in users see comments on the article page
4. Logged-in users see confirmation pop-up window to delete comments

<details>
  <summary>Click here to see mockups details</summary>

**1. Not logged-in users see comments on the article page:**

![Not logged-in users see comments on the article page](/sports_hub_portal/mobile_application_features/comments/images/application_comments_for_not_logged_in_user.png)

**2. Not logged-in users see "Please log in to leave a comment" pop-up window:**

![Not logged-in users see "Please log in to leave a comment" pop-up window](/sports_hub_portal/mobile_application_features/comments/images/application_log_in_to_leave_comments_popup.png)

**3. Logged-in users see comments on the article page:**

![Logged-in users see comments on the article page](/sports_hub_portal/mobile_application_features/comments/images/application_comments_for_logged_in_user.png)

**4. Logged-in users see confirmation pop-up window to delete comments:**

![Logged-in users see confirmation pop-up window to delete comments](/sports_hub_portal/mobile_application_features/comments/images/application_before_delete_popup.png)

</details>

## Test cases

1. Verify that logged-in users can comment an article or existing comments
2. Verify that not logged-in users cannot comment an article or existing comments
3. Verify that logged-in users can edit their comments
4. Verify that logged-in users cannot edit or delete other users' comments
5. Verify that logged-in users can delete their comments to an article or comment

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that logged-in users can comment an article or existing comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is some article with comments enabled</br>- There are some users’ comments to the article|1) Select an article</br>2) Enter a comment</br>3) Tap <b>Submit</b></br>4) Reply to a comment from another user</br>5) Tap <b>Submit</b>|1) Comment appears as the latest comment to the article and is visible to users</br>2) Comment appears as the latest comment to another comment and is visible to users|

### **#2. Verify that not logged-in users cannot comment an article or existing comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is not logged in</br>- There is some article with comments enabled</br>- There are some users’ comments to the article|1) Select an article</br>2) Tap comment icon to the article</br>3) View comments to the article</br>4) Tap comments icon to the comment|1) Message "Please log in to leave a comment" with a link to the log-in page appears</br>2) Message "Please log in to leave a comment" with a link to the log-in page appears|

### **#3. Verify that logged-in users can edit their comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is a comment to the article by this user</br>- There is a reply to the existing comment by this user|1) Go to the article with comments</br>2) Go to your comment and then tap tap <b>Edit</b> icon</br>3) Make some changes</br>4) Tap <b>Submit</b></br>5) Go to your reply to the comment, and then tap the <b>Edit</b> icon</br>6) Make some changes</br>7) Tap <b>Submit</b>|4) The edited comment is immediately posted with the <b>Edited</b> label in the right place, and all users can see it</br>7) The edited comment is immediately posted with the <b>Edited</b> label in the right place, and all users can see it|

### **#4. Verify that logged-in users cannot edit or delete other users’ comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some comments of other users to the article</br>- There are some replies from other users to comments|1) Select some article with comments</br>2) View other users' comments to the article</br>3) View other users' replies to comments|2) The <b>Edit</b> and <b>Delete</b> icons are not available</br>3) The <b>Edit</b> and <b>Delete</b> icons are not available|

### **#5. Verify that logged-in users can delete their comments to an article or comment**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is a comment to the article by this user</br>- There is a reply to the comment by this user|1) Select previously commented article</br>2) Tap the <b>Delete</b> icon near the user’s comment to the article</br>3) Tap <b>Delete</b></br>4) Tap the <b>Delete</b> icon near the user’s comment to the article</br>5) Tap <b>Delete</b>|2) Confirmation pop-up window appears</br>3) Comment is removed and not visible anymore</br>4) Confirmation pop-up window appears</br>5) Comment is removed and not visible anymore|
</details>
