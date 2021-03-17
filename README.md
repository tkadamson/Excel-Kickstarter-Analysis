# hw1-kickstarter-analysis

## Project Instructions | Grade: A
Using the Excel table provided, modify and analyze the data of 4,000 past Kickstarter projects as you attempt to uncover some market trends.

* Use conditional formatting to fill each cell in the `state` column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.

* Create a new column O called `Percent Funded` that uses a formula to uncover how much money a campaign made to reach its initial goal.

* Use conditional formatting to fill each cell in the `Percent Funded` column using a three-color scale. The scale should start at 0 and be a dark shade of red, transitioning to green at 100, and blue at 200.

* Create a new column P called `Average Donation` that uses a formula to uncover how much each backer for the project paid on average.

* Create two new columns, one called `Category` at Q and another called `Sub-Category` at R, which use formulas to split the `Category and Sub-Category` column into two parts.

* Create a new sheet with a pivot table that will analyze your initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per **category**.

* Create a stacked column pivot chart that can be filtered by country based on the table you have created.

* Create a new sheet with a pivot table that will analyze your initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per **sub-category**.

* Create a stacked column pivot chart that can be filtered by country and parent-category based on the table you have created.

* The dates stored within the `deadline` and `launched_at` columns use Unix timestamps. Fortunately for us, [there is a formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) that can be used to convert these timestamps to a normal date.

* Create a new column named `Date Created Conversion` that will use [this formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `launched_at` into Excel's date format.

* Create a new column named `Date Ended Conversion` that will use [this formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `deadline` into Excel's date format.

* Create a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.

* Now create a pivot chart line graph that visualizes this new table.

* Create a report in Microsoft Word and answer the following questions.

1. Given the provided data, what are three conclusions we can draw about Kickstarter campaigns?
2. What are some limitations of this dataset?
3. What are some other possible tables and/or graphs that we could create?

* Create a new sheet with 8 columns:

  * `Goal`
  * `Number Successful`
  * `Number Failed`
  * `Number Canceled`
  * `Total Projects`
  * `Percentage Successful`
  * `Percentage Failed`
  * `Percentage Canceled`

* In the `Goal` column, create 12 rows with the following headers:

  * Less than 1000
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

* Using the `COUNTIFS()` formula, count how many successful, failed, and canceled projects were created with goals within the ranges listed above. Populate the `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data.

* Add up each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column. Then, using a mathematical formula, find the percentage of projects that were successful, failed, or canceled per goal range.

* Create a line chart that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.

* Create a new worksheet in your workbook, and create a column each for the number of backers of successful campaigns and unsuccessful campaigns.

* Use Excel to evaluate the following for successful campaigns, and then for unsuccessful campaigns:

  * The mean number of backers.

  * The median number of backers.

  * The minimum number of backers.

  * The maximum number of backers.

  * The variance of the number of backers.

  * The standard deviation of the number of backers.

* Use your data to determine whether the mean or the median summarizes the data more meaningfully.

* Use your data to determine if there is more variability with successful or unsuccessful campaigns. Does this make sense? Why or why not?

## Analysis

#### Given the provided data, what are three conclusions we can draw about Kickstarter campaigns?

1.	In this sample, the Theater category, and Plays specifically, had the highest number of Kickstarter campaigns by far. In terms of outcomes, more than half were successful, but even the failed theater campaigns outnumber the total number of campaigns in any other category. This trend holds among most all countries with a sample size of 25 or more projects. 
2.	Music was the second-most pursued campaign category. Interestingly, one hundred percent of Rock campaigns were successful. Combined with the point above, these suggest that those that engage in Kickstarter campaigns, as well as those that back them, prefer projects that can generally be put in the broader category of Arts & Culture.
3.	As a general trend, campaigns that set a higher goal for the number f backers tended to fare worse off. As the goal gets higher, success drops quite dramatically, from over 70 percent successful for the smallest campaigns to under 20 percent for the largest campaigns. This could be suggestive of a couple of things. It may be difficult to attract large numbers of backers for Kickstarter campaigns in general. It may also be that more ambitious campaigns over promise on what is actually needed as an upfront investment to get their project off the ground. It is easy to imagine a campaign that promises to be revolutionary, but the technology isn’t quite advanced enough for eventual market sale.

#### What are some limitations of this dataset?

First of all, this data set is a random sample of all Kickstarter campaigns, so the full data set may portray a different picture that hat can be gathered here. More importantly, it is important not to draw any broader conclusions about entrepreneurship or innovations from Kickstarter data alone. Kickstarter is a great platform for creating interesting ideas and products, but it can’t tell us all that much about hat people actually want or need beyond what is interesting to them. Kickstarter may be prone to more flashy and innovative ideas, so as to attract more backers, but it doesn’t give a wider window into general innovation and how it might impact peoples’ lives.

#### What are some other possible tables and/or graphs that we could create?

One chart that would be interesting is the average donation by category and sub-category. I hypothesize that the Tech category has the highest average donation based on the ambitiousness of those projects, the crowded market for such projects, and the incomes of people donating to those campaigns, but I would like to see that data there. 

I would also like to use the Staff Pick and Spotlight columns to see if there is a significant difference in outcomes for those that were highlighted by the Kickstarter platform.

#### Bonus: Use your data to determine whether the mean or the median summarizes the data more meaningfully.

In this case, the median is a more useful measure of central tendency for these data sets. This is because, using a back-of-the-envelope 1.5 IQR test, there are a significant number of outliers in both directions. Since the mean weights outliers heavily, median is more appropriate in this case. 

#### Bonus: Use your data to determine if there is more variability with successful or unsuccessful campaigns. Does this make sense? Why or why not?

According to the calculations done here, successful campaigns have a much higher variance than unsuccessful campaigns. This would make sense given that many unsuccessful campaigns have no backers, which is much close to the median number of backers than the successful campaigns which have a wider range of backers. 

