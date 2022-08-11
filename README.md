# Analysis of Kickstarter Data for Theater Projects and by Goal

## Overview of Project
This project analyzed the outcomes of Kickstarter projects in the theater category as well as the outcomes of projects based on the level of funding requested.
## Purpose
The purpose of this analysis is to help maximize the likelihood of success of Louise's play Fever.
## Analysis and Challenges
To analyze both the outcomes based on launch date and the outcome based on goals, filtered the data to make sure I was only analyzing relevant data. Then, I made a line graph to represent the data graphically.
### Analysis of Outcomes Based on Launch Date
To analyze the outcomes based on launch date, I used a PivotTable. I filtered the PivotTable based on years and parent category. I put the outcomes into columns, count of outcomes in values, and date created in rows as shown in the screenshot below.
![Pivottable](https://user-images.githubusercontent.com/109701875/182739203-1bb582bf-8860-4317-ace2-59581b0f1a7b.PNG)!

 

I then made a line graph to show how each month compared.
 ![image](https://user-images.githubusercontent.com/109701875/182731431-badfe07c-aa4d-436b-a77c-abc4deca1364.png)

### Analysis of Outcomes Based on Goals
To analyze the outcome based on goals, I used COUNTIFS to determine the number of successes, failures, and cancels for each category. For example, I used the code COUNTIFS(Kickstarter!D:D, "<1000",  Kickstarter!F:F, "successful") to determine the number of successful campaigns that aimed to raise under $1000. After calculating the number of successes, failures, and cancels I used SUM to determine the total number of projects in each category. For example, I used the code =SUM(B2:D2) to determine the number of successful campaigns that aimed to raise under $1000. Then, I calculated the percentage of successes, failures, and cancels by dividing each by the total number of projects.  For example, I used the code =B2/E2 in a percentage box to determine 75.81% of all finished projects that try to raise under $1000 are successful. Then I made the line graph below.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/109701875/184043368-9c91b4e3-f0d2-4456-991b-455faf3df9ff.png)


### Challenges and Difficulties Encountered
The sole difficulty I had was getting my dataset for Outcomes based on Goal to match the expected output. I quickly found the error I made was that rather than analyzing based on the goal data, I had instead used the amount pledged data. By fixing this mistake, I was able to output the expected graph. 
## Results
- What are two conclusions you can draw about the Outcomes based on Launch Date?
The first conclusion I can draw about the Outcomes based on Launch Date is that theater projects launch in the summer months (April to August). These five months have 693 out of 1369 results. This information was determined by using SUM(E9:E13) on my Outcomes based on Launch Date worksheet. However, projects launched in these months are not significantly more likely to succeed than the average. By calculating the percentage of successes, I determined that projects launched in these months succeed 63.63% of the time compared to an average success rate of 61.28%. I determined these percentage by using SUM(B9:B13) to sum the successes for the results then dividing that sum by SUM(E9:E13) and comparing it to total successes divided by total projects.
My second conclusion is that projects launched in June are the most likely to succeed. By dividing the successes each month by the failures, I found June projects succeed 65.35% of the time. This percentage is higher than any other month.
- What can you conclude about the Outcomes based on Goals?
The main conclusion I draw from outcomes based on goals is that Kickstarter campaigns that try to raise more money are less likely to be successful. Projects that try to raise under $1000 succeed over 75% of the time while those that try to raise over $50000 succeed just 12.5% of the time. 
- What are some limitations of this dataset?
The first limit of the dataset is that it only contains projects up to 2017. It is quite possible that the trends we are analyzing have changed significantly since 2017.
Second, the dataset is lacking data on donors. How often are successful projects often funded by friends and family or by former fans or customers of an established group? Both questions are relevant to our analysis as it may affect the likelihood of success of a project. 
Finally, the dataset is missing any efforts taken outside of Kickstarter to advertise the project or attract donors. These efforts can be rather extensive and may be a serious contributor to the success of a project. For example, https://www.kickstarter.com/projects/mattcolville/mcdm-monster-book?ref=discovery&term=mcdm is a project that raised three times its rather significant $600,000 goal. Efforts to advertise this project outside of Kickstarter include three YouTube videos
(https://www.youtube.com/watch?v=23hEW88OtVM&t=50s, https://www.youtube.com/watch?v=zasXVokJrEk&t=89s, https://www.youtube.com/watch?v=LhJeOOGiWGM ) each with over 50,000 views alongside other efforts.  
- What are some other possible tables and/or graphs that we could create?
One possible different table to look at would be to combine the two tables I created. Although there may be sample size issues looking at theater projects by goal may provide useful information. Another useful table would be to look at the success of projects based on length of campaign. I could create this table by subtracting the creation date from the deadline to determine the length of the project then sorting by success, failure, and cancellation. A final graph we could construct would be a regression analysis of if the spotlight assists with a successful project.
