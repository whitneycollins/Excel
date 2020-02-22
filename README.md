# Unit 1 | Excel Assignment - KickStart My Chart

## Background

Over two billion dollars have been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the over 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Since getting funded on Kickstarter requires meeting or exceeding the project's initial goal, many organizations spend months looking through past projects in an attempt to discover some trick to finding success. For this week's homework, you will organize and analyze a database of four thousand past projects in order to uncover any hidden trends.

## Overview

![Kickstarter Table](Images/FullTable.PNG)

* Using the Excel table provided, you will be modifying and analyzing the data of four thousand past Kickstarter projects as you attempt to uncover some of the market trends.

* Use conditional formatting to fill each cell in the `state` column with a different color, depending on whether the associated campaign was "successful," "failed," "canceled," or is currently "live".

* Create a new column at column O called `percent funded` that uses a formula to uncover how much money a campaign made towards reaching its initial goal.

  * Use conditional formatting to fill each cell in the `percent funded` column using a three-color scale. The scale should start at 0 and be a dark shade of red, transitioning to green at 100, and then moving towards blue at 200.

* Create a new column at column P called `average donation` that uses a formula to uncover how much each backer for the project paid on average.

* Create two new columns, one called `category` at Q and another called `sub-category` at R, which use formulas to split the `Category and Sub-Category` column into two parts.

  ![Category Stats](Images/CategoryStats.PNG)

  * Create a new sheet with a pivot table that will analyze your initial worksheet to count how many campaigns were "successful," "failed," "cancelled," or are currently "live" per **category**.

    * Create a stacked column pivot chart that can be filtered by `country` based on the table you have created.

  ![Subcategory Stats](Images/SubcategoryStats.PNG)

  * Create a new sheet with a pivot table that will analyze your initial sheet to count how many campaigns were "successful," "failed," "cancelled," or are currently "live" per **sub-category**.

    * Create a stacked column pivot chart that can be filtered by `country` and `parent-category` based on the table you have created.

* The dates stored within the `deadline` and `launched_at` columns are using unix timestamps. Fortunately for us, [there is a formula](http://spreadsheetpage.com/index.php/tip/converting_unix_timestamps/) out there that can be used to convert these timestamps into a normal date.

  * Create a new column named `Date Created Conversion` that will use [this formula](http://spreadsheetpage.com/index.php/tip/converting_unix_timestamps/) to convert the data contained within `launched_at` into Excel's Date format

  * Create a new column named `Date Ended Conversion` that will use [this formula](http://spreadsheetpage.com/index.php/tip/converting_unix_timestamps/) to convert the data contained within `deadline` into Excel's Date format

  ![Outcomes Based on Launch Date](Images/LaunchDateOutcomes.PNG)

  * Create a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.

  * Now create a pivot chart line graph that visualizes this new table.

* Create a report in Microsoft Word and answer the following questions...

1. What are three conclusions we can make about Kickstarter campaigns given the provided data?
2. What are some of the limitations of this dataset?
3. What are some other possible tables/graphs that we could create?

* Create a new sheet with 8 columns: `Goal`, `Number Successful`, `Number Failed`, `Number Canceled`, `Total Projects`, `Percentage Successful`, `Percentage Failed`, and `Percentage Canceled`

  * In the `goal` column, create twelve rows with the following headers...

    * Less Than 1000
    * 1000 to 4999
    * 5000 to 9999
    * 10000 to 14999
    * 15000 to 19999
    * 20000 to 24999
    * 25000 to 29999
    * 30000 to 34999
    * 35000 to 39999
    * 40000 to 44999
    * 45000 to 49999
    * Greater than or equal to 50000

    ![Goal Outcomes](Images/GoalOutcomes.PNG)

  * Using the `COUNTIFS()` formula, count how many successful, failed, and canceled projects were created with goals within those ranges listed above. Populate the `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data.

  * Add up each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column. Then, using a mathematic formulae, find the percentage of projects which were successful, failed, or were canceled per goal range.

  * Create a line chart which graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.


## Conclusions
### What are three conclusions we can make about Kickstarter campaigns given the provided data?
Successful campaigns decline over the period. While a gain during the summer months peaked, the overall trend falls over the time period.
Campaigns that had failed or were canceled were fairly steady throughout the months. Canceled were relatively low in comparison to the other outcomes which means that most campaigns were either successful or failed.
A significant amount of campaigns were in theater and plays, where about ⅔ of the play campaigns had success.

### What are some of the limitations of this dataset?
This data set has roughly ¾ its data pulled from US campaigns. So any significant events that may have occurred in the United States would largely affect this data collected. That being said, many other countries may have limited resources or ability to promote a campaign. 
This collected data is represented in different currencies. Without a common currency, the average pledge per backer is different for multiple countries, which we have here.

### What are some other possible tables/graphs that we could create?
A table or graph that would help would be to find a common currency amongst the data. Since currencies are not equal, the amount pledged or needed (Goal) can vary. This can show new info in regards to what category has the biggest interest and success or fail.
A visual for pledged amounts and outcomes would also be helpful. This would help determine the probability of being successful with no, small or large pledges. This chart would help us see the correlation between the amount of funds the campaign has earned and level of success.

