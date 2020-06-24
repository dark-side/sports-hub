### Back to [Home page of the portal](../../) feature

# Allow admin user to configure Photo of the Day block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to set up Photo of the Day
    So that the site users can see it on the Home page

## Acceptance criteria

    Scenario: An admin user configures Photo of the Day block
    Given I am logged in as an admin user

    When I am on Home configuration page
    Then I see a Photo of the Day block after Breakdown block and show/hide toggle 
      And I see a Photo of the day block contains next fields:
        Add picture - required field with formats .png, .jpg, .tif, .jpeg
        Alt input field - required field
        Photo tile - required field
        Short description - required field
        Author - required field
    When I select a picture and fill out all the fields and click Save
    Then I see a picture and information should be saved as Photo of the Day
    When I click Publish
    Then I see All changes are ready to be displayed for the users on the Home Page

## Mockups

1. The admin user sees Home Page 
2. The admin user sees configured Home Page
3. User sees a photo in edit state

<details>
  <summary>Click here to see mockups details</summary>

**1. The admin user sees Home Page:**

![Home Page](/products/sport_news_portal/web_application_features/home_page/images/home_page_admin_side_empty.png)

**2. The admin user sees configured Home Page:**

![Home Page](/products/sport_news_portal/web_application_features/home_page/images/home_page_admin_side.png)

**3. User sees a photo in edit state:**

![Photo in edit state](/products/sport_news_portal/web_application_features/home_page/images/edit_photo.png)

</details>

## Test Scenarios

1. Verify that admin can configure Photo of the Day block

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can configure Photo of the Day block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Go to home configuration page|
|4|Examine photo of the day block fields|
|5|Select a picture|Photo of the day block contains next fields:<br> - add picture<br> - Alt input field<br> - photo tile<br> - short description<br> - author
|6|Fill in all the fields|
|7|Click Save|The picture and information should be saved as Photo of the Day

</details>

