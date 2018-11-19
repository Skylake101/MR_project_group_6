# Map Reducing Google Play Store Applications and Analysis

## Developers:

Jesse Alford II, Luke Carlson, Hitesh Kolla, and Naresh Vunnam

## Background

The Google Play Store is an app store for mobile applications available on mobile devices such as phones and tablets running Android. Android device owners are able to access the Google Play Store and download thousands of apps. Each app store page includes its own attributes such as ratings, reviews, app type, and updates. 

## Data Source

https://www.kaggle.com/lava18/google-play-store-apps


## Big Data Qualifications

This is a big data problem due to the “Volume” and “Variety” big V’s. This file contains over 70,000 records of varying information, making this a key candidate for a map reduce problem.


## Big Data Questions

For each category find the average ratings.
For each category find the maximum number of reviews.
For each category find the lowest size.
For each year find the total number of apps that are updated.

## Big Data Solutions

For each category find the average ratings.

	Mapper input:  	
		-App: Photo Editor & Candy Camera & Grid & ScrapBook
		-Category: ART_AND_DESIGN
		-Rating: 4.1
		-Reviews: 159
		-Size: 19MB
		-Installs: 10,000+

	Mapper output / Reducer input:  key: ART_AND_DESIGN, value: 4.9 (example:ART_AND_DESIGN, 4.9 )
	Reducer output:   key: ART_AND_DESIGN, value: 4.9 (average: 3.5 )
	Language:  We will be using Python for our MR project.
	What kind of chart will you use to display your results?  Bar Graph

For each category find the maximum number of reviews

	Mapper input:  
		-App: Coloring Book Moana
		-Category: ART_AND_DESIGN
		-Rating: 3.9
		-Reviews: 967
		-Size: 14MB
		-Installs: 500,000+

	Mapper output / Reducer input:  key: ART_AND_DESIGN, value: 967 (example:ART_AND_DESIGN, 967 )
	Reducer output:   key: ART_AND_DESIGN, value: 967 (maximum: 967)
	Language:  We will be using Python for our MR project.
	What kind of chart will you use to display your results?  Bar Graph

For each category find the lowest size

	Mapper input:  
		-App: Draw & Paint
		-Category: ART_AND_DESIGN
		-Rating: 4.5
		-Reviews: 215,644
		-Size: 25MB
		-Installs: 50,000,000+

	Mapper output / Reducer input:  key: ART_AND_DESIGN, value: 25 (example:ART_AND_DESIGN, 25 )
	Reducer output:   key: ART_AND_DESIGN, value: 25 (minimum: 25 )
	Language:  We will be using Python for our MR project.
	What kind of chart will you use to display your results?  Bar Graph

For each year find the total number of apps that are updated

	Mapper input:  
		-App: Infinte Painter
		-Category: ART_AND_DESIGN
		-Size: 29MB
		-Installs: 1,000,000+
		-Content Rating: Everyone
		-Last Updated: 14-Jun-18

	Mapper output / Reducer input:  key: year, value: 10 (example:year, 10 )
	Reducer output:   key: year, value: 10 (2018: 10 )
	Language:  We will be using Python for our MR project.
	What kind of chart will you use to display your results?  Bar Graph
