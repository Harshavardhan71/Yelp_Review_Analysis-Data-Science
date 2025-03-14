# **Yelp Restaurant Reviews Analysis**  

Source Data : https://www.kaggle.com/datasets/yelp-dataset/yelp-dataset

## **Project Overview**  
This project focuses on analyzing Yelp restaurant reviews to understand restaurant distribution, customer preferences, and sentiment trends. It involves **data cleaning, exploratory data analysis (EDA), and sentiment analysis using Support Vector Machine (SVM)** to identify the polarity of words in restaurant reviews.  

---

## **Project Components**  

### **1. Data Cleaning**  
The dataset consists of Yelp business and review data. The cleaning process includes:  
- **Loading Business Data:** Extracts restaurant details from Yelp’s dataset.  
- **Filtering U.S. Restaurants:** Ensures only businesses from the U.S. are included.  
- **Categorizing Restaurants by Cuisine:** Assigns each restaurant to a cuisine type (e.g., American, Italian, Chinese).  
- **Loading and Cleaning Review Data:** Processes user reviews by removing unwanted characters and structuring them properly.  
- **Merging Business and Review Data:** Connects restaurant information with corresponding user reviews.  
- **Sentiment Labeling:** Classifies reviews as **positive (≥4 stars) or negative (<3 stars)**, discarding neutral ones.  
- **Saving Processed Data:** Stores the cleaned dataset in a Parquet file for efficient handling.  

---

### **2. Exploratory Data Analysis (EDA)**  
This phase involves visualizing trends in restaurant distribution and customer reviews:  
- **Restaurant Distribution by Cuisine:** Identifies the most popular types of restaurants.  
- **Top 10 Cities with the Most Restaurants:** Highlights restaurant hotspots.  
- **State-Wise Restaurant Count:** Analyzes which states have the most dining establishments.  
- **Review Count by Cuisine Type:** Determines which cuisines generate the most customer feedback.  
- **Restaurant Ratings Distribution:** Examines how restaurants are rated on average.  
- **Most Reviewed Restaurants:** Identifies the top restaurants based on user engagement.  
- **Sentiment Trends by Cuisine:** Shows which cuisines receive more positive or negative reviews.  
- **Review Length Analysis:** Compares the average length of positive and negative reviews.  

---

### **3. Sentiment Analysis using SVM**  
To analyze sentiment polarity, this phase:  
- **Prepares Data for Sentiment Analysis:** Selects specific restaurant categories for evaluation.  
- **Cleans Review Text:** Processes review content by removing unnecessary characters.  
- **Identifies Important Words:** Extracts words strongly associated with positive or negative sentiment.  
- **Trains a Sentiment Classification Model:** Uses a Support Vector Machine (SVM) to determine polarity scores for words.  
- **Ranks Words by Sentiment Polarity:** Identifies the top positive and negative words influencing restaurant reviews.  
- **Visualizes Sentiment Trends:** Displays word impact on sentiment through bar charts.  

---

## **Installation & Requirements**  
### **Prerequisites**  
- Python 3.x  
- Required libraries: pandas, seaborn, matplotlib, scikit-learn, nltk, pyarrow, wordcloud  

---

## **Usage**  
1. **Data Cleaning:** Prepares restaurant and review data.  
2. **EDA:** Generates visual insights into restaurant distribution and customer sentiment.  
3. **Sentiment Analysis:** Identifies the most impactful words in restaurant reviews.  

---

## **Results & Insights**  
- Identifies the most common restaurant categories and their popularity across the U.S.  
- Highlights cities and states with the most restaurant activity.  
- Shows how different cuisines are perceived based on review sentiment.  
- Extracts key positive and negative words affecting restaurant ratings.  

---
## **Findings**
This analysis reveals key factors influencing restaurant reviews across different cuisine types.  

- **Positive Factors:**  
  - *Taste matters most:* "Delicious" is the top positive word for most restaurant types, suggesting that food quality influences ratings more than service or price.  
  - *Service over cost:* The word "friendly" ranks higher than "reasonable," meaning good service contributes more to high scores than affordability.  
  - *Freshness vs. flavor:* Customers value fresh ingredients more than just tastiness.  

- **Cuisine-Specific Insights:**  
  - *Vietnamese & Italian:* Freshness is a major positive factor.  
  - *French:* Sweet food gets good reviews, but for Korean cuisine, it leads to negative feedback.  
  - *Asian Restaurants (Korean, Japanese, Chinese, Thai):* Friendly service is highly appreciated, especially for Korean restaurants, where "attentive" ranks third.  
  - *Variety:* A key strength for Korean, Japanese, and Thai cuisine.  
  - *Japanese Cuisine:* Customers favor fun and creative dishes.  
  - *Italian Cuisine:* Classic Italian food is preferred.  
  - *French Cuisine:* Romantic ambiance and beautiful presentation lead to high scores.  

- **Negative Factors:**  
  - *Taste Issues:* "Bland" is a major complaint for Korean, Thai, and Vietnamese food, indicating an expectation for spiciness.  
  - *Temperature Problems:* Cold food results in low scores for French, Italian, and Japanese cuisine.  
  - *Ambience Issues:* Dark and crowded spaces affect Japanese restaurant ratings.  
  - *Service & Pricing:* Slow service is a major complaint for Korean and French restaurants, while French restaurants also receive negative feedback for high prices.  
  - *Greasy Food:* The main issue for Thai restaurants.  
  - *Sour Flavor:* A common complaint in Chinese cuisine.  

This analysis helps restaurant owners understand what drives positive and negative reviews. By analyzing customer feedback, they can improve food quality, service, and ambiance while also benchmarking against similar restaurants.
