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

* **Data Scale:** Modelling conducted on a representative urban sample of **9.5 million** individuals (consolidating approximately **15,900** survey records).
* **Exploratory Data Analysis (EDA) & Theoretical Grounding:** Executed a comprehensive analysis of time-allocation structures prior to modelling. Leveraged advanced data visualisation (dual-axis charts) to identify critical socio-demographic correlations—specifically mapping the relationship between education levels and socio-economic status—to ensure a statistically sound selection of model predictors.


|  | Educational Attainment | Income Quintile |
| :---: | :---: | :---: |
| **Paid Work:** <br>Participation Rates & Avg. Hours | <img src="https://github.com/user-attachments/assets/28c57e0d-ed4b-4d39-a80a-9bb91566b517" width="400"> | <img src="https://github.com/user-attachments/assets/1294cc38-ad81-4b85-99ef-eb16fdcb591a" width="450"> |
| **Unpaid Work:** <br>Participation Rates & Avg. Hours | <img src="https://github.com/user-attachments/assets/4cc6a559-d799-430f-952d-5d20db85593b" width="400"> | <img src="https://github.com/user-attachments/assets/4cc6a559-d799-430f-952d-5d20db85593b" width="450"> |

* **Feature Engineering & Data Cleansing:** Created the "Global Workload" metric, amalgamating hours of formal employment, unpaid domestic work, dependent care, and commuting times. Mitigated data volatility inherent in self-reported diaries by applying Tukey’s Method (1.5x IQR) to systematically identify and treat statistical outliers, ensuring robustness when establishing the Time Poverty thresholds.

| Global Workload Distribution |
| :---: |
| <img src="https://github.com/user-attachments/assets/784a81ff-ec3b-4770-8fcd-dc91501159a8" width="275"> <img src="https://github.com/user-attachments/assets/fdaee3f0-680b-4489-9eb0-526431ec963a" width="280"> |

* **Statistical Modelling:** Developed a binary response regression model (Probit) to isolate and measure the marginal effect of variables such as gender, age, education, household configuration (presence of infants/elderly), and income level on the probability of an individual falling below the established time poverty threshold.
<p align="center">
  <img src="https://github.com/user-attachments/assets/9fccb73b-a6a1-4fe5-9d68-2198ea812b4c" width="295">
</p>


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
> *Figure 2: Marginal Effects of Demographic Variables on Time Poverty P![Uploading GW Distribution.svg…]()
robability.*

## 4. Technical Implementation Note
The original raw data consolidation and statistical modelling were executed using **STATA** and **SPSS**. While the legacy `.do` scripts are archived, the methodology strictly followed a Probit Regression approach, ensuring robust treatment of heteroscedasticity and categorical variables for large-scale demographic datasets.
