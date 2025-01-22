# Public Libraries Engagement Analysis in Connecticut

## Project Overview
This project leverages machine learning techniques to analyze public libraries in Connecticut, USA. The goal was to enhance community engagement and identify key factors that differentiate successful libraries from others. By using both supervised and unsupervised learning models, we aimed to uncover actionable insights to support the strategic development of public libraries.

## Motivation
Public libraries are cornerstones of education, culture, and community engagement. Despite their importance, they face challenges in maintaining relevance and community involvement in a fast-paced, digital world. Our motivation stemmed from the desire to:
1. Develop a **Community Engagement Score** for libraries.
2. Use machine learning models to classify libraries and provide data-driven recommendations.
3. Highlight strategies to improve community engagement while considering budgetary constraints.

## Dataset
The dataset, sourced from [data.gov](https://data.ct.gov), includes historical data for 208 libraries spanning 1996 to 2023. Key features include:
- **Demographic Data**: Economic rankings and service area populations.
- **Social Data**: Visits, registrations, circulations, and program attendance.
- **Financial Data**: Operational income, municipal tax appropriations, and salary expenditures.

### Data Preparation
- Removed libraries with excessive missing data, reducing the dataset to 160 libraries (85% of the original).
- Imputed missing values using techniques like linear regression, interpolation, and forward/backward filling.
- Created aggregated statistical features for unsupervised models (mean, median, min, max, std).

## Methodology
### 1. Unsupervised Learning
- **Goal**: Cluster libraries based on shared characteristics.
- **Techniques Used**:
  - **K-Means**: Determined optimal clusters using the Elbow Method.
  - **Gaussian Mixture Model (GMM)**: Selected optimal components using AIC/BIC scores.
  - **Agglomerative Clustering**: Evaluated using silhouette scores.
- **Outcome**: Libraries were grouped into clusters, highlighting socioeconomic and social engagement disparities.

### 2. Supervised Learning
- **Goal**: Classify libraries by community engagement levels.
- **Community Engagement Score**:
  - Weighted formula: 70% library visits and 30% registered borrowers per capita.
  - Libraries were classified into four levels: Excellent, Good, Average, and Failing.
- **Models Tested**:
  - Decision Tree, Random Forest, XGBoost, Gradient Boosting, KNN.
  - **XGBoost** performed best across precision, recall, F1 score, and accuracy.
- **SHAP Analysis**: Identified feature contributions to model predictions, revealing key drivers of community engagement.

## Results
- **Unsupervised Learning**:
  - Libraries in higher socioeconomic clusters had greater community engagement.
  - Key factors included visits, circulations, and program attendance.
- **Supervised Learning**:
  - XGBoost achieved superior classification results.
  - SHAP analysis highlighted critical engagement drivers, such as registered borrowers and program participation.
- **Visual Insights**:
  - Optimal program offerings and resource allocations were identified for improving engagement.

## Repository Structure
- `data/`: Cleaned datasets and preprocessing scripts.
- `notebooks/`: Jupyter notebooks for all analysis steps.
- `README.md`: Project documentation.

## How to Run
1. Clone this repository:
   ```bash
   
## Authors
- **Rotem Ben Attar - Unsupervised Learning**
- **Barak Wirzberger - Supervised Learning**

## Acknowledgments
Special thanks to the course lecturer Dr. Chen Hajaj for their guidance and support throughout the project and in this course.

## Future Directions
1. **Refining the Community Engagement Score**:
   - Incorporate additional social and demographic factors, such as program diversity or digital resource usage, to create a more comprehensive engagement index.
2. **Longitudinal Analysis**:
   - Expand the analysis to identify long-term trends in library engagement, focusing on factors driving changes over multiple decades.
3. **Exploring External Data Integration**:
   - Integrate external data sources, such as municipal budgets, local education statistics, or community surveys, to enrich the dataset and provide deeper insights into library usage patterns.
4. **Targeted Recommendations for Underperforming Libraries**:
   - Develop tailored action plans for libraries in the "Failing" category by identifying specific areas for improvement, such as targeted marketing campaigns or resource reallocation.
5. **Interactive Dashboard**:
   - Create a dynamic and user-friendly dashboard to allow stakeholders, such as policymakers and library managers, to explore the data, visualize trends, and assess the effectiveness of implemented strategies.



