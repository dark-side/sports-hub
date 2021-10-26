### Back to [Comments block on the portal](../../) feature

# Allow users to interact with existing article comments on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to sort comments and like or dislike the comment

## Acceptance criteria

<pre>
<b><i>Scenario: A site user sorts comments and likes or dislikes comments</i></b>

Given I am logged in as a site user

When I view an article page
Then I see the number of existing comments, a list of existing comments with 10 most recent comments at the top, and the <b>Show more</b> comments button at the bottom
  And I see a drop-down list with options to sort by most popular, oldest first, or newest first

When I select an option from the drop-down list
Then I see a comments list is updated based on my selection

When I click <b>Show more</b> comments
Then I see more comments are loaded (up to 20)

When all comments are loaded
Then <b>Show more</b> changes to <b>Show less</b>

When I view an existing comment
Then I see <b>Like</b> and <b>Dislike</b> with numbers

When I click <b>Like</b> or <b>Dislike</b>
Then I see a corresponding number increases

When I click <b>Like</b> or <b>Dislike</b>
Then I see a corresponding number decreases

When I am logged out and click <b>Like</b> or <b>Dislike</b>
Then I see the pop-up window "Please log in to like or dislike comments" with the link to log-in page

<i>NOTE: Comments section should also work in the same way for videos.</i>
</pre>

## Mockups

1. Logged-in users see comments on the article page
2. Users see confirmation pop-up window to delete comments
3. Users see success delete message
4. Users see last comments after clicking the <b>Show more</b> button

<details>
  <summary>Click here to see mockups details</summary>

**1. Logged-in users see comments on the article page:**

![Logged-in users see comments on the article page](/sports_hub_portal/web_application_features/comments/images/comments_for_logged_in_user.png)

**2. Users see confirmation pop-up window to delete comments:**

![Users see confirmation pop-up window to delete comments](/sports_hub_portal/web_application_features/comments/images/before_delete_warning_popup.png)

**3. Users see success delete message:**

![Users see success delete message](/sports_hub_portal/web_application_features/comments/images/comment_deleted_popup.png)

**4. Users see last comments after clicking the Show more button:**

![Users see last comments after clicking the Show more button](/sports_hub_portal/web_application_features/comments/images/expanded_comments.png)

</details>

## Test cases

1. Verify that the <b>Show more</b> button is present if there are more than 10 comments available above the article
2. Verify that the <b>Show less</b> button is present if there are more than 10 comments shown
3. Verify that there are no <b>Show less</b> and <b>Show more</b> buttons available if there are less than 10 comments
4. Verify that logged-in users can like or dislike comments
5. Verify that not logged-in users cannot like or dislike comments
6. Verify that it is possible to change the sorting order of comments

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Show more button is present if there are more than 10 comments available above the article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are more than 20 comments to the article|1) Select any article on the <b>Home</b> page</br>2) Go to the comments section, and then click <b>Show more</b>|1) 10 comments are shown</br>2) 10 more comments are loaded (20 comments in total) and a user can still see the <b>Show more</b> button because there are more comments to show. The <b>Show less</b> button appears|

### **#2. Verify that the Show less button is present if there are more than 10 comments shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are more than 10 comments to the article|1) Select any article on the <b>Home</b> page</br>2) Click <b>Show more</b></br>3) Click <b>Show less</b>|1) 10 comments are shown</br>2) All comments are loaded, the <b>Show more</b> button disappears, and the <b>Show less</b> button appears</br>3) Only 10 comments are show, the <b>Show less</b> button disappears, and the <b>Show more</b> button appears|

### **#3. Verify that there are no Show less and Show more buttons available if there are less than 10 comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are less than 10 comments to the article|1) Select any article on the <b>Home</b> page</br>2) Check if the <b>Show more</b> and <b>Show less</b> buttons are shown|1) All comments are shown</br>2) There are no <b>Show more</b> or <b>Show less</b> buttons in the comments section|

### **#4. Verify that logged-in users can like or dislike comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some comments to the article</br>- There are some replies to comments|1) Select any article on the <b>Home</b> page</br>2) Click <b>Like</b> under any comment</br>3) Click <b>Like</b> under any reply to the comment</br>4) Сlick <b>Dislike</b> under the comment above the article</br>5) Сlick <b>Dislike</b> under the comment above the comment</br>6) Click <b>Like</b> under the comment you previously disliked</br>7) Click <b>Dislike</b> under the comment you previously liked|2) The number of likes increases</br>3) The number of likes increases</br>4) The number of dislikes increases</br>5) The number of dislikes increases</br>6) The number of likes increases and the number of dislikes decreases</br>7) The number of dislikes increases and the number of likes decreases|

### **#5. Verify that not logged-in users cannot like or dislike comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is not logged in</br>- There are some comments to the article</br>- There are some replies to comments|1) Select any article on the <b>Home</b> page</br>2) Click the <b>Like</b> or <b>Dislike</b> icon under any comment above the article|2) Pop-up window "Please log in to leave a comment" with a link to log-in page appears|

### **#6. Verify that it is possible to change the sorting order of comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is not logged in</br>- There are some comments to the article|1) Select any article on the <b>Home</b> page with comments</br>2) Click <b>Sort by > Most popular</b></br>3) Click <b>Sort by > Oldest first</b></br>4) Click <b>Sort by > Newest first</b>|2) Most popular comments are shown first</br>3) Oldest comments are shown first</br>4) Newest comments are shown first|
</details>
