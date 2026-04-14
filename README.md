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
</p>


## 3. Key Findings & Data Insights
The econometric model yielded statistically significant findings with high commercial value for understanding human and urban behaviour:
|  |  | 
| :--- | :---: |
| **The "Double Shift" Reality:** <br> 12.84% of the urban population is time-poor during the working week. Women have a significantly higher probability of experiencing this condition (representing 65.19% of the total affected), driven by the asymmetrical burden of unpaid care work. | <img src="https://github.com/user-attachments/assets/c73724fe-0aaa-4cae-96fc-099ec35afdad" width="300"> |
| .<br><br>**Income vs. Time Paradox:** Contrary to traditional perceptions, time poverty cuts across all socio-economic levels. In fact, higher levels of education and active labour market participation *increase* the probability of being time-poor on weekdays due to the intensity of working hours.<br><br>. | <img src="https://github.com/user-attachments/assets/52bbf6e7-8f22-44a9-9073-1f15625a214a" width="2000"> |
| **The Impact of Commuting & Care:** The inclusion of commuting times to the workplace drastically increases the marginal propensity for time scarcity. | <img src="https://github.com/user-attachments/assets/65f2c1fc-412b-4af7-9799-869bdd62f40e" width="350"> |
| **Unpaid Care & The General Production Boundary:** While dependents and children increase time poverty, elderly members decrease it at rates comparable to hiring domestic help. This reveals hidden value overlooked by traditional economics: seniors' unpaid caregiving enables others' market participation. Consequently, this vital non-market labor operates squarely within the General Production Boundary. | <img src="https://github.com/user-attachments/assets/ee0d099a-14ee-415d-925f-0ad3129e8168" width="295"> |
|  |  | 


## Technical Implementation Note
The original raw data consolidation and statistical modelling were executed using **STATA** and **SPSS**. While the legacy `.do` scripts are archived, the methodology strictly followed a Probit Regression approach, ensuring robust treatment of heteroscedasticity and categorical variables for large-scale demographic datasets.

## Resources & Documentation

* **Full Research Paper:** [Download PDF Version](https://github.com/user-attachments/files/26713341/Tesis.El.Tiempo.como.Diension.Alternativa.para.la.Medicion.de.la.Pobreza.y.sus.Determinantes-Cristobal.Valenzuela.Perez-2017.1.pdf) — *Complete theoretical, methodological and econometric analysis (Spanish).*
* **Defense Presentation:** [View Slides](https://github.com/user-attachments/files/26713824/ppt_Sv4.pptx) — *Key findings and visual summary used for academic defense.*
* **Official University Publication:** [Link to University Repository](https://research.ebsco.com/c/d6h2ty/search/details/yft4d4srff?q=Pobreza%20tiempo)
