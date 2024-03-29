# Google-Data-Analysis-Portfolio
Showcase analysis I completed on Bellabeat dataset.
FitBit Smart Device Analysis
Welcome to the Bellabeat data analysis case study as a part of Google Data Analytics Specialization's capstone project.

Introduction

Urška Sršen and Sando Mur founded Bellabeat, a high-tech company that manufactures health-focused smart products. Collecting data on activity, sleep, stress, and reproductive health has allowed Bellabeat to empower women with knowledge about their own health and habits. Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women.

Scenario:

You are a junior data analyst working on the marketing analyst team at Bellabeat, a high-tech manufacturer of health-focused products for women. Bellabeat is a successful small company, but they have the potential to become a larger player in the global smart device market. Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart device fitness data could help unlock new growth opportunities for the company. You have been asked to focus on one of Bellabeat’s products and analyze smart device data to gain insight into how consumers are using their smart devices. The insights you discover will then help guide marketing strategy for the company. You will present your analysis to the Bellabeat executive team along with your high-level recommendations for Bellabeat’s marketing strategy.

Business Task
Sršen asks you to analyze smart device usage data in order to gain insight into how consumers use non-Bellabeat smart devices. She then wants you to select one Bellabeat product to apply these insights to in your presentation.

Following three points are the questions needed to be answered by this analysis.

What are some trends in smart device usage?
How could these trends apply to Bellabeat customers?
How could these trends help influence Bellabeat marketing strategy?
Prepare
To answer Bellabeat's business tasks I will be using FitBit Fitness Tracker Data: This Kaggle data set contains personal fitness tracker from thirty fitbit users. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. It includes information about daily activity, steps, and heart rate that can be used to explore users’ habits.

Considerations
Ssampling bias could be a issue. It was unclear how many participants wehre chosen. THey could obtain more data when participants become willing to share there data. The data is geared towards women, as Bellabeat is a ttech-driven wellness company for women only. Although the data does not provide that information. THe data is outdated from 2016. I used MySQL to help me process and analyze. For visulizations I used Excel. I only used 8 datasets to complete this task. 


Process

I merged hourIntensities, hourCalories, and hourSteps in excel query. I created hourActivites. I merged them on ID, and ActivityDate. I saved this as a CSV file, to import into MySQL. 


Analyze
TO analyze

--Show total for all activities.    
SELECT Id, ActivityDate, TotalSteps,
CAST(TotalDistance AS FLOAT) AS TotalDistance,
CAST(VeryActiveDistance AS FLOAT) AS VeryActiveDistance,
CAST(ModeratelyActiveDistance AS FLOAT) AS ModeratelyActiveDistance,
CAST(LightActiveDistance AS FLOAT) AS LightActiveDistance,
CAST(SedentaryActiveDistance AS FLOAT) AS SedentaryActiveDistance,
VeryActiveMinutes,
FairlyActiveMinutes,
LightlyActiveMinutes,
SedentaryMinutes,
Calories

FROM dailyactivity

[allactivity.csv](https://github.com/Leahb32/Google-Data-Analysis-Portfolio/files/11107911/allactivity.csv)
