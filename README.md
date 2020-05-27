# UDA_city_Project2

# Investigate a Dataset: No Show Appointments 

## Introduction

This dataset collects information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. A number of characteristics about the patient are included in each row.

● ‘ScheduledDay’ tells us on what day the patient set up their appointment. \
● ‘Neighborhood’ indicates the location of the hospital. \
● ‘Scholarship’ indicates whether or not the patient is enrolled in Brasilian welfare program Bolsa Família. \
● ‘No_show’ it says ‘No’ if the patient showed up to their appointment, and ‘Yes’ if they did not show up.

## Question framed for investigation:
Q1: What was the overall appointment who showed and never showed up?\
Q2: How gender proportion impacting for showing /not showing up for appointment?\
Q3: How age of patient impacting for showing/not showing up appointment? More Senior or Adult?\
Q4: Does more awaiting days leading for appointment to never showed up and on which day?\
Q5: Wat was top 15 neighbourhood who showed up and never showed up?\
Q6: How does medical condition and enrolling in scholarship, and sms improved in showing up appointments?\

## Observation before data cleaning:

1. Data set consists of 110527 values and 14 features.\
2. No missing and duplicated value for data.\
3. Age ranges from -1 to 115, need to clean further. \
4. Values for "Age", "Scholarship", "Hipertension", "Diabetes", "Alcoholism","SMS_received" has values of 0 and 1.\
5. Feature "Handcap" has value from 0 to 4.\
6. "AppointmentID" holds all unique values dont hold much important feature for futher analysis and can be dropped.\
7. "Patiend ID" holds approprimately 44% of duplicated values.\
8. Values for "ScheduledDay" and "AppointmentDay" are dates with dtype as object, need to coverted into datatime.\
9. 'AppointmentDay' has 27 unique values and where as ScheduledDay has 103549.\
10. 'AppointmentDay' ranges from april to june for year 2016.\
11. Values for "Neighbourhood", "Gender" and "No-show" has dtype as strings.\
12. Many typo and spelling mistake for columns.
