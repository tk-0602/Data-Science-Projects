# Data-Science-Projects

This repository houses a collection of data science projects, demonstrating my skills and experience in applying data analysis, machine learning, and statistical techniques to a variety of situations, including real-world scenarios. Each of the projects in this repository highlight different aspects of the data science workflow, from data collection and preprocessing to model development and interpretation. These projects reflect my ability to extract meaningful insights from complex datasets and develop solutions that can drive business decisions.

<details>
<summary><h3>Sentiment Analysis of Airline Reviews</h3></summary>

This project is part of Forage's [British Airways Data Science](https://www.theforage.com/simulations/british-airways/data-science-yqoz) Virtual Experience Program.

<details>
<summary><h4>Task 1: Web Scraping and Sentiment Analysis</h4></summary>
This notebook is the first task of a two-part project aimed at predicting customer booking behaviours. Here, the focus is on collecting raw data and preparing it for analysis. Using web scraping techniques, the notebook extracts reviews from a public website, processes the data to ensure cleanliness and consistency, and prepares it for use in predictive modelling.

<break></break>

The extracted data was processed and analysed using natural language processing (NLP) techniques to perform sentiment analysis to provide valuable insights into customer satisfaction and experience with British Airways.

#### Key Features

- Web scraping using `BeautifulSoup` and `requests` libraries to extract review data from Skytrax - collected a substantial number of reviews (3500), iterating through multiple pages dynamically, and stored them in the `data-BA_reviews.csv` file which is also included here.
- Initial text preprocessing including trimming whitespace as well as removing HTML tags, special characters, and stopwords.
- Advanced data visualisation techniques using Matplotlib and Seaborn to present findings effectively as histograms and wordclouds (utilising the `wordcloud` library). 

#### Results

- Successfully scraped and cleaned a dataset containing reviews, bulding techniques and gaining experience for subsequent predictive analysis.
- Visualised sentiment distribution across various aspects of the airline service.
- Created wordclouds to highlight frequently mentioned positive and negative aspects.
- Demonstrated the feasibility of automating data collection from dynamic web pages.

#### Applications

In the context of this Virtal Experience Program:

- Enhance customer experience by addressing common pain points identified in negative reviews.
- Inform targeted marketing strategies based on positive aspects highlighted by customers.
- Present the ability to benchmark against competitors by comparing sentiment scores.

How this will add to my data analysis and data science experience:

- The web scraping techniques can be adapted to collect data from other domains, such as e-commerce, social media, or news sites.
- The cleaned and structured data produced from this can serve as input for text analysis, sentiment analysis, or predictive modelling in various contexts (e.g. to create and train an RNN for predicting the next word in similar reviews).

#### Future Improvements

- Implement advanced NLP techniques like topic modeling to automatically categorize review content.
- Develop an automated solution by extending the use of the `BeautifulSoup` library here as well as adding real-time sentiment monitoring to track changes in customer satisfaction on a more granular level.
- Integrate sentiment analysis results with other data sources (e.g. flight data and customer demographics) to provide more comprehensive insights
- Create an interactive dashboard for easy exploration of sentiment trends and patterns.

</details>

<details>
<summary><h4>Task 2: Predictive Modeling of Customer Bookings</h4></summary>
This notebook represents the second part of the project of understanding and predicting customer booking behaviours. It builds on the foundational data exploration conducted in Part 1 and implements machine learning solutions that address a specific predictive task: determining whether a customer will complete a booking.

#### Key Features

- Performed data cleaning and transformation, including handling missing values, feature engineering, and encoding categorical variables.
- Highlighted distributions and potential features in the data using bar graphs, boxplots, and kernel density estimate (KDE) plots scatter plots created with the `matplotlib` and `seaborn` libraries.
- Implemented supervised learning models using scikit-learn and conducted hyperparameter tuning via grid search to optimise model performance.
- Evaluated models using metrics such as accuracy, precision, recall, and F1 score.

#### Results
- The trained models successfully predicted customer booking outcomes with high accuracy (0.85 and 0.83 before and after hyperparameter optimisation, respecitvely).
- In between the two, XGBoost with hyperparameter optimisation made better predections as indicated by the models' F1 scores in particular where the initial model had an F1 score of 0.08 which then improved to 0.21 with hyperparameter optimisation. However, since this is still below 0.5, the model still had rather poor performance. This could perhaps be improved by creating more training data using data augmentation, further optimising the hyperparameters, or even using another model such as a Random Forest Classifier or simpler regression methods like Linear, Lasso, Ridge, etc. 
- Feature importance analysis identified critical factors influencing booking behaviour, namely `purchase_lead` (the number of days in between the date of booking and the date of the flight) and `length_of_stay`.

#### Applications

#### Future Improvements

</details>

</details>

<details>
<summary><h3>Customer Churn and Diversity Analysis in a Call Centre</h3></summary>

This project is part of Forage's [PwC Switzerland Power BI](https://www.theforage.com/simulations/pwc-ch/power-bi-cqxg) Virtual Experience Program.

</details>

<details>
<summary><h3>Anime Recommender</h3></summary>
A collaborative filtering-based recommendation system built using Cosine Similarity which is used to measure distance between two points as an alternative to (and animporvement on) the traditional Euclidean Distance measurement.
<br/><br/>

_Add equations of Euclidean Distance and Cosine Similarity_


Read more about this approach in this [Medium article](https://medium.com/@arjunprakash027/understanding-cosine-similarity-a-key-concept-in-data-science-72a0fcc57599)

</details>
