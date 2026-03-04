# Startup-Failure-Risk-Analysis
Analyze startup failure across 5 sectors using Logistic Regression &amp; Random Forest. This project features robust statistical cleaning (VIF &amp; Chi-Squared) to identify "Fatal Risk Drivers" like high burn rates and industry pressures. Key insight: "Risk Decay" proves survival in the first 3 years is a startup's best shield. 🚀
# 1. Objectives 🎯
- Identify and handle missing values and potential duplicates to ensure a clean analytical base.

- Verify data integrity and ensure appropriate data types for regression and classification tasks.

- Perform VIF (Variance Inflation Factor) analysis to detect and mitigate multicollinearity between variables.

- Examine data distribution and skewness, particularly for financial metrics like fundraising totals.

- Analyze categorical relationships using Chi-Squared tests to map failure reasons to specific industry sectors.

- Compare Logistic Regression and Random Forest models to reveal both linear drivers and complex combinatorial risks.

- Prepare clean, reliable datasets and actionable insights for startup founders and investors.

# 2. Key Findings 🏆
- Confirmed Statistical Independence: The VIF for fundraising_log was 2.501986, well below the threshold of 5, proving that total capital raised is a unique predictor.

- Detected High Skewness: Identified that how_much_they_raised_clean had a high skewness of 4.946, requiring a log transformation to normalize the data for the models.

- The "Maturity Shield": Discovered "Risk Decay," where surviving the first 3 years significantly buffers a startup against future failure.

- Capital Velocity Trap: Found that the speed of spending (fundraising_burn_rate) is often more predictive of failure than the total amount raised.

- Sector-Specific Risks: Chi-Squared tests revealed that Manufacturing faces "Giant" competition, while Information startups fail due to "Execution Flaws".

- Predictive Leader: Random Forest outperformed Logistic Regression in capturing the "Danger Zone" where age and budget size interact.

# 3. Visualizations Included 🎨
- Feature Importance Plots: Bar charts ranking the most critical drivers of startup failure.

- Multicollinearity Heatmaps: Visual representations of VIF scores across all independent variables.

- Distribution & Skewness Charts: Histograms showing the effect of log transformations on fundraising data.

- Sector Risk Analysis: Comparative charts showing failure probability across different industries.

- ROC-AUC Curves: Visual performance comparison between the Logistic Regression and Random Forest models.

# 4. Skills Demonstrated 🛠️
- Data Cleaning: Handling missing values and highly skewed financial distributions.

- Statistical Validation: Implementing VIF Analysis and Chi-Squared Tests to ensure mathematical integrity.

- Feature Engineering: Creating the risk_decay and fundraising_burn_rate metrics.

- Machine Learning: Training, testing, and comparing multiple classification models.

- Problem Solving: Developing strategies to handle "Inf" (infinite) VIF values by refining variable selection.

- Documentation: Explaining complex technical results (like scientific notation in VIF) for non-technical stakeholders.

# 5. Technical Details 💻
- Programming Language: Python

- Main Libraries: pandas, scikit-learn, statsmodels, matplotlib, seaborn

- Key Statistical Checks: Skewness analysis, Variance Inflation Factor (VIF), and Chi-Squared Test of Independence

- Data Volume: Multi-sector analysis covering startups in Finance, Health Care, Information, Manufacturing, and Retail

- Log Transformations: Applied to fundraising_log and years_log to address highly skewed distributions

# 6. Installation and Usage
```bash
# Clone the repository
git clone https://github.com/dgalloe/Startup-Failure.git

# Navigate to project directory
cd Startup-Failure

# Install required dependencies
pip install pandas scikit-learn matplotlib statsmodels seaborn

# Run the analysis notebook
jupyter notebook Startup_Failure.ipynb
