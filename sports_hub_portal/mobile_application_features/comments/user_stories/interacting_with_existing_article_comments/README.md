### Back to [Comments block](../../) feature

# Allow users to interact with existing article comments in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to sort comments and like or dislike the comment

## Acceptance criteria

<pre>
<b><i>Scenario: A user sorts comments and likes or dislikes comments</i></b>

Given I am logged in as a user

When I view an article page
Then I see the number of existing comments, a list of existing comments with 2 most recent comments at the top, and the <b>Show more</b> button at the bottom
  And I see a drop-down list with options to sort by most popular, oldest first, or newest first

When I select an option from the drop-down list
Then I see a comments list is updated based on my selection

When I tap <b>Show more</b>
Then I see more comments are loaded (up to 5)

When more comments are loaded
Then <b>Show less</b> button appears

When I view an existing comment
Then I see <b>Like</b> and <b>Dislike</b> with numbers

When I tap <b>Like</b> or <b>Dislike</b>
Then I see a corresponding number increases

When I tap <b>Like</b> or <b>Dislike</b> for already liked or disliked comment
Then I see a corresponding number decreases

When I am logged out and tap <b>Like</b> or <b>Dislike</b>
Then I see the message "Please log in to like or dislike comments" with the link to the log-in page

<i>NOTE: Comments section should also work in the same way for videos.</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Not logged-in users see comments on the article page
2. Logged-in users see comments on the article page
3. Not logged-in users see "Please log in to like or dislike comments" pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Not logged-in users see comments on the article page:**

![Not logged-in users see comments on the article page](/sports_hub_portal/mobile_application_features/comments/images/application_comments_for_not_logged_in_user.png)

**2. Logged-in users see comments on the article page:**

![Logged-in users see comments on the article page](/sports_hub_portal/mobile_application_features/comments/images/application_comments_for_logged_in_user.png)

**3. Not logged-in users see "Please log in to like or dislike comments" pop-up window:**

![Not logged-in users see "Please log in to like or dislike comments" pop-up window](/sports_hub_portal/mobile_application_features/comments/images/application_log_in_to_like_dislike_popup.png)

</details>

## Test cases

1. Verify that the <b>Show more</b> button is present if there are more than 2 comments available above the article
2. Verify that the <b>Show less</b> button is present if there are more than 2 comments shown
3. Verify that there are no <b>Show less</b> and <b>Show more</b> buttons available if there are less than 3 comments
4. Verify that logged-in users can like or dislike comments
5. Verify that not logged-in users cannot like or dislike comments
6. Verify that it is possible to change the sorting order of comments

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Show more button is present if there are more than 2 comments available above the article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are more than 20 comments to the article|1) Select article with comments</br>2) Go to the comments section, and then tap <b>Show more</b>|1) 2 comments are shown</br>2) 5 more comments are loaded (20 comments in total) and a user can still see the <b>Show more</b> button because there are more comments to show. The <b>Show less</b> button appears|

### **#2. Verify that the Show less button is present if there are more than 2 comments shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are 5 comments to the article|1) Select any article on the <b>Home</b> page</br>2) Tap <b>Show more</b></br>3) Tap <b>Show less</b>|1) 2 comments are shown</br>2) All comments are loaded, the <b>Show more</b> button disappears, and the <b>Show less</b> button appears</br>3) Only 2 comments are show, the <b>Show less</b> button disappears, and the <b>Show more</b> button appears|

### **#3. Verify that there are no Show less and Show more buttons available if there are less than 3 comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are less than 3 comments to the article|1) Select the article</br>2) Check if the <b>Show more</b> and <b>Show less</b> buttons are shown|1) All comments are shown</br>2) There are no <b>Show more</b> or <b>Show less</b> buttons in the comments section|

### **#4. Verify that logged-in users can like or dislike comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some comments to the article</br>- There are some replies to comments|1) Select the article</br>2) Tap <b>Like</b> under any comment</br>3) Tap <b>Like</b> under any reply to the comment</br>4) Tap <b>Dislike</b> under the comment above the article</br>5) Tap <b>Dislike</b> under the comment above the comment</br>6) Tap <b>Like</b> under the comment you previously disliked</br>7) Tap <b>Dislike</b> under the comment you previously liked|2) The number of likes increases</br>3) The number of likes increases</br>4) The number of dislikes increases</br>5) The number of dislikes increases</br>6) The number of likes increases and the number of dislikes decreases</br>7) The number of dislikes increases and the number of likes decreases|

### **#5. Verify that not logged-in users cannot like or dislike comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is not logged in</br>- There are some comments to the article</br>- There are some replies to comments|1) Select the article</br>2) Tap the <b>Like</b> or <b>Dislike</b> icon under any comment above the article|2) Message "Please log in to leave a comment" with a link to the log-in page appears|

### **#6. Verify that it is possible to change the sorting order of comments**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is not logged in</br>- There are some comments to the article|1) Select the article with comments</br>2) Tap <b>Sort by > Most popular</b></br>3) Tap <b>Sort by > Oldest first</b></br>4) Tap <b>Sort by > Newest first</b>|2) The most popular comments are shown first</br>3) The oldest comments are shown first</br>4) The newest comments are shown first|
</details>
