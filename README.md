# Kickstarter-Analysis
Performing analysis on the excel dataset [Kickstarter](https://github.com/sucharita1/kickstarter-analysis/blob/21b450f7ffdacdc10890eace448b5d8b4f3ff46c/Kickstarter-Analysis.xlsx) collected from a crowdfunding website to uncover trends for a successful fundraiser.

## Overview of Project
Louise is a playwright who wants to produce a play 'Fever'. She has estimated that her play will cost her 10000-12000$ and started a crowdfunding campaign. She has come close to her fundraising goal in a short amount of time. She wants to know how different crowdfunding campaigns fared so that she can mirror the successful ones and learn her lessons from the failed ones.

### Purpose
Analyzing [Kickstarter](https://github.com/sucharita1/kickstarter-analysis/blob/21b450f7ffdacdc10890eace448b5d8b4f3ff46c/Kickstarter-Analysis.xlsx) to visualize the outcomes of previous crowdfunding campaigns and draw useful insights to help fund the play 'Fever'
- To find the fate of crowdfunding campaigns i.e. 'successful', 'failed' or 'canceled' based on launch date of the campaign.
- To find the percentage of successful, failed, and canceled plays based on the funding goal amount.
    
## Analysis and Challenges
We can see right off the bat that theatre is the largest and most successful category in the Kickstarter dataset. Louise has come to the right place for a crowdfunding campaign. 
![Outcomes_vs_Category](https://github.com/sucharita1/kickstarter-analysis/blob/02e9f98eedba6b72198c4b6807476680eae3f705/Resources/Outcomes_vs_Category.png?raw=true)

For beter insights, we will look into analysis of outcomes based on goals and launch date of the fundraisers for theatre category.

### Analysis of Outcomes Based on Launch Date
Louise was a little concerned about whether she launched her campaign at the right time  so lets find out the outcomes for previous fundraisers based on  the launch month.

![Theatre_Outcomes_vs_Launch](https://github.com/sucharita1/kickstarter-analysis/blob/16de63190d2fddcc3cfd50b49f1bcf55ecce118c/Resources/Theater_Outcomes_vs_Launch.png?raw=true)

By using line chart to analyze the trend every month we can say that:
- The most successful campaigns were lauched in May and but those launched in June, July were fairly successful too. April and August months also were better than the rest of the year but success fell drastically from October to December.

- The failure rate was pretty constant till April but it was the least in May. Failure in June and July was low too. There was a rise in October and December.

Finally, We see a clear spike in the line chart which suggests that launch dates have a big role to play in the success of theatre category.

### Analysis of Outcomes Based on Goals
Louise estimated a budget of 10000$-12000$ for her play and she wants to know the fate of other plays which had a goal similar to hers, so we checkout the sub cateogory plays and divide the outcomes based on the goal amount  so can see that foresee the fate of her campaign and if needed adjust her goals for better success.

![Outcomes_vs_Goals](https://github.com/sucharita1/kickstarter-analysis/blob/02e9f98eedba6b72198c4b6807476680eae3f705/Resources/Outcomes_vs_Goals.png?raw=true)

By using line chart to analyze the trend for goals we can say that:
- The success percentage is more than 70 for goals under the budget of 5000$ and falls dramatically. It comes close to 70 again between 35000 to 45000$ only to fall dismally again for goals higher than 45000$. 
- At the budget range of 10000$-14999$ the chances of success is only a slight more than failure.

Finally we see that success shows clear promise only for goals under 5000$ but keeps plummeting untill it reaches 25000$.

### Challenges and Difficulties Encountered
Since the data belonged to a crowdfunding website the category section included food, television, technology initiatives also. So narrowing down our data was a must.

- The data in theatre category also included spaces and musicals too. Most of the entries under spaces had huge goals and failed a lot. So we created a new sub category by converting Category/Subcategory to seperate columns.

- The data also contained dates in unix format (seconds passed since January 1, 1970) which had to be converted to date type by dividing the unix date by 86400 and adding DATE(1970,1,1).

- Though plays is a sub category but plays can be of many types and generate income and interest in different age groups. But we don't know what type of play it is unless we go through every blurb which is tedious. We used Vlookup to checkout the data of some plays similar to ones Louise plans to produce in UK later.  

## Results
### Conclusions on Outcomes based on launch date
1. The best time to launch the play is May but if you are pressed for time June and July are good too.
2. The worst time to launch the play will be October or December. 

### Conclusions on Outcomes based on Goals
1. For a goal of 10000$-12000$ 54.17% of the projects succeeded and 45.83% failed. If Louise could bring down her budget close to 4000$ she would be in a sweet spot.

It would be in her best interest to keep her budget as tight as possible by bringing down some of the costs shown below. We would suggest to cut down on amount allocated to Costumes, props , sets by re-using all stuff from her plays before. Also Rehearsing at cheaper venues and advertizing via social media would bring down those costs too.
    
![Louise_Budget](https://github.com/sucharita1/kickstarter-analysis/blob/02e9f98eedba6b72198c4b6807476680eae3f705/Resources/Louise_Budget.png?raw=true)


### Limitations of the dataset
- The biggest limitation of the dataset is that we don't have enough information about the backers, the real people who will fund the campaign. If we knew the demography like the age, sex of the backers we could do targeted advertizing using social media on a very small advertizing budget and generate greater funds.

- Though we have a lot of data about plays but it is not sub categorized into types of plays etc. some of the entries in the plays sub category are also about lighting or makeup. Had there been a play subtype we could have visualized the data based plays similar to 'Fever'.

### Some other possible graphs and tables that we could create
Some more graphs that could be added are:
1. A Category_vs_success pie chart for US to clearly see that theater is a popular and successful type of campaign in US. Louise need not think twice before starting a crowdfunding campaign here.
![Category_vs_success_US](https://github.com/sucharita1/kickstarter-analysis/blob/02e9f98eedba6b72198c4b6807476680eae3f705/Resources/Category_vs_success_US.png?raw=true)

2. It is important that Louise's goal should be the right amount so a boxplot for plays in US makes it easier to spot the outliers

![Goals_vs_pledged](https://github.com/sucharita1/kickstarter-analysis/blob/02e9f98eedba6b72198c4b6807476680eae3f705/Resources/Goals_vs_pledged.png?raw=true)

Here we can see clearly that Louise's goal of 10000$-12000$ is outside the upper bound for pledged amount so Louise needs to bring her budget down or else she may not be able raise enough funds

3. It is important to know how campaigns have performed over the years so that we can plot a bar chart displaying Outcomes based on the year of launch.
![Outcomes_vs_year](https://github.com/sucharita1/kickstarter-analysis/blob/02e9f98eedba6b72198c4b6807476680eae3f705/Resources/Outcomes_vs_year.png?raw=true)

Here we can see that the crowdfunding campaigns have really picked up since the year 2014 and the website has been hosting numerous campaigns in the sub category plays for the country US since 2014. 


Finally, We believe with a budget close to 5000$, Louise has a great chance of raising the funds and we wish her play 'Fever' become a huge success.

    


    
    














    

    


   









