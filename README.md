# Marketing_Ab_Testing
Analyzing the impact of marketing campaigns using A/B testing to optimize conversions.



# Evaluating the Impact of Marketing Campaigns using A/B Testing

**Author:** Keho Olamide  
**Date:** June 2025

---

## Problem

In today’s digital marketplace, businesses often struggle to determine whether marketing campaigns actually drive conversions. Launching campaigns without testing can lead to wasted budget, poor ROI, and missed opportunities for optimization.  

The challenge is **quantifying the effectiveness of marketing strategies** and identifying actionable insights for future campaigns.

---

## Solution

We addressed this problem by implementing **A/B testing**, a randomized experimentation method, to evaluate the impact of an advertising campaign. Using historical user-level data, we:

- Compared conversion rates between users exposed to ads and a control group (PSA or no ad).  
- Applied statistical tests to determine if differences in conversion were significant.  
- Analyzed user engagement patterns to identify optimal ad timing and placement.  

The analysis revealed that the ad campaign **significantly increased conversions** and provided insights for optimizing future campaigns.

---

## Dataset Overview

The dataset contains **588,101 user-level records** with the following features:

- `user_id`: Unique user identifier  
- `test_group`: Indicates whether the user saw ads ("ad") or PSA ("psa")  
- `converted`: Boolean indicating purchase  
- `total_ads`: Number of ads seen  
- `most_ads_day`: Day of the week the user saw the most ads  
- `most_ads_hour`: Hour of the day the user saw the most ads  

---

## Exploratory Data Analysis (EDA)

### Conversion Summary by Group

| Test Group | Total Users | Conversions | Conversion Rate |
|------------|------------|-------------|----------------|
| **Ad**    | 564,577    | 14,423      | 2.55%          |
| **PSA**   | 23,524     | 420         | 1.79%          |

**Observations:**

- The **Ad group** had a higher conversion rate than the PSA group.  
- More users were assigned to the Ad group, which is typical for A/B experiments to maximize learning about the treatment.

### Visualizations

---

### Conversion Rate by Test Group

![Conversion Rate by Test Group](https://github.com/Stellabigeal/Marketing_Ab_Testing/blob/main/Conversion_Rates_by_Test_Group.png)

- This plot compares the conversion rates between the two experimental groups: **"ad"** and **"psa"**.
- It visually confirms that users who saw ads were more likely to convert.

---


### Conversion Rate by Day User Saw Most Ads
![Conversion Rate by Day](https://raw.githubusercontent.com/Stellabigeal/Marketing_Ab_Testing/480dd89adc259335e8d2195a7efc99dabc55273d/Conversion_Rates_by_Most_Ads.jpg)


- **Day with Highest Conversion Rate:** Monday (0.0328)  
- **Day with Lowest Conversion Rate:** Saturday (0.0211)  
- This plot reveals which days of the week users were shown the most ads and whether they converted.
- Higher conversion rates from **Monday–Wednesday** suggest people respond better during structured weekday routines.
- Lower conversions on **Saturday** may indicate less attention toward purchases during weekends.
- **Recommendation:** Focus ad delivery on high-performing weekdays and reduce budget spend on low-converting days.

---


## Inferential Statistics: Hypothesis Testing

**Hypotheses:**

- **H0 (Null):** Conversion rates are equal for ad and PSA groups  
- **H1 (Alternative):** Conversion rate for the ad group is higher than the PSA group  

**Method:** Two-proportion Z-test comparing conversion rates between groups  

**Results:**

- **Z-statistic:** ~10.72  
- **p-value:** < 0.0001  

**Conclusion:**  
The p-value is far below 0.05. **We reject the null hypothesis**, confirming that the ad group had significantly higher conversions than the PSA group.

---

## Key Insights

- **Ad Effectiveness:** The advertising campaign significantly improved conversion rates.  
- **User Engagement Patterns:** Most users saw the highest number of ads on specific days and hours, indicating optimal times for ad placement.  

---

## Recommendations

1. Scale up ad campaigns during peak engagement times identified in the data.  
2. Conduct additional A/B tests to evaluate other creative formats, platforms, or audience segments.  
3. Optimize ad budget allocation for higher ROI based on user engagement patterns.

---

## Appendix

- Full Python code used for analysis  
- Conversion summary table (CSV)  
- Charts and visualizations (insert your figures here)
