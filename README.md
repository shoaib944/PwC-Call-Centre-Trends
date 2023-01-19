# PwC Virtual Internship: Call Centre Trends

## Problem Statement:
Create a dashboard in Power BI for Manager that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

Possible KPIs include (to get you started, but not limited to):

Overall customer satisfaction
Overall calls answered/abandoned
Calls by time
Average speed of answer
Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

## Data Visualization
The Call Center Dashboard : Shows KPIs including overall customer satisfaction, overall calls answered/abadoned, calls by time, average speed of answer, agents performance quadrant -> average handle time(talk duration) vs calls answered

[Call center trends dashboard](https://app.powerbi.com/reportEmbed?reportId=ecf91857-9f21-439e-a1f7-f4bfdb1c55c1&autoAuth=true&ctid=18ad1c71-54c7-423e-bef1-c92c52084505)

## Analysis
There are few quick measures used to get the certain insights:

- #Answered =  CALCULATE(COUNTA('Sheet1'[Call Id]), 'Sheet1'[Answered (Y/N)] IN { "Y" })
- #Resolved = CALCULATE(COUNTA('Sheet1'[Call Id]), 'Sheet1'[Resolved] IN { "Y" })
- #CR = DIVIDE([#Resolved], COUNTA('Sheet1'[Call Id]))
Two new columns are also created:
- Hour : To get the hourly number of calls
- AvgTalkDuration(sec): To get the time average talk duration in seconds 

## Insights
- Average customer satisfaction rating: **3.40**
- Average Speed of Answering          : **67.52 Sec**
- Conversion rate- assign to resolve  : **73%**
- **Agents got least calls at 18th hour**
- **Dane is best performing agent**

![Pwc call center](https://user-images.githubusercontent.com/53168269/213384177-25f248fe-d6b0-4712-98c3-c1944f9a8971.JPG)
