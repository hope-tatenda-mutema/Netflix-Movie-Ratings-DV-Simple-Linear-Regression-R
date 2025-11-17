# Netflix Ratings Simple Linear Regression Analysis

A statistical analysis examining the relationship between Netflix movie ratings and global availability using Ordinary Least Squares (OLS) regression.

## 📊 Project Overview

This project investigates whether there is a significant relationship between a movie's rating and its global availability on Netflix using simple linear regression analysis. The analysis employs OLS regression techniques to explore patterns in the 2023 Netflix dataset.

## 🎯 Research Question

**Does global availability of a movie on Netflix affect its rating?**

## 📁 Project Structure

```
├── Netflix_Ratings_Simple_Linear_Regression.qmd    # Quarto analysis document
├── Netflix_Ratings_Simple_Linear_Regression.html   # HTML output report
├── Netflix_Simple_Linear_Regression_R.docx         # Word document report
├── Movie_Ratings_by_Global_Availability.png        # Visualization plot
└── OLS_Assumption_Check.png                        # Diagnostic plots
```

## 🔧 Technologies & Packages

- **R** - Statistical computing language
- **tidyverse** - Data manipulation and visualization
- **summarytools** - Descriptive statistics
- **stargazer** - Regression output formatting
- **ggplot2** - Data visualization
- **Quarto** - Document rendering

## 📈 Methodology

### Variables
- **Dependent Variable (DV)**: Movie Rating (numeric)
- **Independent Variable (IV)**: Available Globally (binary: Yes/No)

### Statistical Model

The analysis uses Ordinary Least Squares (OLS) regression:

$$y = b_0 + b_1X + \epsilon$$

**Fitted Regression Equation:**

$$\widehat{\text{Movie Rating}} = 6.445 + 0.128(\text{Available Globally Yes})$$

## 🔍 Key Findings

### Model Coefficients

| Coefficient | Estimate | p-value | Interpretation |
|-------------|----------|---------|----------------|
| Intercept (b₀) | 6.450 | < 2×10⁻¹⁶ | Average rating for movies **NOT** available globally |
| Slope (b₁) | 0.128 | 1.45×10⁻⁶ | Movies available globally have ratings 0.128 points higher on average |

### Model Performance

- **F-statistic**: 23.225 (p < 0.001) - Model is statistically significant
- **R²**: 0.001 (0.13%) - Very low explanatory power
- **Conclusion**: While the relationship is statistically significant, global availability explains only a minimal portion of the variance in movie ratings

## 📊 Visualizations

### Movie Ratings by Global Availability
![Movie Ratings Distribution](https://github.com/hope-tatenda-mutema/Netflix-Movie-Ratings-DV-Simple-Linear-Regression-R/blob/main/Movie%20Ratings%20by%20Global%20Availability.png)

*Scatterplot showing the relationship between global availability and movie ratings with the fitted regression line.*

### OLS Assumption Diagnostics
![Diagnostic Plots](https://github.com/hope-tatenda-mutema/Netflix-Movie-Ratings-DV-Simple-Linear-Regression-R/blob/main/OLS%20Assumption%20Check.png)

*Four diagnostic plots assessing regression assumptions: Residuals vs Fitted, Q-Q Plot, Scale-Location, and Residuals vs Leverage.*

## ✅ Regression Diagnostics

### Assumption Checks

1. **Linearity** ✓ - Appropriate for binary predictor structure
2. **Normality** ⚠️ - Some deviation in Q-Q plot, especially at the tails
3. **Homoscedasticity** ✓ - Equal variance assumption holds reasonably well
4. **Influential Points** ✓ - No influential outliers detected

### Diagnostic Interpretation

- **Residuals vs Fitted**: Shows two vertical clusters (expected for binary predictor) with no obvious patterns
- **Q-Q Plot**: Deviation from normality at the tails suggests caution with hypothesis tests
- **Scale-Location**: Similar variance across both groups confirms homoscedasticity
- **Residuals vs Leverage**: No influential data points affecting model fit

## 📝 Conclusions

1. **Statistical Significance**: Movies available globally have statistically significantly higher ratings (p < 0.001)
2. **Practical Significance**: The effect size is very small (0.128 points), with minimal explanatory power (R² = 0.13%)
3. **Model Validity**: Most OLS assumptions are satisfied, though normality of residuals shows slight violations typical of binary predictors
4. **Recommendation**: While the model provides reliable estimates of group mean differences, the low R² suggests other factors play a much larger role in determining movie ratings

## 👤 Author

**Hope Tatenda Mutema**

## 📄 License

This project is available for educational and research purposes.

## 🚀 How to Use

1. Clone this repository
2. Open the `.qmd` file in RStudio
3. Ensure all required packages are installed:
   ```r
   install.packages(c("tidyverse", "summarytools", "stargazer", "ggplot2"))
   ```
4. Run the analysis or render the Quarto document:
   ```r
   quarto::quarto_render("Netflix_Ratings_Simple_Linear_Regression.qmd")
   ```

## 📊 Data Source

Netflix dataset from 2023 containing movie ratings and global availability information.

---

*For questions or collaborations, please open an issue in this repository.*
