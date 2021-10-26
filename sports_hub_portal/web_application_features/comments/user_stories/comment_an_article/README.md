### Back to [Comments block on the portal](../../) feature

# Allow users to comment an article on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to leave a comment on the article page

## Acceptance criteria

<pre>
<b><i>Scenario: A site user leaves a comment on the article page</i></b>

Given I am logged in as a site user

When I view an article page
Then I see a comments section below the article content
  And I see the text field where I can enter a comment and reply to existing comments

When I enter a comment
Then I see the <b>Cancel</b> and <b>Submit</b> buttons

When I click <b>Cancel</b>
Then my comment text is discarded

When I enter text into the comment text field
  And I click <b>Submit</b>
Then I see a comment is immediately posted on the site and submitted for moderation

When I am not logged in
  And I click comment text field or try to reply to a comment
Then I see the pop-up window "Please log in to leave a comment" with the link to the log-in page

When I am logged in and view comment submitted by me
Then I see the <b>Edit</b>, <b>Delete</b>, and <b>Comment</b> buttons

When I click <b>Delete</b>
Then I see the confirmation pop-up window

When I confirm deletion
Then I see my comment is removed from the comment list

When I click <b>Edit</b>
Then I see my comment is moved to the submission form

When I change my text and post a comment
Then I see the edited comment is immediately posted on the site in the right place and submitted for moderation
  And I see my comment has the <b>Edited</b> label

<i>NOTE: Comment section should also work in the same way for videos.</i>
</pre>

## Mockups

1. Not logged-in users see comments on the article page
2. Logged-in users see comments on the article page
3. Users see comments block with sub-comments
4. Users enter a comment text to the input field
5. Users see "Log in to leave comments" pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Not logged-in users see comments on the article page:**

![Not logged-in users see comments on the article page](/sports_hub_portal/web_application_features/comments/images/comments_for_no_logged_in_user.png)

**2. Logged-in users see comments on the article page:**

![Logged-in users see comments on the article page](/sports_hub_portal/web_application_features/comments/images/comments_for_logged_in_user.png)

**3. Users see comments block with sub-comments:**

![Users see comments block with sub-comments](/sports_hub_portal/web_application_features/comments/images/sub_comments.png)

**4. Users enter a comment text to the input field:**

![Users enter a comment text to the input field](/sports_hub_portal/web_application_features/comments/images/posting_comments_in_progress.png)

**5. Users see "Log in to leave comments" pop-up window:**

![Users see "Log in to leave comments" pop-up window](/sports_hub_portal/web_application_features/comments/images/log_in_to_leave_comments_popup.png)

</details>

## Test cases

1. Verify that logged-in users can comment an article or existing comments
2. Verify that not logged-in users cannot comment an article or existing comments
3. Verify that logged-in users can edit their comments
4. Verify that logged-in users cannot edit or delete other users’ comments
5. Verify that logged-in users can delete their comments to an article
6. Verify that logged-in admin can delete any users’ comments

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that logged-in users can comment an article or existing comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is some article with comments enabled</br>- There are some users’ comments to articles|1) Select an article</br>2) Enter a comment</br>3) Click <b>Submit</b></br>4) Reply to a comment from another user</br>5) Click <b>Submit</b>|1) Comment appears as the latest comment to the article and is visible to users</br>2) Comment appears as the latest comment to another comment and is visible to users|

### **#2. Verify that not logged-in users cannot comment an article or existing comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is not logged in</br>- There is some article with comments enabled</br>- There are some users’ comments to the article|1) Select an article</br>2) Select comment form to the article</br>3) View comments to the article</br>4) Select comment form to reply to a comment|2) Pop-up window "Please log in to leave a comment" with a link to log-in page appears</br>4) Pop-up window "Please log in to leave a comment" with a link to log-in page appears|

### **#3. Verify that logged-in users can edit their comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is a comment to the article by this user</br>- There is a reply to the existing comment by this user|1) On the <b>Home</b> page, select an article with comments</br>2) Go to your reply to a comment, and then click <b>Edit</b></br>3) Make some changes</br>4) Click <b>Submit</b>|4) The edited comment is immediately posted with the <b>Edited</b> label in the right place, and all users can see it|

### **#4. Verify that logged-in users cannot edit or delete other users’ comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some comments of other users to the article</br>- There are some replies from other users to comments|1) Select some article with comments</br>2) View other users’ comments to the article</br>3) View other users’ replies to comments|2) The <b>Edit</b> and <b>Delete</b> buttons are not available</br>3) The <b>Edit</b> and <b>Delete</b> buttons are not available|

### **#5. Verify that logged-in users can delete their comments to an article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is a comment to the article by this user</br>- There is a reply to the comment by this user|1) Select previously commented article on the <b>Home</b> page</br>2) Click the <b>Delete</b> button near the user’s comment to the article</br>3) Click <b>Delete</b></br>4) Click the <b>Delete</b> button near the user’s comment to the article</br>5) Click <b>Delete</b>|2) Confirmation pop-up window appears</br>3) Comment is removed and not visible anymore</br>4) Confirmation pop-up window appears</br>5) Comment is removed and not visible anymore|

### **#6. Verify that logged-in admin can delete any users’ comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- There are some comments to an article</br>- There are some replies to comments|1) On the <b>Home</b> page, select previously commented article</br>2) Select a comment, and then click <b>Delete</b>|1) Confirmation pop-up window appears</br>2) Comment is removed and not visible anymore</br>|
</details>
