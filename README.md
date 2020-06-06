# UDA_city_Project-2

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

Question 4 :Does more awaiting days leading for appointment to never showed up and on which day?
1. As expected as number of awaiting days increase there are more cases are of not showing up appointment.
2. Monday has majority of appointment which never showed up and least on saturday and visa vera.
3. Average awaiting days for not showing up was almost twice the average awaiting days for showing up.
4. Awaiting days turn out to be important feature in predicting for appointment in showing up and for not showing up.

Question 5: Wat are top 15 neighbourhood who showed up and never showed up?
1. Not much difference between showed and not showed cases between neighbourhood.

Question 6: How does medical condition, enrolling in scholarship, and sms improved in showing up appointments?
1. Patients who didn't enrolled in scholorship has more show case i.e 72% when compared to those who are enrolled 7.5%.
2. Ratio for showed up to no showed scholorship is approximately 80%
3. The group who received a SMS reminder did not show up more often compared to those who did not receive a reminder.
4. The group not having received a reminder has a much smaller proportion of no shows.
5. Patient with medical condition like hypertension, diabetes and alcholism has showed up for appointment in less as compared with patient without any medical condion.
6. Proportion of never showed for all medical condition are approximately smilar for all with showed up case.
7. Handicap of value '0' have more showed up when compared to those no showed up and for other values.

## Conclusions
1. My analysis revealed that patients age and number of awaiting days for appointment could be an important feature in determining if patient is going to show up for appointment or not.

2. Futhere patient without any of the in the dataset stated diseases have higher no-show rates compared to those having a disease. Thereby it does not make much of a difference, which disease (hypertension, diabetes, alcoholism or handicap) the patient suffers.

3. Enrolling in scholorship has not much impact on predicting for possiblity if patient in going to turn up for show or not.

4. Lastly, and most surprisingly is the fact that for the appointments within this dataset a SMS-reminding the patients of their upcoming appointment made things worse.

## Limitations
1. It appears that the dataset is only based on 27 unique dates worth of data spread over April, May and June (27 unique dates in AppointmentDay) and therefore it doesn't provide a representative sample for predicting whether a patient is likely to not show up on a date outside of those 27 days. If the data was based on longer date range, then the conclusions drawn might have been different and the features in feature selection may also have been completely different.

2. Missing features which may have been useful to this analysis could be whether a patient in the past has been a no-show, or a patient's post-code, clinic distance from neighbourhood, or whether the patient is employed or unemployed or even the reason they scheduled an appointment.
