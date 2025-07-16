# Predicting-Visitor-Engagement-at-Five-Guys
Hi there!
In this project, I explored how customers interact with Five Guys locations across Massachusetts. By using mobility data, I aimed to understand patterns in visitor behavior—like how far people travel and how often they return—to help inform smarter business decisions around marketing, staffing, and operations.

* Project in a Nutshell
Using SafeGraph’s Weekly Patterns dataset, I analyzed foot traffic data and defined visitor engagement as:

Engagement Ratio = visit counts / unique visitors

I then built predictive models to estimate engagement based on how frequently people visit and how far they travel.

* Business Question
Can I predict how engaged visitors are based on their distance and visit frequency?

*Tools & Techniques
Python, Jupyter Notebook
Pandas, NumPy – Data wrangling
Matplotlib, Seaborn – Visualizations
Scikit-learn – Linear Regression & Random Forest
Haversine Formula – To compute distance from Boston

* Dataset Highlights
The dataset was filtered to include only Five Guys locations in Massachusetts.
Key fields used:
location_name, latitude, longitude
raw_visit_counts, raw_visitor_counts
visits_by_day, visits_by_each_hour

* Workflow Summary
Data Cleaning – Removed nulls, standardized column names, filtered for relevant locations
Feature Engineering – Calculated distance from Boston and created the engagement ratio
Exploratory Data Analysis – Visualized relationships and identified patterns/outliers
Modeling – Built Linear Regression and Random Forest models
Random Forest performed better with non-linear patterns
Evaluation – Compared actual vs predicted engagement using visual plots

*Key Takeaways
Distance doesn’t always reduce engagement—loyal customers travel farther!
Engagement can be reasonably predicted using just visit counts and distance
Random Forest worked best due to its flexibility with non-linear data

*What’s Next?
Add time-series trends like day-by-day visit patterns
Bring in external data like weather or local events
Turn this into a dashboard with Streamlit or Tableau

*Created by: Muskan Bhatt
Data Analytics Graduate Student
Developed as part of the XN Capstone initiative

* References
SafeGraph Weekly Patterns · Scikit-learn Docs · Research & blog posts
