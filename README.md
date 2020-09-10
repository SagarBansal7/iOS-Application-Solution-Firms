# iOS Mobile Application Analytics #
## Graduate Course: Managing with Analytics ##

### Introduction ###

With millions of apps in the market, it is important for app developers to understand the users’ needs as well as the demands of the apps. Most importantly, it is important that app developers understand the success of the applications for further progress in the market. This was a team project from a course on Managing with Analytics. Me and my teammates utilized the Mobile App Statistic data set to analyze and identify trends to support app developers in their efforts to develop successful applications. Recommendations include a prioritized list of industries as well as key aspects driving user downloads to be considered when building an application, to support app developers in their efforts to uncover prospect markets and develop successful applications.

### Data ###

The Mobile Application data set was sourced from Kaggle (Ramanathan, 2017) and was made available by the authors in two parts: a dataset containing the individual application names and characteristics (AppleStore.csv), and an additional dataset with detailed descriptions of the applications (AppleStore_description.csv.). For the purpose of this project, we utilized the full list of applications and their characteristics only (AppleStore.csv file), with a size of 13 MB. The additional app description in the second file was not found to be relevant to the scope of the project and was thus excluded from the analysis. The dataset is comprised of 7,197 applications available in the iOS store, for a total of 7,197 rows and 16 columns. The data was collected on July 2017 from the iTunes Search API in the Apple Inc. website utilizing R and Linux web scraping tools (Ramanathan, 2017). The applications utilized in this data set are the most frequently ranked applications of 2016. This file provides key variables such as user ratings, categories, pricing, and size.

### Methodology

With Mobile Applications Solutions firms as a target audience, the goal of this analysis is to infer the characteristics of mobile applications that drive a high number of users. As the number of users for each app is not publicly disclosed, we used the number of ratings as a proxy for number of users. This key assumption is the foundation of the analysis in the following pages. The assumption is that the amount of ratings is generally proportional to the amount of user downloads. The goal is not to derive the raw number of users, but to compare the characteristics of apps with a larger inferred amount of users against apps with a lower inferred number of users and identify key differences. Furthermore, we sought to identify current app categories that do not yet have a large number of users, but that have growth potential in the future based on user growth. We used the relationship between total user ratings and the number of ratings of the most recent version of the app. The second key assumption driving this section of the analysis is that a larger proportion of ratings for the most recent version of the app is an indication that either the app or the specific Category continues to grow its user base.

Using Tableau, we explored the relationships between the various dimensions and our KPI - total number of ratings, using scatterplots, histograms and distributions. We identified certain variables that were inconclusive in determining the success of an app and were thus excluded from the analysis. These variables include the number of languages in which an app has been made available, the size of an application and the number of devices that can support the application.

### Findings

#### Most Popular Categories

The Gaming category is the largest in our dataset in terms of number of applications available, representing more than half (54%) of the iOS applications, followed by Entertainment (7%), Education (6%), Photos and Video (5%), Utilities (3%) and Health and fitness (3%), with the rest of the categories representing between 2% or less of the total number of applications available.

As expected, the Gaming category also sees the highest total number of ratings. This is, in part, driven by the sheer size of the category, containing the highest number of applications, thus is not a good indicator of app popularity or user downloads. When accounting for the number of applications in each category, it is evident that Gaming apps do not have the highest amount of users per single app and instead, the most popular app categories driving the largest amount of users appear to be Social Networking, Music, Shopping, Weather and Reference.

The figure below highlights the total number of ratings in a category (bar chart ranking) against the amount of ratings per individual app in each category, highlighted by the shaded colors, with the darkest blue bars representing the categories with the largest number of ratings per app. For example, the ‘Games’ category has a total number of ratings of 52.9M with 13.7K ratings per app compared to Social Networking has a total number of ratings of 9.8M and 58.1K ratings per app. 

#### Figure 2 - Total Ratings by Category

![Image 1](https://user-images.githubusercontent.com/37155988/92641205-6cb02000-f2ac-11ea-85ec-06b45a92d947.png)

#### App Pricing 

Pricing plays a significant role in driving app users. Free applications appear to drive more app usage compared to non-free applications across all categories. While $0 applications represent most in our sample, they also drive the highest usage as indicated by the number of ratings per individual application in the ‘free’ app segment. Figure 3 showcases the general trend between the price and inferred number of downloads irrespective of the categories. We represented the variation in ratings per app using the blue-orange color scale, while the size of the bar represents the absolute number of ratings. Low ratings per app are colored in dark orange, while high ratings per app are represented in dark blue. The largest number of apps have a price set to zero and highest ratings/app of 17,832.

Conversely, 621 apps with $1 price have a ratings/app of 3,812, 683 apps with $2 price have a ratings/app of 2,806, 277 apps with $3 price have a ratings/app of 1,661, 394 apps with $4 price have a ratings/app of 3,242 and 166 apps with $6 price have a ratings/app of 5,548. All other price values have app count of less than 100. For non-free applications, there is no apparent relationship between price and app usage, as there are a sizeable number of paid apps with high number of users.

#### Figure 3 - App Price vs Number of Ratings 

![image 6](https://user-images.githubusercontent.com/37155988/92641458-c44e8b80-f2ac-11ea-9875-9a01cd77ab43.png)

While Social Networking apps have the second lowest average price ($0.03), corresponding to the highest number of inferred users (ratings per app ratio of ~58K) there are also a number of paid apps that are in the top 5 categories by app usage. Particularly, the Reference and Music categories have the third ($4.837) and fourth ($4.835) highest average price per app and they also have the third (22,411) and second (28,842) maximum number of downloads, suggesting that customers are willing to pay a higher price for Music apps, as well as for practical applications such as the ones in the Reference categories. (See Figure 4 below)

#### Figure 4 Ratings by Category vs Average Price

![Image4](https://user-images.githubusercontent.com/37155988/92641613-04157300-f2ad-11ea-8fcf-8f74bc89f9bf.png)

#### Visual Marketing of the Apps

We examined the effect of the number of screenshots on the number of ratings for different categories (prime genres). The relationship between the number of screenshots featured in the app store and the number of ratings varies notably by category. There is a positive relationship between the number of screenshots and the number of ratings for each app for Book, Catalogs, Finance, Games, Medical, Music, Navigation, Photos and Video, Productivity, Reference, Shopping, Travel and Utilities. By contrast, for Business, Education, Entertainment, Food and Drink, Health and Fitness, Lifestyle, News and Social Networking, Sports and Weather categories it appears that the number of featured screenshots does not have any effect on app usage. Generally, word of mouth, user need (as in the case of Business and Education) and other forms of advertising likely drive app usage in these categories. In general, it appears that at least three screenshots could drive a higher number of downloads. (See Figure 5 below)

#### Figure 5 Number of Screenshots vs Number of Ratings per App by Category

![Image3](https://user-images.githubusercontent.com/37155988/92641670-142d5280-f2ad-11ea-8522-f7a26023bf1f.png)

#### Category Growth Potential

Under the assumption that most users rate their apps within a few months since download, we calculated the ratio of the number of ratings for the most recent version of the app to the total number of ratings (please refer to the Methodology section for details on the assumptions). A higher ratio indicates that the application or category is continuing to grow its user base, thus representing potential for future investment. App categories such as Utilities (0.11), Lifestyle (0.1156) and Education (0.10) show the highest user growth ratio. However, these categories are generally relatively new to the mobile app ecosystem, therefore they likely have only one version, which they never updated, or they just launched, driving a high percent of ratings on the newest version. Excluding these categories, the highest growth genres are Games, Reference, Weather, Shopping, Photos and Videos. Note that Reference, Weather and Shopping are also among the top 5 by app usage, solidifying the recommendation that they are prioritized by app developers.

#### Figure 6 Rating per App. (Color: Ratio of Ratings of Current Version over Total Ratings)

![Image5](https://user-images.githubusercontent.com/37155988/92641516-e0522d00-f2ac-11ea-95d2-724a945a707a.png)

### Recommendations

1) App developers should consider prioritizing Social Media, Music, Weather, Reference and Shopping apps, as they typically get the most users and have the most monetary potential. The more users an apps gets, the higher the likelihood of driving sales for in-app purchases, advertising, selling aggregated data, in addition to the cost of the actual app.

2) Consider pricing your app relatively low in the Social Media space, as most apps are either free of cost <$1 and an expensive Social Media app would have difficulty competing in the space. Music apps, along with need-based apps in the Business, Reference and Productivity space can be priced >$4.

3) App Visuals can be a powerful means to attract customers as they can give graphical and user- interface insights about the app. However, in certain categories such as business, education, entertainment, news, social networking screenshots do not bear significant weight in driving app usage, as these categories are typically driven by word of mouth and pre-existing popularity. Generally, 3-4 screenshots in the application’s description are recommended for optimal results.

4) Although individual apps in Gaming, Shopping and Photo & Video do not drive the highest usage per individual app, the ratio of current version ratings to the total ratings suggests these categories are still growing and should be considered as target categories in the near future.

### Conclusion

Social media continues to be one of the most engaging mobile app categories, as social media giants are increasingly facilitating many activities, such as shopping, payments, gaming and news-reading, in addition to social interaction. As with many consumer goods and services, the price is a major driver of demand. ‘Free’ apps attract most users, particularly in leisure categories such as Social Media, Shopping and Entertainment, as well as Games, albeit with a higher number of customers willing to pay to play in this category. Free apps have as much monetary potential as paid apps, if not more, thanks to the amount of users available to be exposed to paid ads, as well as the amount of data collected from user activity, which in turn can be sold to data aggregators.

Conversely, while expensive apps drive less users, practical and need-based apps in the Medical and Education fields can be priced very high, as digitization in these industries grows over time. Visual marketing continues to be an important driver of demand. However, app developers must study the current mobile app environment closely to find strategies to compete with existing top performing apps and engage users through various forms of marketing and advertising outside of the app store. Word of mouth and peer groups as well as trusted influencers continue to bear significant weight in driving awareness.

This dataset, while limited, provides insights about the macro-drivers of app usage and emphasize the key foundations of a successful app. However, the app ecosystem is constantly evolving, and additional data is needed to understand the ways in which users engage with apps in order to design or change mobile app development strategies accordingly.

### References

Glauninger, Silke (October 2017). Why Ratings and Reviews Matter in App Store Optimization. Medium. Retrieved from: https://medium.com/app-radar-highlights/why-ratings-andreviews-matter-in-app-store-optimization-5c93d285f029
Nicas, Jack. Collins, Keith (September 2019). How Apple's Apps Topped Rivals in the App Store It Controls. The New York Times. Retrieved from: https://www.nytimes.com/interactive/2019/09/09/technology/apple-app-storecompetition.html
Ramanathan. (2017). Mobile App Store (7200 apps). Retrieved December 7, 2019, from Kaggle.com website: https://www.kaggle.com/ramamet4/app-store-apple-data-set-10kapps/discussion 
Categories and Discoverability - App Store - Apple Developer. (2019). Retrieved from Apple Developer website: https://developer.apple.com/app-store/categories/
AppleInsider. (2017, October 4). Apple pulls Catalogs category from App Store, Dice & Educational subcategories under Games. Retrieved December 8, 2019, from AppleInsider website: https://appleinsider.com/articles/17/10/04/apple-pulls-catalogs-category-fromapp-store-dice-educational-subcategories-under-games
