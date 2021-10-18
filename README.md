# Kickstarting with Excel

## Overview of Project

### Purpose
The primary purpose of this exercise is to extract specific information from a set of raw data, organizing it to most easily visualize and draw conclusions from. This is achieved through the tools available in Microsoft Excel, both having the raw data in a format that can be utilized and using pivot tables and graph generators to most effectively manipulate this data.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Creating a pivot table with Year and Parent Category as filters required extra columns of data, making Parent Category and Subcategory independent columns and Unix time into a readable date and an isolated year. The former required the "Text to Columns" tool of Excel, while the latter required applying a Unix-time converting equation (=X/86400+DATE(1970,1,1)) to increment the number of days from Unix's default time of Jan. 1, 1970. The resulting pivot table used these parameters to generate, with "outcomes2" representing an identical dataset to "outcomes".
![image](https://user-images.githubusercontent.com/77989740/137660736-2b00689a-a3cd-4c66-98fb-402996a1cc5d.png)

### Analysis of Outcomes Based on Goals
Generating new columns from existing data was straightforward - a combination of Excel's functions COUNTIFS, COUNTIF, and SUM accomplished isolating everything necessary to create an effective graph. The function ROUND was not needed for percentiles, as Excel's toolbar accomodates for displaying simple division as a percentile with any desired level of precision. To best represent fractions such as 2/3, 4/6, and 2/16, I designed my percentiles with one decimal point. 
![image](https://user-images.githubusercontent.com/77989740/137661623-61f8ff2e-6dd1-402d-9118-ed9736d0aa23.png)


### Challenges and Difficulties Encountered
When working with the pivot table in the Outcomes Based on Launch Date, I found it difficult to have the outcomes both as a counted variable and a column divider. To overcome this, I duplicated the outcomes column in my Raw Data sheet, naming the latter "outcomes2". I'm unsure if there are solutions to this issue without having to disturb the original dataset. I also found saving the graphs as independent .png files took a roundabout solution of copying the chart into MSPaint first. 
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

There's a significant increase of overall attempts and successes in theater-based kickstarters from May to August. At the same time, the number of failures hardly changes in the same timespan. This shows an overall increased success rate over the summer months, making it the best time to begin a kickstarter for theater. December seems to be the least profitable timing, with failures almost just as likely as successes. 

- What can you conclude about the Outcomes based on Goals?

While the most successful goal value is less than $5000, there's a range of ~$5000-$25000 where the percentage of successful kickstarters remains roughly the same with a slight decline. More ambitious plays requiring larger budgets should aim to stay under this mark, as anything beyond $25000 only has an overall success rate of 40% in its small sample size. I can also note that not a single play-based kickstarter canceled before the funding deadline, and having no outlier in over 1000 campaigns is unusual. 

- What are some limitations of this dataset?

This dataset can't properly include the quality of the project being 'pitched,' nor the previous success of the kickstarter owners. Both influential variables are subjective enough to make tracking in a dataset difficult, but lacking them altogether can lead to an incomplete picture of the data in question.

- What are some other possible tables and/or graphs that we could create?

With the information on hand, there are many possible trends that could be discovered when creating more tables and graphs. Both the number of backers and having a "spotlight" compared to kickstarter success rate could show a positive correlation. The success of kickstarters for certain industries can be graphed over multiple years. Specific parent categories could be compared to their average or median goal, depending on possible outliers. 
