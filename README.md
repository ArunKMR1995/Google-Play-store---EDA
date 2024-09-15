# Google-Play-store---EDA
## Introduction
The data is collected from https://www.kaggle.com/datasets/gauthamp10/google-playstore-apps and inspired by work from https://www.kaggle.com/code/bextuychiev/my-6-part-powerful-eda-template.

The data has a total of 2.4M records of applications in the google play store. With billions of android phone in the world google play store is the most important app which allows end users to download and install applications of thier choice. There are many different categories such as

Education
Adventure
Music
Social
Tools
Entertainment and many more.

## Objective
The objective of this notebook is to perform EDA on the different types of apps, ratings, which categories are more popular, understand the user behavior and how play store has grown over time.

## Approach Plan
### Observations
The data contains 2312944 rows and 24 columns.
Has 15 columns with object data type, 5 columns are float(4) and int(1), and 4 are boolean types.
Columns like Released, Last Updated and Scrapped time are represented as object type though their values are datetime.
Out of the 5 numerical columns
Rating: Has range starting from 0 to 5
Installations varies from 0 to billions.
The prices of the applications are either free or charged and the highest paid app is 400.
Note: We are unsure of the denomination value of price.

#### Handling missing values
Out of the ~55 million data points the data frame has ~1.3 million missing values. Since all missing values cannot be dropped we will explore it further.

#### Handling duplicates
We can drop the columns which has the least impact on our dataset such as Size, Currency, Installs, Minimum Installs, Developer ID, Developer Email and App Name.
We have to be cautious while performing EDA with columns associated with
1. Released
2. Rating
3. Rating count
4. Minimum Android
5. Developer website
6. Privacy policy

Based on the data we see there are no duplicate rows. However, there are duplicate entries with app name similarly most of the columns should be having duplicates. But they are not duplicate as they have different app id and other metadata.

#### Data Normalization
We will recategorize the content rating to simple ratings
Everyone -- Everyone, unrated
Teen -- Teen, Everyone 10+
Adults - Adults only 18+, Mature 17+

#### Perform EDA

![image](https://github.com/user-attachments/assets/f87b8498-fe34-4333-9017-b42dd2772f5b)

##### Ratings per Category
![image](https://github.com/user-attachments/assets/79257b64-d987-4721-a224-28cac40cf3fd)

##### Installs by app rating
![image](https://github.com/user-attachments/assets/7cfff8e1-8b8e-4bbc-b72a-a9e8be6df9bb)

##### Installs by payment type
![image](https://github.com/user-attachments/assets/142a9c0b-5dd8-40b5-bd68-5fcdd9ce1e5f)

##### Paid vs free apps by category
![image](https://github.com/user-attachments/assets/b7b148cf-e4b2-45e5-b87b-a409134effc5)

##### Top 10 categories
![image](https://github.com/user-attachments/assets/c754cf68-42ac-479d-8b01-adb4cc3daf63)

##### Top 10 highly rated app category
![image](https://github.com/user-attachments/assets/7eb72954-5a49-48b8-9584-822eedca1e2e)

##### Apps released by year
![image](https://github.com/user-attachments/assets/4385a0dd-cb3f-405d-98f5-ff391819edce)

##### Seasonality - Apps released by month and year
![image](https://github.com/user-attachments/assets/65da62bc-d7ce-45fd-9ffa-de9be9e156f1)

##### Apps released by year and month
![image](https://github.com/user-attachments/assets/cc3ffeb0-e5b1-4495-b93b-a9b7359cffcc)

## Executive Summary
Between 2010 and 2021, a total of 2.3 million apps were released on the Google Play Store. The Education category leads with 18% of all apps released. Tools is the most downloaded category, amassing over 110 billion downloads, followed by Communication with 70 billion downloads. Role-playing apps hold the highest average ratings among all categories. Users tend to favor apps with ratings of 3.5 and above.

## Key Observations
### App Releases:
1. Education apps constitute 18% of all releases up to 2021.
2. Google Play Store crossed 500,000 app releases in 2020.
3. The highest app releases usually occur in Q3 and Q4, but in 2020, Q1 and Q2 saw significant activity.
### Downloads:
1. Tools category leads with over 110 billion downloads.
2. The most downloaded apps are primarily Google-affiliated: Google Play Services, YouTube, Google, Google Maps, and Google Text-to-Speech.
3. Among the top 10 downloaded apps, 40% are Tools, 20% are Communication, and the remaining 40% are divided among other categories.
### User Preferences:
1. Role-playing apps have the highest average ratings.
2. Users prefer downloading apps with ratings of 3.5 and above.
3. Adults rate apps the least, while teens and everyone rate apps the most.
### Free vs. Paid Apps:
1. 98% of apps on the Play Store are free.
2. Education has the highest number of payable apps (6,547), followed by Personalization (5,767).
   
## Recommendations
### Focus on Quality: 
Ensure apps have a rating of 3.5 or higher to increase download rates.
### Leverage Education Category: 
Given its dominance, developers should consider entering or expanding within the Education category, particularly with paid app offerings.
### Optimize Release Timing: 
Align app releases with peak periods in Q3 and Q4 to maximize visibility, but also take advantage of early-year trends observed in 2020.
### Capitalize on Trends: 
Given the high ratings of role-playing apps, developers could explore creating high-quality role-playing games.
### Understand User Demographics: 
Tailor marketing strategies to target teens, who are more likely to rate apps, and enhance features that appeal to this demographic.
** By focusing on these areas, developers and marketers can better align their strategies with observed trends and user preferences to maximize app success and market penetration.
**
