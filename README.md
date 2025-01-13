# From Data to Insights: Analyzing Factors Impacting Brewery Sales

This project investigates factors influencing brewery sales by analyzing a dataset of 10 million records (2020–2024). By uncovering key insights, the aim is to help breweries optimize inventory management, marketing, and operational efficiency in a competitive market.

## Key Features of the Dataset

- **Production Factors:** Beer style, pH levels, fermentation time, temperature, and ingredient ratios.
- **Sales Performance:** Total sales, SKU, and geographical location.
- **Quality Metrics:** Alcohol content, bitterness, color, and quality scores.
- **Efficiency:** Loss during brewing, fermentation, and bottling/kegging.

## Dataset
The dataset used in this project can be accessed on Kaggle:
[Brewery Operations and Market Analysis Dataset](https://www.kaggle.com/datasets/ankurnapa/brewery-operations-and-market-analysis-dataset).

## Methodology

### 1. Data Preprocessing
- Imputed missing values: **Median** for numerical, **Mode** for categorical.
- Removed duplicates: 894,036 entries eliminated.
- Standardized data formats: Unified date formats, adjusted temperature to Celsius.
- Managed outliers using logical limits and quantile-based trimming.

### 2. Hypothesis Testing
Conducted statistical analyses to identify relationships between production variables and outcomes:
- **Beer Style vs. Quality**: No significant relationship (Chi-Square Test, p-value: 0.355).
- **pH Levels Across Locations**: Consistent across locations (ANOVA, p-value: 0.996).
- **Fermentation Time vs. Sales**: No significant difference (t-test, p-value: 0.690).
- **Bitterness vs. Quality**: Slight negative impact (Regression, p-value: 0.008).
- **Alcohol Content vs. Sales**: No significant difference (Z-Test, p-value: 0.220).

### 3. Dimensionality Reduction and Model Optimization
- Applied **Gaussian Random Projection** and **Johnson-Lindenstrauss Lemma**.
- Reduced runtime for training large datasets by ~34% but increased prediction error in Linear Regression.

### 4. Scalability Enhancements
- Utilized Kaggle T4 GPUs to reduce computational time from 13.03 minutes to 8.55 minutes.

## Results
- Hypothesis testing highlighted key insights but showed limited effects of certain production variables on sales and quality.
- Dimensionality reduction helped scale computations but did not improve Linear Regression accuracy.

## Repository Structure
```
.
├── dataset-eda-regression-and-clustering.ipynb        # Exploratory Data Analysis of the used dataset
├── hypothesis_testing.ipynb        # Statistical tests and hypothesis validation
├── randomised_scaling_techniques.ipynb  # Dimensionality reduction and scaling techniques
└── README.md                       # Project overview (this file)
```

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/Aarya-Gupta/Brewery-Sales-Analysis-Data-Science.git
   ```
2. Open the `.ipynb` files in Jupyter Notebook or Google Colab.
3. Ensure dependencies are installed:
   ```bash
   pip install -r requirements.txt
   ```

## Future Work
- Implement advanced machine learning models like **Random Forests** or **Neural Networks**.
- Explore real-time analytics using temporal models such as **ARIMA** or **LSTMs**.
- Enhance scalability with distributed computing frameworks (e.g., Apache Spark).

## Authors
- Aarya Gupta
- Adarsh Jha
- Keshav Chhabra

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
