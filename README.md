# UDA_city_Project2

# Investigate a Dataset: No Show Appointments 

## Introduction

This dataset collects information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. A number of characteristics about the patient are included in each row.

● ‘ScheduledDay’ tells us on what day the patient set up their appointment. \
● ‘Neighborhood’ indicates the location of the hospital. \
● ‘Scholarship’ indicates whether or not the patient is enrolled in Brasilian welfare program Bolsa Família. \
● ‘No_show’ it says ‘No’ if the patient showed up to their appointment, and ‘Yes’ if they did not show up.

## Question framed for investigation
Q1: What was the overall appointment who showed and never showed up?\
Q2: How gender proportion impacting for showing /not showing up for appointment?\
Q3: How age of patient impacting for showing/not showing up appointment? More Senior or Adult?\
Q4: Does more awaiting days leading for appointment to never showed up and on which day?\
Q5: Wat was top 15 neighbourhood who showed up and never showed up?\
Q6: How does medical condition and enrolling in scholarship, and sms improved in showing up appointments?\

## Observation before data cleaning

1. Data set consists of 110527 values and 14 features.
2. No missing and duplicated value for data.
3. Age ranges from -1 to 115, need to clean further. 
4. Values for "Age", "Scholarship", "Hipertension", "Diabetes", "Alcoholism","SMS_received" has values of 0 and 1.
5. Feature "Handcap" has value from 0 to 4.
6. "AppointmentID" holds all unique values dont hold much important feature for futher analysis and can be dropped.
7. "Patiend ID" holds approprimately 44% of duplicated values.
8. Values for "ScheduledDay" and "AppointmentDay" are dates with dtype as object, need to coverted into datatime.
9. 'AppointmentDay' has 27 unique values and where as ScheduledDay has 103549.
10. 'AppointmentDay' ranges from april to june for year 2016.
11. Values for "Neighbourhood", "Gender" and "No-show" has dtype as strings.
12. Many typo and spelling mistake for columns.

## Data Cleaning

### Steps taken for data cleaning:
1. Fixing columns for typo, inconsistendcy and spelling mistakes.
2. Fixing dtype for columns scheduledday' and 'appointmentday to datetime and created new feature-'Awaiting days'.
3. Treatment of outlier for Awaiting days.
4. Created new feature by extraction 'weekday'.
5. Treatment of outlier for age.
6. Dropping features which are unique and least important.

## Exploratory Data Analysis

Question 1 : What is the overall appointment who showed and never showed up?
1. Majority of appointment are showed up by 80% when compared to are never showed up by 20%,
2. If it would be for machine learning, then this target variable can create imbalance problem.

Question 2 : How gender proportion impacting for showing /not showing up for appointment?
1. Not much difference can be seen between gender who showed up or never showed.
2. Female proportion almost same for appointment showed up i.e 64.86 and never showed i.e 65.3.
3. Male proportion are also almost same for appointment showed up i.e 35.14 and never showed i.e 34.7.
4. In context of proportion for gender, Female are majorly higher than man for showing up and never showing up as well.

Question 3 : How age of patient impacting for showing/not showing up appointment? More Senior or Adult?
1. Patient with more age is most likely to show up appointment.
2. Mean age for female is greater than Male age in both showed up and never showed up.
3. Female with more age are most likely to show up appointment when compared with whom never showed up.
4. Male with less age are most likely to never show up appointment when compared with whom showed up appointment.
5. Age can be important feature in predicting for appointment showing up and not showing due to patient with more age are most likely to be showing up appointment.

