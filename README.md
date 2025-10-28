# Breast Cancer Recurrence Statistical Analysis

## Project Overview

A comprehensive statistical analysis applying logistic regression, ANOVA, and multiple linear regression to examine tumor characteristics and predict breast cancer recurrence. This project demonstrates advanced statistical modeling techniques for clinical decision support in oncology using data from the UCI Machine Learning Repository.

---

## Key Findings

- **Tumor Grade as Primary Predictor**: Degree of malignancy more than doubles recurrence odds (OR = 2.09, 95% CI: 1.39-3.18, p < 0.001)
- **Lymph Node Involvement**: Each additional invasive node increases recurrence odds by 11.8% (OR = 1.12, p = 0.008)
- **Tumor Size Association**: Larger tumors significantly associated with recurrence (mean 29.24cm vs 25.21cm, p = 0.001)
- **Predictive Model Performance**: Logistic regression achieves AUC = 0.725, demonstrating good discriminative ability

---

## Dataset Information

- **Source**: [UCI Machine Learning Repository - Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer)
- **Size**: 286 patients with complete data
- **Variables**: Age, menopause status, tumor size, invasive nodes, node caps, degree of malignancy, breast location, quadrant, radiation therapy
- **Outcome**: Recurrence vs. no recurrence events
- **Data Quality**: Complete cases after removing missing values

---

## Technologies & Methods

### Programming & Tools
- **R** - Statistical modeling and analysis
- **R Markdown** - Reproducible research documentation
- **Statistical packages** - Advanced regression and diagnostics

### Statistical Methods
- Logistic regression for binary outcomes
- Analysis of Variance (ANOVA)
- Multiple linear regression
- Pearson correlation analysis
- Two-sample t-tests (Welch's method)
- Shapiro-Wilk normality testing
- Chi-square tests for proportions
- ROC curve analysis

### R Libraries Used
```r
library(ggplot2)     # Data visualization
library(dplyr)       # Data manipulation
library(pROC)        # ROC curve analysis
library(car)         # Regression diagnostics
library(lmtest)      # Statistical testing
library(knitr)       # Report generation
```

---

## Analysis Components

### Module 1: Descriptive Statistics and Normal Distribution
- Summary statistics by recurrence status
- Shapiro-Wilk normality tests
- Distribution visualizations (histograms, Q-Q plots, boxplots)
- Probability calculations using normal approximation

### Module 2: Statistical Inference and Hypothesis Testing
- Two-sample t-tests for tumor size differences
- Welch's t-test for unequal variances
- Hypothesis testing for invasive nodes by treatment group
- 5-step hypothesis testing framework

### Module 3: Correlation and Simple Linear Regression
- Pearson correlation between tumor characteristics
- Simple linear regression for malignancy prediction
- Scatter plots with regression lines
- Global F-test (ANOVA for regression)

### Module 4: Multiple Linear Regression
- Multivariate prediction of invasive nodes
- Model comparison using adjusted R²
- Diagnostic plots (residuals, Q-Q, leverage)
- Identification of influential observations

### Module 5: Analysis of Variance (ANOVA)
- One-way ANOVA for tumor size across age groups
- Two-way ANOVA (ANCOVA) with interaction terms
- Tukey's HSD post-hoc tests
- Interaction plots

### Module 6: Logistic Regression and Proportions
- Binary outcome prediction (recurrence)
- Odds ratios with 95% confidence intervals
- Proportion tests and chi-square analysis
- ROC curve and AUC evaluation

---

## Key Insights & Clinical Implications

### For Clinicians
- **Risk Stratification**: Tumor grade and nodal status provide strong predictive value for recurrence risk
- **Treatment Planning**: Statistical models support evidence-based decisions for aggressive vs. conservative treatment
- **Patient Counseling**: Quantified risk factors help communicate prognosis to patients

### For Researchers
- **Reproducible Methodology**: Complete statistical workflow documented in R Markdown
- **Model Validation**: Diagnostic procedures identify assumptions and limitations
- **Framework Application**: Analytical approach transferable to similar oncology datasets

### For Healthcare Systems
- **Predictive Analytics**: Moderate AUC (0.725) demonstrates clinical utility of basic parameters
- **Resource Allocation**: Risk models support targeted follow-up and intervention strategies
- **Quality Improvement**: Statistical analysis identifies factors for protocol optimization

---

## Repository Structure
```
breast-cancer-statistical-modeling/
├── README.md                          # Project overview
├── BreastCancer_Morshedi.Rmd         # R Markdown analysis code
├── BreastCancer_Morshedi.html        # Rendered HTML report
└── LICENSE                            # MIT License
```

**Note**: Dataset is loaded directly from UCI repository URL in the analysis code.

---

## How to Run This Analysis

### Prerequisites
- R (version 4.0 or higher)
- RStudio (recommended)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/morshediem-mm/breast-cancer-statistical-modeling.git
```

2. Install required R packages:
```r
install.packages(c("ggplot2", "dplyr", "pROC", "car", "lmtest", "knitr"))
```

3. Open `BreastCancer_Morshedi.Rmd` in RStudio

4. Click "Knit" to generate the HTML report

The analysis will automatically download the dataset from the UCI repository.

---

## Statistical Highlights

### Hypothesis Testing Results
- **Tumor Size Difference**: t = -3.28, p = 0.001 (recurrence vs. non-recurrence)
- **Nodal Involvement**: t = -4.48, p < 0.001 (radiation vs. no radiation)
- **Correlation**: r = 0.161, p = 0.007 (tumor size vs. invasive nodes)

### Model Performance
- **Best Predictive Model**: Model 1 (nodes + malignancy), Adj. R² = 0.050
- **Logistic Regression**: AUC = 0.725, indicating good discrimination
- **Primary Predictor**: Degree of malignancy (OR = 2.09, p < 0.001)

### ANOVA Results
- **Age Effect**: F(5,280) = 0.413, p = 0.84 (not significant)
- **Quadrant Effect**: F(5,275) = 0.816, p = 0.54 (not significant)

---

## Limitations

### Methodological Considerations
- **Sample Size**: Relatively small dataset (n=286) limits statistical power
- **Variable Conversion**: Categorical ranges converted to midpoints may introduce measurement error
- **Normality Violations**: Some variables deviate from normal distribution (addressed via robust methods)
- **Influential Observations**: Observation #64 has perfect leverage due to single case in age group

### Clinical Context
- **Missing Modern Biomarkers**: Lacks hormone receptor, HER2, and molecular subtype data
- **Selection Bias**: Observational design limits causal inference
- **Temporal Relevance**: Dataset may not reflect current treatment protocols
- **Single Institution**: Generalizability to broader populations uncertain

Despite limitations, this analysis demonstrates rigorous statistical methodology and provides clinically relevant insights into breast cancer recurrence factors.

---

## About This Project

This analysis was completed as part of my **MS in Health Informatics program at Boston University**. It demonstrates proficiency in:

- Advanced statistical modeling for healthcare applications
- Clinical data analysis and interpretation
- Reproducible research practices using R Markdown
- Biostatistics and epidemiological methods
- Healthcare data science and predictive analytics

---

## Author

**Elham Morshedi Meibodi**  
MS Health Informatics | Healthcare Data Analyst  
DDS with 10+ years of clinical experience

[LinkedIn](https://linkedin.com/in/elham-morshedi-meibodi-dmd) | [Email](mailto:morshediem@gmail.com) | [Google Scholar](https://scholar.google.com/citations?user=NAKEQVMAAAAJ)

---

## Related Work

This analysis complements my published clinical research:
- Treatment Effects of R-appliance and Anterior Inclined Bite Plate, *Journal of Applied Oral Sciences*
- Cervical Vertebrae Anomalies in Class III Patients, *Journal of Craniovertebral Junction and Spine*
- Effect of Mandibular Tongue Cribs on Dentoskeletal Changes, *World Journal of Orthodontics*

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Citation

If you use this analysis in your research, please cite:
```
Morshedi, E. (2025). Breast Cancer Recurrence Statistical Analysis. 
GitHub repository: https://github.com/morshediem-mm/breast-cancer-statistical-modeling
```

---

## Acknowledgments

- **Dataset**: Matjaz Zwitter, M. S. (1988). Breast Cancer [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C51P4M
- **Course**: MS Health Informatics Program
- **Institution**: Boston University
- **Application**: Clinical oncology research and biostatistics

---

*Last Updated: October 2025*
```
