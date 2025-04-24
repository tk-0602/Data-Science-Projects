# Data-Science-Projects

This repository is a collection of data science projects, demonstrating my skills and experience in applying data analysis, machine learning, and statistical techniques to a variety of situations. This includes real-world scenarios. Each of the projects in this repository highlight different aspects of the data science workflow, from data collection and preprocessing to model development and interpretation. These projects reflect my ability to extract meaningful insights from complex datasets and develop solutions that can drive business decisions.

For my projects focusing specifically on machine learning methodologies, please explore my dedicated repository: [Machine-Learning-Projects](https://github.com/tk-0602/Machine-Learning-Projects).

<details>
  <summary><h2>Sentiment Analysis of Airline Reviews</h2></summary>
  
  This project is part of the [British Airways Data Science Virtual Experience on Forage](https://www.theforage.com/simulations/british-airways/data-science-yqoz) during which I applied data science techniques to analyse customer feedback and enable data-driven decision-making. This involved performing sentiment analysis on airline reviews, building machine learning models to predict the most important factors towards customers completing their bookings, and visualising key trends to inform improvements. For this, I used Python and natural language processing (NLP) techniques to extract insights from unstructured text data in the form of online reviews which I scraped and saved to a `.csv` file (the `data-BA_reviews.csv` file included in this repository). Overall, I developed a deeper understanding of how data science can be used in various industries (the aviation industry, in this case) to drive customer-focused decision-making, improve operational efficiency, and enhance the overall passenger experience.
  
  <details>
  <summary><h3>Task 1: Web Scraping and Sentiment Analysis</h3></summary>
  This notebook is the first task of a two-part project aimed at predicting customer booking behaviours. Here, the focus is on collecting raw data and preparing it for analysis. Using web scraping techniques, the notebook extracts reviews from a public website, processes the data to ensure cleanliness and consistency, and prepares it for use in predictive modelling.
  
  <break></break>
  
  The extracted data was processed and analysed using natural language processing (NLP) techniques to perform sentiment analysis to provide valuable insights into customer satisfaction and experience with British Airways.
  
  ### Key Features
  
  - Web scraping using `BeautifulSoup` and `requests` libraries to extract review data from Skytrax - collected a substantial number of reviews (3500), iterating through multiple pages dynamically, and stored them in the `data-BA_reviews.csv` file which is also included here.
  - Initial text preprocessing including trimming whitespace as well as removing HTML tags, special characters, and stopwords.
  - Advanced data visualisation techniques using Matplotlib and Seaborn to present findings effectively as histograms and wordclouds (utilising the `wordcloud` library). 
  
  ### Results
  
  - Successfully scraped and cleaned a dataset containing reviews, bulding techniques and gaining experience for subsequent predictive analysis.
  - Visualised sentiment distribution across various aspects of the airline service.
  - Created a wordcloud to highlight frequently mentioned positive and negative aspects.
  - Demonstrated the feasibility of automating data collection from dynamic web pages.
  
  <img src = "British-Airways-Data-Science/BA Data Science plots/01 Web Scraping and Sentiment Analysis/Reviews_per_Score.png">
  
  <img src = "British-Airways-Data-Science/BA Data Science plots/01 Web Scraping and Sentiment Analysis/Wordcloud.png">
  
  ### Applications
  
  In the context of this Virtal Experience Program:
  
  - Enhance customer experience by addressing common pain points identified in negative reviews.
  - Inform targeted marketing strategies based on positive aspects highlighted by customers.
  - Present the ability to benchmark against competitors by comparing sentiment scores.
  
  How this will add to my data analysis and data science experience:
  
  - The web scraping techniques can be adapted to collect data from other domains, such as e-commerce, social media, or news sites.
  - The cleaned and structured data produced from this can serve as input for text analysis, sentiment analysis, or predictive modelling in various contexts (e.g. to create and train an RNN for predicting the next word in similar reviews).
  
  ### Potential Extensions
  
  - Implement advanced NLP techniques like topic modeling to automatically categorize review content.
  - Develop an automated solution by extending the use of the `BeautifulSoup` library here as well as adding real-time sentiment monitoring to track changes in customer satisfaction on a more granular level.
  - Integrate sentiment analysis results with other data sources (e.g. flight data and customer demographics) to provide more comprehensive insights
  - Create an interactive dashboard for easy exploration of sentiment trends and patterns.
  </details>
  
  <details>
  <summary><h3>Task 2: Predictive Modeling of Customer Bookings</h3></summary>
  This notebook represents the second part of the project of understanding and predicting customer booking behaviours. It builds on the foundational data exploration conducted in Part 1 and implements machine learning solutions that address a specific predictive task: determining whether a customer will complete a booking.
  
  ### Key Features
  
  - Performed data cleaning and transformation, including handling missing values, feature engineering, and encoding categorical variables.
  - Highlighted distributions and potential features in the data using bar graphs, boxplots, and kernel density estimate (KDE) plots scatter plots created with the `matplotlib` and `seaborn` libraries.
  - Implemented supervised learning models using scikit-learn and conducted hyperparameter tuning via grid search to optimise model performance.
  - Evaluated models using metrics such as accuracy, precision, recall, and F1 score.
  
  ### Results
  - The trained models successfully predicted customer booking outcomes with high accuracy (0.85 and 0.83 before and after hyperparameter optimisation, respecitvely).
  - In between the two, XGBoost with hyperparameter optimisation made better predections as indicated by the models' F1 scores in particular where the initial model had an F1 score of 0.08 which then improved to 0.21 with hyperparameter optimisation. However, since this is still below 0.5, the model still had rather poor performance. This could perhaps be improved by creating more training data using data augmentation, further optimising the hyperparameters, or even using another model such as a Random Forest Classifier or simpler regression methods like Linear, Lasso, Ridge, etc. 
  - Feature importance analysis identified critical factors influencing booking behaviour, namely `purchase_lead` (the number of days in between the date of booking and the date of the flight) and `length_of_stay`.
  
  
  <img src = "British-Airways-Data-Science/BA Data Science plots/02 Predictive Modeling of Customer Bookings/Outliers_in_Numeric_Columns.png">
  
  Box plots to identify outliers in the numeric columns.
  
  <break></break>
  
  <img src = "British-Airways-Data-Science/BA Data Science plots/02 Predictive Modeling of Customer Bookings/Dist_of_Numerical_Data.png">
  
  Distributions of the numerical columns.
  
  <break></break>
  
  <img src = "British-Airways-Data-Science/BA Data Science plots/02 Predictive Modeling of Customer Bookings/Feature_Transformation.png">
  
  The distributions were not normal so feature transformation was performed so that the ML model will have better results.
  
  <break></break>
  
  <img align = "left" src = "British-Airways-Data-Science/BA Data Science plots/02 Predictive Modeling of Customer Bookings/XGBoost.png">
  
  Confusion matrix for the initial XGBoost Classifier:
  
  - Accuracy (Test Set): 0.85
  - Precision (Test Set): 0.42
  - Recall (Test Set): 0.04
  - F1-Score (Test Set): 0.08
  - roc_auc (test-proba): 0.52
  - roc_auc (train-proba): 0.53

  <br clear = "left"/>
  
  <break></break>
  
  <img align = "left" src = "British-Airways-Data-Science/BA Data Science plots/02 Predictive Modeling of Customer Bookings/XGBoost_with_Hyperparameter_Optimisation.png">
  
  Confusion matrix for the classifier after hyperparameter optimisation:
  
  - Accuracy (Test Set): 0.83
  - Precision (Test Set): 0.34
  - Recall (Test Set): 0.15
  - F1-Score (Test Set): 0.21
  - roc_auc (test-proba): 0.55
  - roc_auc (train-proba): 0.98

  <br clear = "left"/>
  
  <break></break>
  
  <img src = "British-Airways-Data-Science/BA Data Science plots/02 Predictive Modeling of Customer Bookings/Feature_Importance.png">
  
  Results of the most important features determined by the model.
  
  ### Applications
  
  - Enhance the booking experience by prioritising features important to customers within the user interface.
  - Optimise pricing strategies by identifing price sensitivities in different customer segments. This can also include personalising marketing campaigns (e.g. loyalty programs and special offers) by targeting customers with a higher likelihood of purchasing.
  - Extend the data analysis and ML models into a real-time predictive system in which the models (and hyperparameters) constantly update as live data is added.
  
  ### Potential Extensions
  
  - Compare the current models with other types such as Random Forest.
  - Explore data augmentation techniques to increase the training and test data samples.
  - Implement deep learning approaches such as neural networks for potentially higher accuracy.
  - Utilise ensemble methods for potentially improved performance by directly combining the predictions from multiple models or even combining the predictions from models trained on different representations of the data.
  - Incorporate additional data sources like macroeconomic indicators or competitor pricing to enhance the model's predictive power.
  </details>

</details>

<details>
  <summary><h2>Customer Churn and Diversity Analysis in a Call Centre</h2></summary>
  
  This project is part of the [PwC Switzerland Power BI Virtual Case Experience on Forage](https://www.theforage.com/simulations/pwc-ch/power-bi-cqxg). During this I utilised data visualisation, automation, and data cleaning techniques to address real-world business challenges. The project involved developing a series of interactive Power BI dashboards focusing on Call Centre Trends, Customer Retention, and Diversity & Inclusion. These dashboards were designed to provide actionable insights into key aspects of business operations and, in this case, help identify patterns in customer behaviour, optimise retention strategies, and assess inclusivity within the workplace. By leveraging the power of clear and easy-to-understand visuals, I was able to present the insights within the datasets in a way that can support informed decision-making, highlight areas for improvement, and suggest avenues for innovation. In the end, this virtual case experience strengthened my ability to apply data analytics in a business context and also boosted my rather limited prior knowledge of Microsoft Power BI to a much more comfortable level.
 
  > **Note: To view and interact with these dashboards, Power BI Desktop is required.** <br>Download the `.pbix` files corresponding to each task and open them with Power BI Desktop. Although also given separately in this repository, the datasets are embedded in this dashboard files, so not additional setup is needed to explore the visualisations

  ### Call Centre Trends
  This first dashboard provides an in-depth analysis of call centre operations by highlighting key metrics such as average customer satisfaction (overall, by topic, and by agent), average call volumes over a day, and agent performance. By identifying trends and inefficiencies using these visuals, data-driven decision can be made to enhance service quality and operational efficiency.
  
  <img src = "PwC-Power-BI/Dashboard screenshots/Call_Centre_Trends_Analysis_1.png">
  
  ### Customer Retention
  Developed in response to a request from the telecom's Retention Manager, the second dashboard presents important insights into customer loyalty and retention. By visualising patterns in customer behaviour, it helps predict customer churn risk and suggests actionable strategies to improve retention.
  
  <img src = "PwC-Power-BI/Dashboard screenshots/Customer_Churn_and_Risk_Analysis_1.png">
  <img src = "PwC-Power-BI/Dashboard screenshots/Customer_Churn_and_Risk_Analysis_2.png">
  <img src = "PwC-Power-BI/Dashboard screenshots/Customer_Churn_and_Risk_Analysis_3.png">
  
  ### Diversity & Inclusion
  Finally, the third dashboard focuses on the telecom client’s objective of improving the gender balance at the executive management level. Therefore, the dashboard visualises metrics which highlight diversity and inclusion. Consequently, this brings attention to current trends in terms of representation at all levels throughout the company and also accentuatesareas which need improvement.
  
  <img src = "PwC-Power-BI/Dashboard screenshots/Diversity_and_Inclusion_1.png">
  <img src = "PwC-Power-BI/Dashboard screenshots/Diversity_and_Inclusion_2.png">
  <img src = "PwC-Power-BI/Dashboard screenshots/Diversity_and_Inclusion_3.png">
</details>
