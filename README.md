# UK-Youth-Unemployment-Analysis
This project investigates youth unemployment trends across England and Wales using data from the 2011 and 2021 UK censuses. It combines statistical computing, Bayesian modeling, and dimensionality reduction techniques to explore disparities by region, gender, and industry, and predicts unemployment patterns for 2030. The project aims to equip policymakers, educators, and industry leaders with data-driven insights for inclusive labor market strategies.

## Project Overview 
Youth unemployment remains a persistent concern across the UK. This project focuses on:
1. Analyzing socio-economic disparities in unemployment across 300+ regions
2. Forecasting unemployment trends for 2030 using Bayesian Ridge Regression
3. Visualizing regional, gender, and industry-level gaps through interactive dashboards using Tableau
4. Informing future workforce policies with interpretable, statistically grounded evidence

## Datasets
The project uses official UK census datasets for individuals aged 16–24:
### 2011 Census:
* DC6110EW: Economic Activity by Industry
* DC6201EW: Economic Activity by Gender
* DC5203EW: Highest Qualification by Age
### 2021 Census:
* RM024: Economic Activity by Gender
* RM064: Economic Activity by Industry

### Data Preparation 
The raw census tables required extensive cleaning across years:
1. Whitespace and formatting corrections for region names
2. Data type standardization (int64 for counts, object for region labels)
3. Duplicate checks to ensure unique region entries
4. Missing Value Imputation:
   * Used IterativeImputer with Bayesian Ridge Regression to fill missing 2011 values
5. Region Mapping:
   * Mapped 2011 regions to their 2021 counterparts to resolve renamed/merged districts
   * Enabled consistent comparison across census years

### Statistical & ML Techniques
1. Dimensionality Reduction
   * PCA (Principal Component Analysis): Simplified feature space to uncover broad patterns in youth labor trends
   * UMAP (Uniform Manifold Approximation and Projection): Preserved local structure and revealed nuanced regional disparities
2. Forecasting 2030 Trends
   * Bayesian Ridge Regression
3. Clustering
   * K-Means: Clustered PCA-reduced data to group regions with similar youth employment patterns

## Visual Analytics: 
Built interactive **Tableau** dashboards to communicate insights clearly. All dashboards included interactive filters, hover-based tooltips, choropleth layers for spatial exploration
1. Dashboard 1: Educational Attainment vs. Employment 
2. Dashboard 2: Unemployment in Major Cities
3. Dashboard 3 & 4: Labor Participation (2011 vs 2021)
4. Dashboard 5: Predicted Unemployment for 2030
5. Dashboard 6: PCA vs UMAP Comparison

## Key Insights 

1. Gender Disparity: Males had higher unemployment; females showed higher inactivity, suggesting re-engagement strategies are needed.
2. Regional Inequality: Cities like Manchester showed major progress, but regions like Rutland saw no change.
3. Industry-Specific Gaps: Retail, Hospitality, and Public Services employed the most youth; Construction lagged behind.
4. Education Link: Surprisingly, Level 4 qualification showed only a moderate correlation with employment—highlighting a potential mismatch in skills vs. market demand.

## Impact and Applications
This project delivers a replicable and interpretable framework to:
* Track youth labor patterns over time
* Guide resource allocation for underserved regions
* Inform gender- and sector-specific policy interventions
* Predict employment trends with Bayesian confidence

## Future Work
1. Integrate external macroeconomic indicators (inflation, GDP)
2. Deploy web-based dashboards using Streamlit or Plotly
3. Test higher-order Bayesian models for richer 2030 projections
4. Add interactive region-level policy recommendations

## Citation 
If you find this project useful, please consider citing it:
```
@software{sharan2025censusunemployment,
  author = {Tanya Sharan},
  title = {Youth Unemployment Trends in England and Wales: A Census-Based Analysis},
  year = {2025},
  url = {https://github.com/yourusername/census-youth-unemployment}
}
```



