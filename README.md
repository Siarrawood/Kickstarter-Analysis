# Kickstarting with Excel
## Overview of Project
* This project explores the various trends in project campaigns to help a friend, Louise, establish her campaign strategy. The Kickstarter data was organized and sorted, and visualizations were created to strengthen the analysis. 
* First, the data was filtered so we could focus on the projects that had a similar monetary goal as Louis of $12,000. Conditional formatting was then used to organize the outcomes column of the Kickstarter campaigns in the data: cells that denoted a successful campaign were colored green and those that represented failed campaigns were colored red. 
* The deficit between the fundraising goal and the amount pledged was calculated using Excel's ROUND formula to measure how much of the campaign's goal was actually met. We made a new column in the data for easier visualization. Then, how close a campaign came to reaching or even exceeding the funding goal could be rapidly determined. It seemed many campaigns only barely missed their goal amount.
* In order to help Louise organize her incentives, it would be useful to see how much money people pledge to campaigns in the past. Using the ROUND formula again with the Pledged column data, we just slightly modified it to specify 2 digits after the decimal rather than a whole number.   
* The new column created had errors that had to be dubugged. While all campaigns had a fundraising goal not every campaign has backers. Since there is no number to dived by in the formula, an error occurs that should be cleaned up. We nested the =IFERROR(value,value_if_error) formula and the ROUND formula so we get a zero-value input. Filters were appled on the cells to only include the Theater category because Louise is only interested in the theater campaigns. 
### Purpose
* The purpose of this project is to analyze crowdfunding data to help determine trends in project campaigns using Excel. Specifically, comparing the outcomes of different campaigns based on their launch dates and their funding goals through summary tables, charts, and graphs.  
## Analysis and Challenges
* While Louise is focused on theater campaigns, it is beneficial to look at the outcomes of all the categories for additional insight.
* The data was broken down further by separating the "Category and Subcategory" into 2 separate columns: "Parent Category" and "Subcategory." I generated a pivot chart to help Louise determine if the the length of a campaign correlates with its success. I then created a line chart with the same data as I am looking at trends over time. 
### Analysis of Outcomes Based on Launch Date
![](Theater_Outcomes_vs_Launch.png)
* Pivot tables and graphs in Excel were used to visualize the campaign outcomes based on the launch date. The outcomes were labeled as "successful," "failed," or "canceled."
* A new column was created in the workbook and the year was extracted from the "Date Created Conversion" column using the following code
```
YEAR(serial_number)
```
### Analysis of Outcomes Based on Goals
![](Outcomes_vs_Goals.png)
### Challenges and Difficulties Encountered
* Navigating throughout the Excel sheet tabs proved challenging after there were so many of them. It seemed like all of my work was kind of scattered in many different worksheets and it was difficult to arrange them sensibly. 
* When my formulas had errors, the pop-up did not really give much direction or help so it took some time for me to figure it out on my own. Using the VLOOKUP formula proved challenging for me as I kept trying to use the formula without absolue reference. I had to learn that cells serving as references must be fixed with the "$".
* Learning the Markdown Syntax was a challenge for me as I have never used Github or made a README. I kept getting an error when uploading my graphs from the Excel worksheet into the README. 
## Results
* The launch date of a campaign does correlate with its success. Campaigns launched in the spring and summer months, particulary May, June, and July are more likely to be successful than those beginning in the winter months like November and December. 
* Failed Kickstarter campaigns have much higher fundraising goals than those that are successful. Campaigns that were funded with under $4,000 had the most success rate at about 80%.  
* Some limitations of this dataset 
* We could graph the 
