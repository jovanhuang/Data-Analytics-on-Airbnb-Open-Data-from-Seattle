# Formulated Problem
A notebook written to answer the question of what listings on AirBnb are worh it. Rather than focus on utilising CatBoost for predictive modeling, we used CatBoost to gain an intuition of the factors which might affect the value of listings.  

What makes an Airbnb listing worth it?
# Secondary problems:
What features apart from price and reviews make an apartment "worth it"?  
How can we quantify "worth" in an accurate manner?  
Can we determine if a listing is "worth it" without looking at price?  
Does the presence of certain amenities correlate with review scores?  
# Our approach
Whether a listing is “worth it” is determined using a new feature: “value”  
  
We defined “value” as: review_scores_rating/price  

# Initial preparation of dataset
### Data formatting:
Convert dates to datetime format  
Remove ‘$’ and ‘,’ from price features and convert them to float  
Convert percentage based features to float  
Convert true/false features to boolean format  
Remove rows that do not have review data  
### Process features into readable inputs  
Convert "last_scraped" date to the number of months since last scraped  
One-hot encode "host_verifications" and "amenities" into a group of binary features  
Classify dates in "calendar_updated" into more generic categories  

# Further Data Wrangling
### Data Imputation
Used feature’s median values to fill null values
### Feature Selection
Excluded data IDs and URLs

# Exploratory Data Analysis (EDA) 
Review Score’s Analysis  
Neighbourhood Analysis  
Host Analysis  
Listing Property Analysis  
(Refer to jupyter notebook for more info)

# Assumption and Biases
### Assumptions:
The concept of value can be assessed by considering only price and review ratings.  
The distribution from the dataset is representative of the population.  
Listings are informative enough.  
### Biases:
Features like room types and fees drive prices up.  
Certain neighbourhoods have higher natural prices.  
Components of reviews score are biased, causing the rating scores to be biased.  

# Machine Learning Models used
Model 1: Classification Decision Tree  
Model 2: Logistic Regression  
Model 3: K-Nearest-Neighbour   
Extra Model: Feed-forward Neural Network  
Model 4: Gradient-boosted decision tree  

Used F1-Score to evaluate the models  

# What we learnt
Statistics: Bayesian Bootstrap, F1-Score   
Visualisation: Tableau, Plotly, Seaborn, Matplotlib  
Data Wrangling: Median-Imputation, One-hot encoding, Feature-Crossing  
Machine Learning: GB Trees, Recursive Feature Elimination, Deep learning  
Machine Learning Tools: sklearn, keras, catboost  
Techniques: k-fold CV, NLP, GridsearchCV  

# Conclusion
Model performance > High likelihood that we missed out other important features  
Study done by Carnegie Mellon University concluded that high quality images increased annual revenue by ~ $2000  
Did not include sentiment analysis from text reviews  
NLP data was too small  
Reviews were skewed positively  
Extracted sufficient information to inform consumers of things to look out for other than price/ reviews  


