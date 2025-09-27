# Pre-Roll Ad Gender Analysis

This project applies statistical modeling on 10,000 user sessions from a South Korean portal to examine gender-based differences in skippable pre-roll ad acceptance. Comparing linear probability, logistic, probit, and interval regression models, the study finds that men are more likely to complete (and skip later) drink, finance, and medicine ads, while women are more likely to complete health food and movie ads and skip later on male-oriented ads—offering strategies to improve ad acceptance.

---

## Project Motivation
Understanding gender-based differences in ad engagement can help marketers optimize pre-roll ad targeting and improve user experience across different ad categories.

---

## Data
- **Source:** pre-roll_ad.csv
- **Size:** 10,000 user sessions
- **Period:** July 1–28, 2019
- **Observations:** 10,000 users who were exposed to 15-second pre-roll skippable video ads on a South Korean popular online video content platform
- **Features:** Ad type, completion/skipping behavior, user demographics  
- **Preprocessing:** Data cleaned and categorized for modeling

## Variables
| Variable | Description |
|----------|-------------|
| `user_id` | Unique identifier for each user |
| `tt` | Hour of the day the ad was viewed |
| `age_new` | User age group (10-year intervals) |
| `media_platform` | Platform used to view the ad |
| `gender_new` | Gender of the user |
| `clip_duration` | Duration of video clips following ads (seconds) |
| `ad_brand_cat` | Ad brand category |
| `ad_complete` | Indicates whether the ad was watched in full |
| `gender_new:ad_brand_cat` | Interaction term to examine how ad category effect varies by gender |
| `l_ad_stop` | Lower limit of time interval when an ad was skipped (seconds) |
| `u_ad_stop` | Upper limit of time interval when an ad was skipped (seconds) |
| `genre_new` | Program genre preceding the ad |
| `day` | Day of the week the ad was viewed |

---

## Analysis Approach
1. Data cleaning and preprocessing  
2. Exploratory data analysis  
3. Model fitting: Linear Probability, Logistic, Probit, and Interval Regression  
4. Interpretation of gender-based differences across ad categories  

---

## Key Findings
- **Men:** More likely to complete and later skip drink, finance, and medicine ads  
- **Women:** More likely to complete health food and movie ads, and skip male-oriented ads  
- **Implication:** Tailoring ad targeting by gender and category can improve ad acceptance  

---

## Visualizations
Example plot of ad completion rates by gender:  
![Ad Completion Rates](images/ad_completion.png)  

---

## Key Methods & Tools
| Category | Details |
|----------|---------|
| Methods  | Linear Probability Model, Logistic & Probit Regression, Interval Regression |
| Tools    | RStudio (packages: dplyr, ggplot2, lmtest, margins) |

---

## How to Run
1. Clone the repository:  
```bash
git clone https://github.com/yourusername/pre-roll-ad-gender-analysis.git
