### Back to [Desktop application](/desktop_application_features/desktop_application_features_list/README.md) functional requirements

# Manage advertisements on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

The admin user should be able to configure the advertisements list: add new advertisements, edit, delete, and disable advertisements for the whole site. Two types of advertisements should be supported:
  - Category related
  - Site-wide

When an admin user publishes a new advertisement, they can optionally choose the advertisement category. If no category is selected, the advertisement is site-wide and will be shown on any page of the site. If a category is selected for an ad, this ad should be displayed only on the site pages related to the selected category.
When there is more than one ad that should be shown in the category, ads will be rotating every 3 seconds.

## Check list:

  - Verify if UI corresponds to the prototype
  - Admin user should be able to edit the advertisements list (including adding new advertisements, editing advertisements, deleting advertisements, and disabling advertisements for the whole site)
  - Category related and site-wide advertisements should be supported
  - Site-wide advertisements should be shown on any page of the site

## Prototype of the feature

Please click to see the clickable prototypes:
  - [Windows/Linux](https://www.figma.com/proto/vmcb5e0R1a220Fb7LdvNrS/Manage-advertisements?page-id=0%3A1073&node-id=6422-284&viewport=-4754%2C1012%2C0.17&t=a7DaUckjk0Pdxyla-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=0%3A2335)
  - [MacOS](https://www.figma.com/proto/vmcb5e0R1a220Fb7LdvNrS/Manage-advertisements?page-id=7603%3A1165&node-id=7603-2249&viewport=-6029%2C991%2C0.48&t=UYZeGGgbh55J24xQ-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=7603%3A1187)

Please click [here](https://www.figma.com/file/vmcb5e0R1a220Fb7LdvNrS/Manage-advertisements?node-id=7603%3A1165) to see mockups that were included in the prototypes and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure advertisements**](/desktop_application_features/manage_ads/user_stories/configure_ads/README.md)|<pre>As an admin user<br>I want to configure the list of advertisements<br>So that it is possible to promote them via the Sports Hub site</pre>
