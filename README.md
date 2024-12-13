PWC Power BI Virtual work experience- Call Center Trends
 image

Table of Contents

    Problem Statement

    Data source

    Data Preparation

    Data Modelling

    Data Analysis

    Data Visualization Dashboard

    Insights

Problem Statement

    Track Customer Satisfaction – Visualize overall satisfaction levels for improvement.

    Analyze Call Efficiency – Monitor calls answered vs. abandoned and average speed of answer (ASA).

    Identify Call Volume Trends – Show call patterns by time (hour, day, week) for resource optimization.

    Evaluate Agent Performance – Use a quadrant chart (average handle time vs. calls answered) to assess agents.

    Enhance Decision-Making – Provide actionable insights via interactive visualizations for better service and operations.

Data source

Dataset used for this task was presented by PWC and call center trends dataset:

The Call Center Trends dataset has been transformed and loaded into Microsoft Power BI Desktop for modeling.

The dataset contains 10 columns and 5,000 rows of observations.

Dataset:

Data Preparation

The data cleaning process in Power Query Editor included the following steps:

    Removed irrelevant columns.

    Eliminated unnecessary rows.

    Verified and ensured correct data types for all columns.

Data Analysis

And then dataset was cleaned and transformed, it was ready to the data modeled.

The dataset includes several new measures for in-depth analysis:

Total Calls – The total number of calls received.

Total Resolved Calls – The number of calls that were successfully resolved.

Unresolved Calls – The number of calls that remain unresolved.

Average Talk Duration – The average duration of conversations during calls.

Average Satisfaction – The average customer satisfaction score across calls.

Average Speed of Answer – The average time taken to answer calls.

These measures are designed to provide detailed insights into call center performance and agent efficiency.

Data analysis(DAX):

answered call = COUNTX(FILTER('Call Center trends','Call Center trends'[Answered (Y/N)] = "Y"), 'Call Center trends'[Answered (Y/N)])

Average Satisfaction Rating = AVERAGE('Call Center trends'[Satisfaction rating])

Average Speed of Answer = AVERAGE('Call Center trends'[Speed of answer in seconds])

Total Calls = COUNTROWS('Call Center trends')

Total Resolved Calls = COUNTROWS(FILTER('Call Center trends',TRIM('Call Center trends'[Resolved]) = "Y"))

Unanswered Calls = COUNTROWS(FILTER('Call Center trends',TRIM('Call Center trends'[Answered (Y/N)]) = "N"))

Unresolved Calls = COUNTROWS(FILTER('Call Center trends', 'Call Center trends'[Resolved] = "N"))

Data Visualization (Dashboard) :

Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:

Dashboard:

Shows visualizations from Call Center Trends :

image

Insights

1.The dashboard provides several key insights into the call center trends:

Total Calls: 5,000 calls were received, with 4,054 calls answered and 946 calls answered by agents.

2.Agent Performance:

Jim resolved the highest number of calls (666), followed by Martha (638) and Dan (633).

Martha also had the fastest response time, with an average speed of answer of 36 seconds, while Stewart had the slowest, at 32 seconds.

3.Topic Analysis:

The highest number of calls were related to Streaming (1.02K calls, 20.44%), followed by Technical Support (0.98K calls, 19.52%).

4.Satisfaction Ratings:

A large number of calls (1,218) were rated with a 3-star satisfaction, while 5-star ratings accounted for 843 calls.

5.Daily Call Resolution Trends:

Call resolution spikes occurred around Day 16, with 143 calls resolved. A general decline is visible towards the end of
