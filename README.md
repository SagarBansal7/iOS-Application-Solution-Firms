# iOS Mobile Application Analytics #
## Graduate Course: Managing with Analytics ##

This was a project from a course on Managing with Analytics.

### Introduction ###

With millions of apps in the market, it is important for app developers to understand the users’ needs as well as the demands of the apps. Most importantly, it is important that app developers understand the success of the applications for further progress in the market. We utilized the Mobile App Statistic data set to analyze and identify trends to support app developers in their efforts to develop successful applications. Recommendations include a prioritized list of industries as well as key aspects driving user downloads to be considered when building an application, to support app developers in their efforts to uncover prospect markets and develop successful applications.

### Data ###

The Mobile Application data set was sourced from Kaggle (Ramanathan, 2017) and was made available by the authors in two parts: a dataset containing the individual application names and characteristics (AppleStore.csv), and an additional dataset with detailed descriptions of the applications (AppleStore_description.csv.). For the purpose of this project, we utilized the full list of applications and their characteristics only (AppleStore.csv file), with a size of 13 MB. The additional app description in the second file was not found to be relevant to the scope of the project and was thus excluded from the analysis. The dataset is comprised of 7,197 applications available in the iOS store, for a total of 7,197 rows and 16 columns. The data was collected on July 2017 from the iTunes Search API in the Apple Inc. website utilizing R and linux web scraping tools (Ramanathan, 2017). The applications utilized in this data set are the most frequently ranked applications of 2016. This file provides key variables such as user ratings, categories, pricing, and size.

### Methodology

With Mobile Applications Solutions firms as a target audience, the goal of this analysis is to infer the characteristics of mobile applications that drive a high number of users. As the number of users for each app is not publicly disclosed, we used the number of ratings as a proxy for number of users. This key assumption is the foundation of the analysis in the following pages. The assumption is that the amount of ratings is generally proportional to the amount of user downloads. The goal is not to derive the raw number of users, but to compare the characteristics of apps with a larger inferred amount of users against apps with a lower inferred amount of users and identify key differences. Furthermore, we sought to identify current app categories that do not yet have a large amount of users, but that have growth potential in the future based on user growth. We used the relationship between total user ratings and the number of ratings of the most recent version of the app. The second key assumption driving this section of the analysis is that a larger proportion of ratings for the most recent version of the app is an indication that either the app or the specific Category continues to grow its user base.

Using Tableau, we explored the relationships between the various dimensions and our KPI - total number of ratings, using scatterplots, histograms and distributions. We identified certain variables that were inconclusive in determining the success of an app and were thus excluded from the analysis. These variables include the number of languages in which an app has been made available, the size of an application and the number of devices that can support the application.

### Findings

#### Most Popular Categories

The Gaming category is the largest in our dataset in terms of number of applications available, representing more than half (54%) of the iOS applications, followed by Entertainment (7%), Education (6%), Photos and Video (5%), Utilities (3%) and Health and fitness (3%), with the rest of the categories representing between 2% or less of the total number of applications available.

As expected, the Gaming category also sees the highest total number of ratings. This is, in part, driven by the sheer size of the category, containing the highest number of applications, thus is not a good indicator of app popularity or user downloads. When accounting for the number of applications in each category, it is evident that Gaming apps do not have the highest amount of users per single app and instead, the most popular app categories driving the largest amount of users appear to be Social Networking, Music, Shopping, Weather and Reference.

The figure below highlights the total number of ratings in a category (bar chart ranking) against the amount of ratings per individual app in each category, highlighted by the shaded colors, with the darkest blue bars representing the categories with the largest number of ratings per app. For example, the ‘Games’ category has a total number of ratings of 52.9M with 13.7K ratings per app compared to Social Networking has a total number of ratings of 9.8M and 58.1K ratings per app. 

#### Figure 2 - Total Ratings by Category

![Image 1](https://user-images.githubusercontent.com/37155988/92641205-6cb02000-f2ac-11ea-85ec-06b45a92d947.png)


