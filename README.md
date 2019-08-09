# Geo Location API 

This is an API to determine whether an incoming geographical location is inside at least one of the given areas in GeoJSON format

## Installation

1) `git clone ...`
2) `cd geo-location-api`
3) `bundle install`
4) `rails s`

## Task (Option 1) Description
* Create an API-only on Ruby on Rails Application
* The application implements the following use-cases via API endpoints:
    * Fetch the list of the given areas in GeoJSON format
    * Check if a given Location is inside any of the given areas:
        * IN: GeoJSON of type Point
        * OUT: inside? true/false
* The application should gracefully handle errors
* Automation tests with RSpec
* Put source code in GitHub
* Host an application in the cloud (e.g. Heroku) and provide a link

## How to Run the App

1) To visit home, URL is https://geo-locate-api.herokuapp.com #GET

<img width="1126" alt="home" src="https://user-images.githubusercontent.com/24937779/62769808-a69f6900-ba91-11e9-8d2c-d329987f6d09.png">

2) To fetch list of given areas in GEOJSON format, URL is https://geo-locate-api.herokuapp.com/areas #GET

<img width="1116" alt="get_areas_request" src="https://user-images.githubusercontent.com/24937779/62770214-71dfe180-ba92-11e9-83b6-d9f9fb056ce3.png">

3) To check if the location is inside any of the given areas, URL is https://geo-locate-api.herokuapp.com/areas #POST

<img width="1104" alt="post_inside_request" src="https://user-images.githubusercontent.com/24937779/62770286-a18ee980-ba92-11e9-9456-0d80bc63b168.png">

For (3) above i.e. POST request, the key-value input format should be like the one as shown in the snapshot above i.e.
``{point[0]:-117.86, point[1]:50.23}``.
``type_point`` determines if the input is a valid x-y point while ``inside`` determmines if the point is located within any of the given areas which are boolean results

## Test

Run `rspec`

