SpaceX Launch Success Prediction - IBM Data Science Capstone
Table of Contents

Project Overview

Business Problem

Data Sources

Methodology

Key Questions Addressed

Summary of Findings

Machine Learning Model

Technologies Used

Project Structure

Acknowledgments

Project Overview
This project is the final capstone for the IBM Data Science Professional Certificate. The primary goal is to analyze historical SpaceX launch data to identify key factors contributing to launch success and to build a machine learning model capable of predicting the outcome of future launches. The analysis covers everything from data collection and wrangling to exploratory data analysis (EDA), interactive dashboard creation, and predictive modeling.

Business Problem
SpaceX is a dominant player in the space launch industry. A significant part of its competitive advantage comes from reusing the first stage of its rockets, which dramatically reduces the cost of each launch. If SpaceX can predict whether the first stage will be successfully recovered, it can determine a more accurate price for a launch contract. This project aims to use data science to determine the factors that lead to a successful launch and first-stage landing, thereby helping SpaceX make more informed business decisions and maintain its competitive edge.

Data Sources
The dataset was compiled using two primary methods:

SpaceX REST API: Pulled comprehensive data on past launches, including details about the rockets, payloads, launch sites, and outcomes.

Web Scraping: Scraped a Wikipedia page listing SpaceX launches to gather supplementary information and cross-reference data points, particularly regarding booster versions and launch costs.

Methodology
The project followed a standard data science workflow:

Data Collection: Gathered data from the sources mentioned above using Python's requests library and BeautifulSoup.

Data Wrangling & Cleaning: Processed and cleaned the collected data using Pandas. This involved handling missing values, standardizing formats, and creating new features for analysis.

Exploratory Data Analysis (EDA) with SQL & Python: Performed initial database exploration using SQL. Subsequently, used Matplotlib and Seaborn to visualize relationships between launch variables (e.g., launch site, payload mass, orbit type) and the launch outcome.

Interactive Visualizations: Developed an interactive dashboard using Plotly and Dash. Created interactive maps with Folium to show the locations of launch sites and mark their success/failure rates.

Predictive Modeling:

Feature Engineering: Prepared the data for machine learning by scaling numerical features and applying one-hot encoding to categorical features.

Model Training: Trained and evaluated several classification models, including Logistic Regression, Support Vector Machine (SVM), Decision Tree, and K-Nearest Neighbors (KNN).

Hyperparameter Tuning: Used GridSearchCV to find the optimal parameters for the best-performing model to maximize its accuracy.

Key Questions Addressed
The analysis sought to answer several key questions:

How do launch success rates differ across various launch sites?

What is the relationship between payload mass and launch outcome?

Is there a correlation between the type of orbit and the success of a launch?

Which rocket booster versions have the highest success rates?

Summary of Findings
Launch Site Impact: Certain launch sites, like CCAFS SLC-40, demonstrated higher success rates over time, likely due to operational experience and infrastructure improvements.

Payload Mass vs. Success: A clear relationship was observed where launches with extremely heavy payloads had slightly lower success rates, especially in the early years.

Orbit Type Matters: Launches to specific orbits, such as Geostationary Transfer Orbit (GTO), are more complex and showed a different success profile compared to launches to Low Earth Orbit (LEO).

Booster Version Evolution: Newer versions of the Falcon 9 booster (e.g., Block 5) have a near-perfect success rate, highlighting the impact of iterative engineering improvements.

Technologies Used
Data Manipulation & Analysis: Python, Pandas, NumPy

Data Collection: Requests, BeautifulSoup

Database: SQL (SQLite)

Data Visualization: Matplotlib, Seaborn, Plotly, Folium

Machine Learning: Scikit-learn

IDE: Jupyter Notebooks

Project Structure

The repository is organized into a series of Jupyter Notebooks, each corresponding to a specific stage of the project:

Acknowledgments
This project was completed as part of the IBM Data Science Professional Certificate on Coursera.

Thanks to SpaceX for making their launch data publicly available via their API.
