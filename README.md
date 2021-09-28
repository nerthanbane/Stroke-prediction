<h1>stroke-prediction</h1>
Stroke infarct growth prediction (Jupyter)

<h2>Introduction<h2>
The main purpose of this notebook is to provide a comprehensive exploratory data analysis (EDA) for those wishing to quickly get a feel for the data and move on to modeling. I also tidy up the data set for those wishing to fork this notebook and use the cleaned data. The code for this EDA can be viewed by clicking the “Code” box next to the output, by selecting “Show all code” at the top right of this document, or by scrolling down to the full R markdown document at the bottom of the page.

<h2>DataSet</h2>
When building a predictive model one should look at the test set as little as possible, and ideally not at all, as to minimize the influence it has in the model building process. This practice best simulates building a model which is to be tested on previously unseen data. However, we must also make sure the entire data set is suitable for analysis prior to splitting, and that there were no data entry errors, inconsistencies in labeling, etc. Below I briefly examine the entire data set, tidy it up, then split it into training and testing sets. The following list details the changes:

One subject with Gender = “Unknown” was removed from the data
The ID column (unique identifiers for each subject) was removed
Added consistent capitalization
All feature names begin with a capital letter
Acronyms (such as BMI) are fully capitalized
All feature categories begin with a capital letter (ex: Yes, No)
BMI values of “N/A” were converted from character to an actual NA value
All categorical variables were recoded as labelled factors
The data were split 80/20 stratified by Stroke. The outcome (Stroke) is incredibly imbalanced in the data.



