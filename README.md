# TRAFFIC CRASH 
## Introduction
This dataset contains information about traffic crashes that took place in Chicago, IL from year 2015 to 2023. There are Categorical (CAT) and Numerical (NUM) variables in the dataset. 
Variables contain information like the crash date, crash time, type of the crash, at what posted speed limit crash happened, what was the weather condition when crash occured, primary cause of accident, damage amount, roadway surface condition, lighting condition of roads, etc.
There are 769409 rows and 49 columns in the dataset. The various variables (49 features) of the dataset are:
•	CRASH_RECORD_ID: This is a unique id of a dataset that indicates traffic crash. (Alphanumeric)
•	CRASH_DATE_EST_I: Crash date estimated by officer or reporting authority. (CAT)
•	CRASH_DATE: This represents the day on which an accident takes place. (Date time)
•	POSTED_SPEED_LIMIT: This represents a posted speed limit of the area in which an accident happens. (NUM)
•	TRAFFIC_CONTROL_DEVICE: Traffic control devices present at the location where the crash happened. (CAT)
•	DEVICE_CONDITION: Condition of traffic control device, as determined by reporting officer. (CAT)
•	WEATHER_CONDITION: Condition of weather when crash happened like, rainfall, snowfall, etc. (CAT)
•	LIGHTING_CONDITION: Road light condition at the time of crash (Day or nighttime) (CAT)
•	FIRST_CRASH_TYPE: Type of first collision in traffic crash (CAT)
•	TRAFFICWAY_TYPE: Type of traffic way where crash happened. (CAT)
•	LANE_CNT: Total number of lanes in either direction excluding turn lane. (NUM)
•	ALIGNMENT: Street alignment at the location of crash. (Text)
•	ROADWAY_SURFACE_COND: Road surface condition at the time of accident. (Text)
•	ROAD_DEFECT: Road defects as determined by the reporting officer. (Text)
•	REPORT_TYPE: Administrative report type at scene. (Text)
•	CRASH_TYPE: A general severity classification for the crash. Can be either Injury and/or Tow Due to Crash or No Injury / Drive Away. (CAT)
•	INTERSECTION_RELATED_I: Whether an intersection contributed to the collision. Does not indicate if the collision happened inside the intersection. (CAT)
•	NOT_RIGHT_OF_WAY_I: Whether the initial crash happened outside of the public right-of-way. (Categorical Yes or No)
•	HIT_AND_RUN_I: Did or did not a driver cause the crash and then leave the site without exchanging information or helping? (CAT)
•	DAMAGE: Estimated Vehicle Damage during accident (in $). (NUM)
•	DATE_POLICE_NOTIFIED: Date when police were notified of accident. (Date)
•	PRIM_CONTRIBUTORY_CAUSE: Primary Contributory cause in causing the crash. (Text)
•	SEC_CONTRIBUTORY_CAUSE: Secondary Contributory cause in causing the crash. (Text)
•	STREET_NO: Street address number of crash location. (NUM)
•	STREET_DIRECTION: Street address direction (North, South, East, West) (Text)
•	STREET_NAME: Street address Name where crash happened. (Text)
•	BEAT_OF_OCCURRENCE: Chicago Police Department Beat ID. (NUM- ID)
•	PHOTOS_TAKEN_I: Whether photos were taken at crash location? (CAT)
•	STATEMENTS_TAKEN_I: Whether statement were taken at crash location? (CAT)
•	DOORING_I: Whether a car occupant's opening of a door into a bicyclist's route resulted in the crash. (Categorical)
•	WORK_ZONE_I: Whether the accident took place in a work zone area (Categorical)
•	WORK_ZONE_TYPE: The type of work zone where an accident happened. (Text)
•	WORKERS_PRESENT_I: Whether there were construction workers at the scene of the crash? (Categorical Yes or No.)
•	NUM_UNITS: Number of units involved in the crash. (Numerical)
•	MOST_SEVERE_INJURY: Most severe injury sustained by any person involved in the crash. (CAT)
•	INJURIES_TOTAL: Total persons sustaining injuries. (NUM)
•	INJURIES_FATAL: Total persons sustaining fatal injuries in the crash. (NUM)
•	INJURIES_INCAPACITATING: Total persons sustaining incapacitating/serious injuries in the crash. (NUM)
•	INJURIES_NON_INCAPACITATING: Total persons sustaining non-incapacitating injuries in the crash. (NUM)
•	INJURIES_REPORTED_NOT_EVIDENT: Total persons sustaining possible injuries in the crash that are not evident. (NUM)
•	INJURIES_NO_INDICATION: Total persons sustaining no injuries in the crash. (NUM)
•	INJURIES_UNKNOWN: Injuries undefined in the crash. (NUM)
•	CRASH_HOUR: The CRASH_DATE component's hour of the day. (Integer)
•	CRASH_DAY_OF_WEEK: The CRASH_DATE component's day of the week. (Integer)
•	CRASH_MONTH: The month component of CRASH_DATE. (Integer)
•	LATITUDE: The latitude of the crash location. (Numeric Location)
•	LONGITUDE: The longitude of the crash location. (Numeric Location)
•	LOCATION: The crash location, as determined by police/ reporting officer. (Point)

## My research questions are:
• In which month of the year do most accidents happen?
• On what day of the week most traffic crashes happen and at what time?
• Does weather condition play an important role in traffic crashes.
• What were the main causes of the accident that took place in the intersection?
• What factors are important in deciding if a traffic crash would result in high, medium, or low damage.
• What factors lead to serious injury/ tow due to crash?
• Does posted speed limit play a role in the crashes?

## DATA ANALYSIS
There was a strong correlation between injuries total & injuries non incapacitating and injuries total & injuries reported not evident. Rest in the other variables there was no correlation.
Using correlation, we have found that there is a strong correlation between very few variables with 0.76 and value 0.57 maximum. Below heat map shows a correlation between variables mentioned above. 
 ![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/9874f6e3-7b3b-46be-a529-cf2212faf7fa)

After visualizing the data, I have kept 11 variables that are related to our research question.
Variables such as 'POSTED_SPEED_LIMIT', 'WEATHER_CONDITION', 'ROAD_LIGHTING_CONDITION', 'ROADWAY_SURFACE_CONDITION', 'ROAD_DEFECT', 'CRASH_TYPE', 'INTERSECTION_RELATED_I', 'DAMAGE', 'CRASH_DAY_OF_WEEK', 'CRASH_MONTH', 'CRASH_HOUR'.
I found most of the traffic crashes that took place in Chicago have data of accidents that have no injury and drive away.
  ![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/b66cf3d7-096c-4e3e-b765-9e77aba0c909)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/1fe9f125-9b66-4953-bceb-1261667e9693)

Variables Damage tells us the amount of damage that happened to a car after a crash, we can find that many accidents resulted in high damage over $1500 and very few resulted in low damage of $500 or less. 
In my analysis, DAMAGE is the output variable whereas all others are predictor variables.
   ![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/0b8a2abf-2c75-4a80-9ed3-82138d873f85)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/96382e20-3622-4f14-ae0c-6c122d157467)

Data shows that most of the accident crashes took place in clear weather and comparatively very less during rain and snow weather conditions and roadway surface is related to it. 
Roadway surface condition variable tells that many accidents crash happened on dry surface road and few crashes happened due to wet, or snow surface. There were no defects in the roads where the accident happened while some were unknown. I later dropped roadway surface condition and road defect variable because most of the data was of DRY roadway surface condition and road defect as no defects, so the road conditions have not played any role in the accident.
 ![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/f643908c-7e83-4043-af61-89223f7cad3f)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/d44e8c1f-4570-4114-bc7b-969cc9404ea4)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/a563b223-8a59-4343-b238-d1b369d05fc9)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/ba1ecf6f-353e-46a5-b09b-9aad22d2c362)


The above plots show that most of the accidents take place on Friday (6) and Saturday (7) between 3 to 5PM. The data shows that the accident crash cases gradually increase in the month of May (5) and are at peak in October and after October accident crash decreases. Which means most accidents happen during summer and fall.
Variable INTERSECTION_RELATED_I, tell whether accident crash happened is related to intersection. The above chart shows only 20% of accidents happened near an intersection. 
There were some outliers in POSTED_SPEED_LIMIT and INJURIES_TOTAL variables. So, we removed speed limit values above 70 and below 15mph as we know in general, US minimum speed limit is 15 and max 70mph in Illinois. After removing outliers, we see that most of the crashes happened at the 30-speed limit area and few at 15, 20, 25, and 35mph. 
     ![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/162e2c47-e25f-43fa-b1d5-979c58492b37)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/0baa4f9c-4437-416b-824e-b6e06f764f78)
Similarly, Injuries_Total variable has an outlier, so I only kept values below 5 because in an accident not more than 5 person can get injured and in dataset most of the crashes took place had only 1 or 2 person injured. Data shows that in an accident a maximum of 1 or 2 people are injured in a traffic crash.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/268ae263-c0e5-4475-ba1d-d364b9c5c00f)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/856cce7d-fad5-494b-b43f-62413fc669fa)

Below graphs clearly show the analysis to answer the question: What was the main cause of the injury that took place near the intersection? 
   ![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/69c2e6d1-e356-4f03-a1b0-75d117bce834)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/6de05317-36ea-4379-bbd9-28704bc82c2e)

I have used variable INTERSECTION_RELATED_I which shows only 20% of accidents happened near an intersection. But during rainy weather most of the accidents happened in or near intersections. So, weather conditions play a major role in accidents near intersections.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/4ab4dc7a-ce6a-4f0a-b542-7edff9824785)

To answer the question: What factors are important in deciding if a traffic crash would result in high, medium or low damage.
I have visualized each variables against damage. Factors like weather condition, crash type, lighting conditions and intersection relation accidents result in high damage of over $1500.
    
During weather conditions = snow, most of the traffic crashes happen during office hours. Below crash hour plot shows peak accident at 8AM and 5PM. During January and Febraury most of the accident happened due to snowfall.
    

### Outcome of EDA

Most of the traffic crashes took place at 30mph and comparatively very few accidents happened at the 20,25 and 35 mph speed limit. In EDA, it was found that many accidents take place in clear weather and very few in rain, snow, and cloudy weather. This may be because data contains very little information on rain, snow, and cloudy weather. It was found that in rainy weather 34.3% got injured whereas in CLEAR weather only 26.6% got injured/tow due to crash. During weather conditions such as rain, cloudy and snow, most of the traffic crash resulted in medium and high damage. There was no damage below $500 in cloudy and snowy weather. 
Most of the crashes happened on dry surfaces followed by wet, unknown, and snowy surfaces. This variable is somewhat related to weather conditions, based on the weather conditions, the surface of roads changes. Due to which this categorical variable is not used in input while building model.
I have renamed Lighting_Condition variable from lighting condition to Road_lighting_condition because they are talking about natural lighting condition of road instead of vehicle lighting. The data shows most of accident happened during daylight followed by darkness, lighted road condition and very few at Dusk, dawn and darkness.
Injuries_Total variable contained outliers which were removed during data analysis and kept only injuries total below 5 because in each traffic crash maximum of 1 or 2 people were injured. Most of the data is of total 0 injuries.
Data shows that in most of the traffic crash people were not injured/and they simply drive away and only 40% were injured/and towed due to crash.
It was found that most of the traffic crashes resulted in Damage of Over $1500 followed by $501-$1500 and $500 or less. It was found that when damage was Over $1500, 35.7% of people got injured and were towed due to crash but when damage was less than equal to $500, only 19.7% got injured.
The primary contributory cause of traffic crashes tells that most accidents happened was due to failing to yield right-of-way, followed by following too closely, improper overtaking and failing to reduce speed to avoid crash. It was found that only 18.4% got injured and towed due to crash when they were following too closely but 39.6% got injured when they failed to yield right-of-way.
It was analyzed that most of the traffic crashes took place on Friday (6) and Saturday (7) between 3 to 5PM. The data shows that the accident crash cases gradually increase in the month of May (5) and are at peak in October and after October accident crash decreases. Which means most accidents happen during summer and fall. Using visualization, it was found that in Chicago many accidents occurred due to snow were peak at office hours i.e., at 8 am & 5 pm. 

## 1. In which month of the year do most accidents happen?
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/0d34694d-a1c3-4915-a0dc-022e94264068)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/ef7b0d6d-f859-4993-a521-440d675f5103)

## 2. On what day of the week most traffic crashes happen and at what time?
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/23c7af70-80ff-40a9-a9c1-be42b965fb0e)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/0571b9ce-75fa-447c-8f36-0e5ff7756304)

![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/e74889ce-784f-45d5-9a6a-dca394cec4d9)

## 3. Does weather condition play an important role in traffic crashes.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/d2eb5007-7931-4cc7-99d1-6efbf18b93db)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/8b3f95c3-c85b-4f84-ae6b-c838cc84f961)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/83993208-b66a-4464-8ed9-1ae079106115)

![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/2d162cf7-9fcd-4448-bad9-6b9742943e71)

## 4. What were the main causes of the accident that took place in the intersection?
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/021f8c14-9989-43bb-94fe-2d12eabe2ad9)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/04f18ebe-c9be-4516-a8da-88994b39edb2)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/cf7199d4-3c09-4c85-a74b-10db2a7374ee)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/3fdd8ebe-08f9-4ab7-a8eb-3bee8df42de8)
Failing to yield and rain were higher contributor to intersection related injuries when compared to snow weather condition and following too closely
My initial assumption was that following too closely might play a major role in intersection related injuries but failing to yield ended up being the biggest contributor.

## 5. What factors are important in deciding if a traffic crash would result in high, medium, or low damage.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/7093983b-87c9-417d-9b5a-18227bd88bed)
  The ratio of high damage when compared to medium and low damage is higher in darkness, lighted road when compared to day light.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/da0a585c-a27c-44a2-97c3-2bf4140d1dcf)
  The ratio of high damage when compared to medium and low damage is higher in intersection related crashes.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/2513f320-bdc9-4bc4-9554-6bc9ae149bd9)
  The ratio of high damage when compared to medium and low damage is higher in cases where injury and tow due to crash happen.

## 6. What factors lead to serious injury/ tow due to crash?
Failing to yield right-of-way was major contributor that led to serious injuries/tow due to crash when compared to following too closely.
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/8f9ca8cc-bd9f-4927-b621-93a147f15ba2)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/80a24f5c-840b-43b9-87de-5dabe62981d7)

## 7. Does posted speed limit play a role in the crashes.
Most of the accidents happened in the area where the posted speed limit was 30.
This suggests that very less accidents happened on the highways where posted speed limit is higher
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/043bdb94-da18-4985-8792-5af04b9c5263)


## Model Development
Objective: Using predictive model (K-NN) we will predict based on different features, traffic crash will result in how much damage (high, medium, or low)
Converted categorical input variables into dummy variables. 
In model building, DAMAGE is kept as an output variable which is dependent on other numerical and dummy variables. I have considered damage over $1500 as high damage, between $500 to $1500 as medium damage and damage $500 or less as low damage but have not renamed it. 
I have divided dataset into test and train dataset in the ratio of 0.7:0.3. 
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/7a921cda-ff4f-4585-9e12-3cc48ba73384)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/c7ce6d3d-28af-4b91-a169-8f462943d5b7)

![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/c3aa60f8-832a-4af1-b2b7-28c0d1549f91)
![image](https://github.com/deepshisachan25/Python--Traffic-Crashes/assets/170371796/33f5d4ee-0b84-4311-8456-3e76e757f63c)
With K=10, the model gives the highest accuracy of 58% approximately.

### Learning
While building the model, I found KNN model will be the best model as outcome variable is categorical and KNN finds closest training set data that matches the new data which needs to be forecast.
Using K-NN model, I have built a classification model where DAMAGE was the output variable, and it is able to predict whether a traffic crash would result in high, medium or low damage. With K=10, the model gives the highest accuracy of 58% which means model will be able to accurately predict the new data that traffic crash will result in high, medium or low damage.

 


