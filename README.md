# Mobile Device Usage and User Behavior Analysis

## **Supported Tools**

- **Python** with libraries such as Pandas, Matplotlib, and Seaborn for data processing and visualization.

## **Step 1: Univariate Analysis**

### Descriptive Statistics

The dataset consists of 700 samples. The analysis covers 8 variables used in the study.
![image](https://github.com/user-attachments/assets/e2c8be8b-1304-4749-a1e6-03fec3e9cd19)

- **App Usage Time (min/day)**: On average, users spend 271.13 minutes per day on apps, with a large dispersion ranging from 30 to 598 minutes. Most users use apps between 113.25 to 434.25 minutes per day.
- **Screen On Time (hours/day)**: The average screen-on time is 5.27 hours per day, with a range from 1 hour to 12 hours. Most users have screen-on time between 2.5 to 7.4 hours per day.
- **Battery Drain (mAh/day)**: On average, users consume 1525.16 mAh of battery per day, with a range from 302 mAh to 2993 mAh. Most users consume between 722.25 mAh and 2229.5 mAh daily.
- **Number of Apps Installed**: The average number of installed apps is 50.68, with a range from 10 to 99. Most users have between 26 to 74 apps installed.
- **Data Usage (MB/day)**: On average, users consume 929.74 MB of data daily, with a range from 102 MB to 2497 MB. Most users use between 373 MB to 1341 MB of data daily.
- **Age**: The average age of users is 38.48 years, with a range from 18 to 59 years. Most users fall within the age range of 28 to 49.
- **User Behavior Class**: The average user behavior class is 2.99, with a range from 1 to 5. More information is needed on the classification system to better understand this average.

### Distribution & Box Plot

The distribution of the variables was reviewed, and box plots were used to identify outliers.

---

## **Step 2: Multivariate Analysis**

### Correlation Matrix
![image](https://github.com/user-attachments/assets/67ff04c4-b539-4ee9-b71d-54bda4a3302c)

The variables related to app usage time, screen-on time, battery drain, number of apps installed, and data usage show strong correlation with each other, indicating a near-linear relationship. As one variable increases, the others tend to increase as well.

### Pairwise Variable Analysis

- **Age Group Analysis**: The analysis divides users into different age groups such as Gen Z, Millennials, Gen X, and Baby Boomers to better understand usage behavior based on age.
    ![image](https://github.com/user-attachments/assets/9f7ed38b-3d24-448d-b143-257058c794dd)
- **Screen On Time vs. App Usage Time by Age Group**
  ![image](https://github.com/user-attachments/assets/a0e6babf-6e11-400d-87ad-44e14682dfd3)
- **Data Usage by Gender and Age**
  ![image](https://github.com/user-attachments/assets/7da1499f-02da-4a41-9542-5700c2457d4a)
- **Number of Apps Installed by Gender and Age**
  ![image](https://github.com/user-attachments/assets/b61ee75e-02c1-4ad8-a567-28c71bdd00df)
- **Battery Drain by Device and OS**

![image](https://github.com/user-attachments/assets/50340db4-2959-419c-8ecd-04af91314a1f)

---

## **Step 3: Hypothesis Testing**

### Hypothesis 1: "The average app usage time between males and females is the same."

- **Null Hypothesis (H0)**: μ_Male(App Usage Time) = μ_Female(App Usage Time)
- **Alternative Hypothesis (H1)**: μ_Male(App Usage Time) ≠ μ_Female(App Usage Time)

**T-statistic**: -0.12

**P-value**: 0.90

The p-value is greater than α (0.90 > 0.05), so we fail to reject the null hypothesis. Therefore, the average app usage time is similar between males and females.

![image](https://github.com/user-attachments/assets/c56f7e69-e335-47cf-ac12-735f841fca9c)

### Hypothesis 2: "The average app usage time differs by age group."

- **Null Hypothesis (H0)**: μ_18-24 = μ_25-34 = μ_35-44 = μ_45-54 = μ_55+
- **Alternative Hypothesis (H1)**: At least one μ differs.

**F-statistic**: 1.42

**P-value**: 0.23

The p-value (0.23) is greater than α (0.05), so we fail to reject the null hypothesis. There is no significant difference in app usage time across age groups.

![image](https://github.com/user-attachments/assets/aa43100d-b99e-4a59-8f22-20a62b6bd30f)

### Hypothesis 3: "The daily screen-on time of Gen Z is not less than 5 hours per day."

- **Null Hypothesis (H0)**: μ_18-24(Screen On Time) ≥ 5
- **Alternative Hypothesis (H1)**: μ_18-24(Screen On Time) < 5

**T-statistic**: 1.77

**P-value**: 0.96

With a p-value of 0.96 (greater than α = 0.05),fail to reject the null hypothesis. Gen Z's average screen-on time is not less than 5 hours per day.
![image](https://github.com/user-attachments/assets/54c8f269-3295-4a39-be5a-948e7e08b0cd)

- The distribution graph of screen usage time for Gen Z reveals a concerning reality: on average, a Gen Z youth spends over 5 hours a day interacting with their phone. This figure far exceeds the recommendations of health experts. Excessive screen usage is associated with health concerns, such as impaired vision, sleep disturbances, and psychological issues. To address this, schools, families, and governments need to collaborate to educate young people on healthy technology usage, while also creating environments that encourage outdoor activities and direct social interactions.
### Hypothesis 4: "The daily screen-on time of Baby Boomers is no more than 3 hours per day."

- **Null Hypothesis (H0)**: μ_55+(Screen On Time) ≤ 3
- **Alternative Hypothesis (H1)**: μ_55+(Screen On Time) > 3

**T-statistic**: 5.35

**P-value**: 7.32e-07

Since the p-value is very low, reject the null hypothesis and conclude that the daily screen-on time of Baby Boomers is more than 3 hours per day.

![image](https://github.com/user-attachments/assets/082480cd-5ba4-40b2-8b24-51d8d8d40a4d)

- The distribution graph of screen usage time for the Baby Boomer generation shows that older adults spend about 2-4 hours per day interacting with smartphones. While this is not as common as among younger generations, older adults are increasingly spending more time using smartphones. The graph has a right-skewed shape, meaning that a few individuals use screens for many hours a day, stretching the tail to the right. Most of the data is concentrated on the left side, indicating that the majority of Baby Boomers use screens for relatively short periods. The right-skewed shape also suggests an uneven distribution, with some older adults using screens very frequently. This reflects the Baby Boomer generation's adaptation to technology and their need to connect with family and friends, gather information, and seek entertainment. However, excessive screen usage raises concerns about its impact on health and quality of life for older adults, particularly regarding sleep and eye issues.
---

## **Limitations**

- This study primarily focuses on technical and behavioral variables such as app usage time, screen-on time, battery drain, and data usage. It lacks direct indicators related to health. Therefore, a more in-depth analysis of the health impacts of mobile device usage cannot be performed with the current dataset.

## **Future Improvements**

To enhance the analysis, future research could consider adding the following variables to the dataset:

- **Sleep Quality and Duration**: Average sleep hours per day and sleep disturbances.
- **Eye Health**: Frequency of eye strain, dryness, or need for corrective eyewear.
- **Psychological Effects**: Anxiety levels or dependence on mobile devices.
- **Environmental Factors**: Usage of mobile devices in low-light settings or screen brightness.
- **Biometric Data**: Heart rate, calories burned while using devices for extended periods.
