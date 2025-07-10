# Predicting-Visitor-Engagement-at-Five-Guys
Predicting Visitor Engagement at Five Guys Locations in Massachusetts Using Mobility Data

Welcome! This project explores how mobility data can be used to understand and predict visitor engagement at Five Guys restaurant locations across Massachusetts. The goal is to help businesses like Five Guys identify patterns in customer behavior—such as how often people return and how far they travel—to support better decision-making in marketing, staffing, and operations.

🚀 Project Overview
With customer behavior becoming increasingly important in the quick service restaurant (QSR) space, this project leverages SafeGraph’s Weekly Patterns dataset to uncover insights that go beyond raw foot traffic. We're looking at visitor frequency, distance traveled, and repeat engagement to build predictive models that estimate how engaged customers are with specific Five Guys locations.

📌 Business Question
Can we predict how engaged visitors will be at Five Guys locations in Massachusetts based on how far they travel and how frequently they visit?
This project defines engagement as the ratio of visit counts to unique visitors, giving us a more behavioral view than simply counting footfall.

🧰 Tools & Technologies Used
Python
Pandas, NumPy – Data wrangling & transformation
Seaborn, Matplotlib – Visualizations
Scikit-learn – Modeling (Linear Regression & Random Forest)
Geospatial logic (Haversine Formula) – Calculating distance from a central point (Boston)
Jupyter Notebook – Experimentation & development

🔍 Dataset Description
We worked with a filtered version of the SafeGraph Weekly Patterns dataset that includes:

location_name
latitude, longitude
raw_visit_counts, raw_visitor_counts
visits_by_day, visits_by_each_hour
median_dwell (not used in final model)
For simplicity and relevance, only Five Guys locations in Massachusetts were included.

📈 Workflow Summary
Data Cleaning
Removed null values in key fields
Standardized column names
Filtered dataset for Five Guys in Massachusetts

Feature Engineering
Computed distance_from_home using latitude/longitude and the Haversine formula
Calculated engagement_ratio = raw_visit_counts / raw_visitor_counts
Exploratory Data Analysis (EDA)
Visualized relationships between visits, distance, and engagement
Identified patterns and outliers using scatterplots and histograms

Modeling
Built two models: Linear Regression and Random Forest Regressor
Evaluated model performance using RMSE and R² Score
Random Forest gave better predictions for nonlinear behavior
Visualization of Predictions
Line plots comparing actual vs predicted engagement
Insights from EDA and model outputs to support business interpretation

📊 Key Insights
Distance isn’t always a barrier: Some customers travel longer distances yet show high engagement.
Visitor engagement can be predicted with decent accuracy using just visit counts and distance.
Random Forest outperforms Linear Regression, likely due to its ability to handle non-linearity in behavioral data.

🧪 Next Steps & Future Work
Add more time series features like visits_by_day trends
Incorporate external variables like weather or local events
Deploy as a live dashboard using Streamlit or Tableau Public

📁 Repository Structure
graphql
Copy
Edit
📦 fiveguys-visitor-engagement/
├── data/                  # Filtered dataset (CSV)
├── notebooks/             # Jupyter notebooks for EDA & modeling
├── visuals/               # EDA and prediction charts
├── fiveguys_model.py      # Python script for the modeling pipeline
├── README.md              # You're here!
👩‍💻 Maintainer
Muskan Bhatt
Data Analytics Graduate Student
Project developed as part of the XN Capstone initiative

📚 References
SafeGraph Weekly Patterns Dataset
Vallapuram et al. (2022) – Retail Loyalty through Foot Traffic
He & Patel (2021) – Predicting Store Performance Using Visitor Metrics
Scikit-learn documentation
Towards Data Science Blog – Random Forest vs Linear Regression for Real-World Data

