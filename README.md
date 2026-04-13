# Demographic & Socio-Economic Data Modelling
**The Impact of Time Poverty: A Quantitative Analysis of Demographic Determinants in Urban Populations**

![Data Analytics](https://img.shields.io/badge/Data%20Analytics-Econometrics-blue)
![STATA](https://img.shields.io/badge/STATA-Probit%20Modelling-1857C5)
![SPSS](https://img.shields.io/badge/SPSS-Data%20Consolidation-CC292B)

## The Commercial Context & Problem Statement
In modern societies, the traditional measurement of well-being has focused exclusively on income, ignoring a fundamental resource: time. In high-pressure labour environments (such as Chile, averaging 1,988 annual working hours versus the OECD average of 1,766), time scarcity diminishes productivity, learning, and overall well-being. 

The objective of this analysis and econometric model was to quantitatively identify the demographic and socio-economic characteristics of individuals most likely to suffer from "Time Poverty"—defined as the inability to allocate hours to rest or personal development due to high burdens of paid work, unpaid domestic labour, and commuting.

## Methodology & Data Strategy
The development of the predictive model followed a rigorous two-stage analytical approach:

* **Data Scale:** Modelling conducted on a representative urban sample of 9.5 million individuals (consolidating approximately 15,900 survey records).
* **Exploratory Data Analysis (EDA) & Theoretical Grounding:** Executed a comprehensive analysis of time-allocation structures prior to modelling. Leveraged advanced data visualisation (including dual-axis charts) and covariance matrices to map critical socio-demographic correlations—specifically isolating the structural overlap between education and socio-economic status—ensuring statistically robust feature selection.
* * **Feature Engineering & Data Cleansing:** Created the "Global Workload" metric, amalgamating hours of formal employment, unpaid domestic work, dependent care, and commuting times. Mitigated data volatility inherent in self-reported diaries by applying Tukey’s Method (1.5x IQR) to systematically identify and treat statistical outliers, ensuring robustness when establishing the Time Poverty thresholds.
* **Statistical Modelling:** Developed a binary response regression model (Probit) to isolate and measure the marginal effect of variables such as gender, age, education, household configuration (presence of infants/elderly), and income level on the probability of being time-poor.

To develop this predictive model, I led the analysis of the National Time Use Survey (ENUT 2015):
* **Data Scale:** Modelling conducted on a representative urban sample of 9.5 million individuals (consolidating approximately 15,900 survey records).
* **Feature Engineering:** Created the "Global Workload" metric, amalgamating hours of formal employment, unpaid domestic work, dependent care, and commuting times.
* **Statistical Modelling:** Developed a binary response regression model (Probit) to isolate and measure the marginal effect of variables such as gender, age, education, household configuration (presence of infants/elderly), and income level on the probability of being time-poor.

## 3. Key Findings & Data Insights
The econometric model yielded statistically significant findings with high commercial value for understanding human and urban behaviour:

* **The "Double Shift" Reality:** 12.84% of the urban population is time-poor during the working week. Women have a significantly higher probability of experiencing this condition (representing 65.19% of the total affected), driven by the asymmetrical burden of unpaid care work.
* **Income vs. Time Paradox:** Contrary to traditional perceptions, time poverty cuts across all socio-economic levels. In fact, higher levels of education and active labour market participation *increase* the probability of being time-poor on weekdays due to the intensity of working hours.
* **The Impact of Commuting & Care:** The inclusion of commuting times to the workplace drastically increases the marginal propensity for time scarcity. Furthermore, the presence of each infant (0-4 years) in the household increases the probability of being time-poor by 6.3% during the week, and up to 9.5% on weekends.

> *(Placeholder for Visual)*
> `![Time Poverty by Gender](link-to-your-image-1.png)`
> *Figure 1: Distribution of Global Workload and the Gender Gap.*

> *(Placeholder for Visual)*
> `![Marginal Effects](link-to-your-image-2.png)`
> *Figure 2: Marginal Effects of Demographic Variables on Time Poverty Probability.*

## 4. Technical Implementation Note
The original raw data consolidation and statistical modelling were executed using **STATA** and **SPSS**. While the legacy `.do` scripts are archived, the methodology strictly followed a Probit Regression approach, ensuring robust treatment of heteroscedasticity and categorical variables for large-scale demographic datasets.
