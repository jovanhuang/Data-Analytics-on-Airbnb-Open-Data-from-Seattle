# Formulated Problem
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
## Data formatting:
Convert dates to datetime format  
Remove ‘$’ and ‘,’ from price features and convert them to float  
Convert percentage based features to float  
Convert true/false features to boolean format  
Remove rows that do not have review data  
## Process features into readable inputs  
Convert "last_scraped" date to the number of months since last scraped  
One-hot encode "host_verifications" and "amenities" into a group of binary features  
Classify dates in "calendar_updated" into more generic categories  

# Further Data Wrangling
## Data Imputation
Used feature’s median values to fill null values
## Feature Selection
Excluded data IDs and URLs
