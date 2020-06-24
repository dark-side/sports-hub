# Manage teams on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the Feature](#prototype-of-the-feature)
- [User Stories](#user-stories)

## Description

All of the sports fans have their favorite team or teams. The goal of this feature is to allow the registered site users to customize Team Hub where they will see news related only to their favorite team(s). In case the user did not select any of the teams, then they will see news about the teams from their geolocation.

User with admin permission should be able to manage teams, namely:
  - add a new team
  - view existing teams
  - edit the existing team
  - remove the existing team

## Check list:

  - Admin should be able to add new team
  - Admin should be able to view existing teams
  - Admin should be able to edit existing team
  - Admin should be able to remove existing team
  - Registered user should be able to customize the news
  - Registered user should be able to select favourites teams
  - Registered user should be able to read news of the favorite teams
  - Registered user should be able to unfollow a team
  - Geolocation should work and select related teams if the list of favourite teams are empty
  - All popups and buttons should not be corrupted
  - All the buttons and dropdown lists should be in a standard format and size
  - Web page content should be correct without any spelling or grammatical errors
  - All fonts should be the same as per the requirements
  - All the text should be properly aligned

## Prototype of the feature

  Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/Sport-News?node-id=0%3A8215) [here](https://www.figma.com/proto/HB6RaAViOl1Iw5qCsEb2gj/Manage-the-teams?node-id=0%3A1&scaling=min-zoom) and to see a clickable prototype for the feature.

## User Stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin users to view Teams page**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/view_teams_page)|<pre>As an admin user<br>I want to be able to view Teams page<br>So that I can see a map with the location of the existing teams and a list of the teams</pre>
2 |[**Allow admin users to add a new Team/Player**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/add_new_team_player)|<pre>As an admin user<br>I want to be able to add a new Team/Player</pre>
3 |[**Allow admin users to edit the existing Team/Player**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/edit_existing_team_player)|<pre>As an admin user<br>I want to be able to edit the existing Team/Player<br>So that I can change the logo or the name of the existing team</pre>
4 |[**Allow admin users to delete the existing Team/Player**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/delete_team_player)|<pre>As an admin user<br>I want to be able to delete the existing Team/Player</pre>
4 |[**Allow users to see Team Hub management page in the personal cabinet**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/team_hub_management_page)|<pre>As a site user<br>I want to be able to have a Team Hub management page<br>So that I can customize the news</pre>
4 |[**Allow users to manage favorite teams in the personal cabinet**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/team_hub_manage_favorite_teams)|<pre>As a site user<br>I want to be able to select my favorite teams</pre>
4 |[**Allow users to see Team Hub page**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/team_hub_page)|<pre>As a site user<br>I want to be able to go to Team Hub page<br>So that I can read news of my favorite teams</pre>
4 |[**Allow users to see teams news on Team Hub based on user’s geolocation**](/products/sport_news_portal/web_application_features/manage_the_teams/user_stories/team_hub_list_teams_by_geolocation)|<pre>As a site user<br>I want to be able to read news of teams from my geolocation on Team Hub page</pre>