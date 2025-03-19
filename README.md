<img src="Kickstarter-logo.jpg" width="200" height="150"/>

#  Analysis of Kickstarter Website Data (Board Games)
This repository analyzes Kickstarter data to identify key success factors for board game campaigns. It provides insights and recommendations to help creators optimize their crowdfunding strategy.        

           

## Project Overview  
In this project, we were assigned to analyse data from the Kickstarter website to understand the crowdfunding process and identify key factors that contribute to a successful campaign. Our goal is to provide valuable insights and actionable recommendations for someone who is planning to launch a Kickstarter campaign specifically for a board game.  

## Data  
Source Data  
• Website link: (Kickstarter web link)  
• Raw data: (The Data we were given)  
• Profiled data: (The Data we cleaned using PowerBI)  
• Cleaned data: (The Data we cleaned using Python)  

## Data Acquisition  
The data was web scrapped from the Kickstarter website (the link is given in the above section).  
 
## Data Dictionary  
| Column Name         | Description                                                       | Data Type    |  
|---------------------|-------------------------------------------------------------------|--------------|  
| `Project_id`        | A unique identifier for each project.                             | Integer      |  
| `Category`          | The category under which the project was launched (e.g., “Games”, "Technology", "Art"). | Text      |  
| `Subcategory`       | A more specific classification within the main `category`(eg, “Board & Card Games”, “Video Games”)                             | Text     |  
| `City`        | The geographic location of the project creator or where the project is based.          | Text     |  
| `State`        | The geographic location of the project creator or where the project is based.          | Text     |  
| `Status`            | The status of the funds received (e.g., "successful", "failed", “live”).   | Text  |  
| `Goal`              | The funding goal the project aims to raise in USD.                             | Whole Number    |  
| `pledged`           | The total amount of money pledged by backers in USD.              | Whole Number        |  
| `funded percentage` | The percentage of the funding goal that the project have received                          | Percentage     |  
| `backers`           | The total number of backers (Sponsors) who funded for the project.                      | Whole Number     |  
| `Date`       | The date and time when the project was launched.                  | Date    |  
| `Levels`            | Different tiers or levels of pledge amounts set by the project creator.                         | Whole Number     |  
| `Reward Levels` | The rewards or perks that players receive at each `level` | Text      |  
| `Updates` | Regular posts or emails to keep backers informed about progress, milestones, or challenges | Whole Number        |  
| `Duration`        | The duration of the project campaign in days                           | Whole Number      |  
| `Total Reward` | Sum of the rewards or perks that players receive at each `level` | Text      |  

## Data Preprocessing  
The data was first profiled and cleaned in PowerBI, here is a step by step guide for the cleaning:  
1. Filtered board games from the whole data, because our task was to analyse the board games only.  
2. The location column had the state and city both together, that column was split into two different columns, state and City/Country.  
3. Removed the duplicate rows.  
4. The subcategory column had the same type of board games just with two different names, we created a custom column renaming both categories to “Board Games”. Then replaced it with the original one.  
5. The Date column had date and time both in it, we just need the date in it, so we changed the column data type from date and time to date.  
6. Changed the types of columns: Funded Percentage, from float to percentage; Duration, from float to whole number.  
7. We copy and pasted the table from PowerBI to excel to extract the data, and then saved it as a CSV file.  

After we were done with most of the cleaning part in PowerBI, we couldn’t clean the column Reward Levels in it, so we used Python to add another column.  
1. We first imported two libraries pandas and re.  
2. We read the file using pandas.  
3. We created a column “Total Reward” where the values were the sum of reward levels using the library re.  

## Quantitative Analysis  


## Qualitative Analysis


