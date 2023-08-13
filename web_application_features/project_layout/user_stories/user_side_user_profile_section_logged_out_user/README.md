### Back to [Page layout on the portal](../../README.md) feature

# Page structure (user side): user profile section in the header (user logged out)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see Sign up and Log in buttons when I am logged out

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views profile section when their are logged-out</i></b>

Given I am a site user

When I view any page on the site
Then I see the user profile in the Header section
  And that section contains <b>Sign up</b> and <b>Log in</b> buttons
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Sign up</b> and <b>Log in</b> buttons when they are not signed in

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Sign up and Log in buttons when they are not signed in:**

![Users see Sign up and Log in buttons when they are not signed in](/web_application_features/project_layout/images/home_page_logged_out_user.png)

</details>

## Test cases

1. Verify that users see Sign up and Log in buttons when they are not signed in

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users see Sign up and Log in buttons when they are not signed in**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to the Sports Hub home page|1) User is not logged-in</br>|1) See <b>Sign up</b> and <b>Log in</b> buttons in the header|

</details>
