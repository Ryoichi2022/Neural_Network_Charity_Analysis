Challenge 19
# Neural_Network_Charity_Analysis

## Overview of the analysis

### i. Project purpose
A nonprofit foundation, Alphabet Soup, has raised and donated over 10 billion dollars in the past 20 years to invest in lifesaving technologies and organize reforestation groups. The foundation needs analysis to ensure that its money is being used effectively. To meet this need, a deep learning neural network will be designed and trained through the project.

### ii. Dataset received for analysis
The dataset contains more than 34,000 organizations that have received funding from Alphabet Soup and captures the following data about organizations:\
**EIN and NAME** - Identification columns\
**APPLICATION_TYPE** - Alphabet Soup application type
AFFILIATION - Affiliated sector of industry
CLASSIFICATION - Government organization classification
USE_CASE - Use case for funding
ORGANIZATION - Organization type
STATUS - Active status
INCOME_AMT - Income classification
SPECIAL_CONSIDERATIONS - Special consideration for application
ASK_AMT - Funding amount requested
IS_SUCCESSFUL - Was the money used effectively


## Results

### Data transformation procedure
The analysis was conducted over the dataset of book reviews (amazon_reviews_us_Books_v1_02.tsv.gz), which included 3,105,520 reviews in total. Among all reviews, only two were written through the Amazon Vine program.

Out of the original dataset, the following columns were selected to create a new dataset (Table 1) for further analysis: review_id, star_rating, helpful_votes, total_votes, vine, and verified_purchase. Then, only reviews with 20 or more total votes were retrieved, and percentage of helpful votes to total votes was calculated for each of these reviews.

(Table 1) New dataset with selected columns

<img src="https://github.com/Ryoichi2022/Amazon_Vine_Analysis/blob/main/New_dataset.png" width="600"/>

### Number of Vine and non-Vine reviews
There were 501,609 reviews with 20 or more votes, and all of them were non-Vine reviews. Although two reviews were written by the Vine program members, they received less than 20 total votes and were excluded from the analyzed dataset.

### 5-Star Vine reviews
As described above, no Vine reviews were available in the analyzed dataset.

### 5-Star non-Vine reviews
403,807 out of 501,609 reviews gained 50% or more helpful votes and were considered helpful by customers. As shown in Table 2, 242,889 or approximately 60% of the helpful reviews rated products with five stars.

(Table 2) Summary of non-Vine reviews

<img src="https://github.com/Ryoichi2022/Amazon_Vine_Analysis/blob/main/Unpaid_review_summary.png" width="800"/>

## Summary

### Positivity bias in Vine reviews
In conclusion, it would not appropriate to determine whether or not there is a positivity bias for reviews in the Vine program based on the dataset without Vine reviews. However, a further review of the dataset indicates a remarkable gap in the percentage of 5-Star reviews between helpful reviews and others (Table 3).

(Table 3) Summary of 5-Star reviews

<img src="https://github.com/Ryoichi2022/Amazon_Vine_Analysis/blob/main/Five_star_summary.png" width="800"/>

### Potential of further analysis
Other datasets could be extracted than book reviews to examine Vine reviews for positivity bias. In addition, by grouping datasets by number of stars and focusing on 5-Star reviews, it could be determined whether they are likely to receive a helpful vote from customers.
