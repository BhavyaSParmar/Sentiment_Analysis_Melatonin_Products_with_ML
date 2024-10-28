# Sentiment_Analysis_Melatonin_Products_with_ML
Here's a breakdown of what this code is doing:

### Data Preparation and Merging
1. **Libraries Installation and Import**: Installs necessary libraries (`TextBlob`, `WordCloud`, `plotly`, etc.) and imports essential data manipulation and visualization libraries (`pandas`, `numpy`, `matplotlib`, etc.).
2. **CSV File Reading and Merging**: Loads multiple CSV files containing melatonin product reviews and merges them into a single dataframe called `merge_df`.
3. **Data Cleaning**:
   - Checks for missing values and removes rows where the "review_text" or "dose" is missing.
   - Extracts the dose information from the product titles and stores it in a new column called "dose".

### Sentiment Analysis
4. **Sentiment Calculation**: Uses the `TextBlob` library to calculate the sentiment polarity of each review in the "review_text" column and stores the result in a new column named "sentiment".
5. **Mapping Ratings to Sentiment Categories**: Converts numerical review ratings into sentiment categories like "Favorable," "Moderate," or "Unfavorable" based on the review rating values.

### Visualization
6. **Interactive Bubble Plot**: Plots an interactive bubble chart using `plotly` to show the relationship between dose and sentiment. The bubble size represents the count of each dose.
7. **Count Plot by Dose**: Plots a count plot using `seaborn` to visualize the distribution of different doses based on their sentiment category.
8. **3D Scatter Plot**: Visualizes a 3D scatter plot using `plotly` to display the relationship between average rating, sentiment polarity, and dose.
9. **Violin Plot**: Displays a violin plot to show the distribution of sentiment polarity for each dose category.

### Text Processing and TF-IDF Analysis
10. **Text Preprocessing**: Preprocesses review text by tokenizing and removing stopwords using NLTK. Converts the text to a filtered version containing only significant words.
11. **TF-IDF Vectorization**: Transforms the cleaned review text into numerical vectors using `TfidfVectorizer`, which measures the importance of words in the context of all reviews.
12. **Word Cloud**: Creates a word cloud to visualize the most frequent words appearing in all reviews.
13. **Correlation Matrix**: Displays an interactive correlation matrix to explore the relationships between different words in the TF-IDF vectors.

### Exploratory Data Analysis (EDA)
14. **Histplot of Dose Distribution**: Uses a histogram to display the distribution of different doses present in the dataset.
15. **Top Occurring Words Bar Plot**: Plots the 29 most occurring words using a custom color palette.

### Building Machine Learning Models
16. **Data Splitting**: Splits the preprocessed dataset into training and testing sets using `train_test_split`.
17. **Feature Extraction and Transformation**: Applies TF-IDF vectorization and scaling to the text and numerical features. Combines the extracted features with additional columns like average ratings and review ratings.
18. **Logistic Regression Model**: 
   - Fits a logistic regression model on the training data.
   - Evaluates its accuracy and prints the classification report on the test set.
19. **Random Forest Classifier**:
   - Trains a Random Forest Classifier with 200 trees and evaluates its accuracy and classification report on the test set.
    
- The code processes and analyzes product review data related to melatonin supplements. It uses text-based sentiment analysis and creates several visualizations to understand the relationships between review sentiment, doses, and ratings.
- Additionally, the code leverages machine learning algorithms (Logistic Regression and Random Forest) to predict doses based on review text, ratings, and sentiment features.
- The emphasis on visualizations like bubble charts, 3D plots, and violin plots adds more exploratory insights to the sentiment and dose-related trends.

This project combines various aspects of data science, including data cleaning, exploratory data analysis, sentiment analysis, feature engineering, and machine learning, making it a comprehensive analysis on sentiment in product reviews.
