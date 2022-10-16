Challenge 19
# Neural_Network_Charity_Analysis

## Overview of the analysis
The purpose of the project was to analyze Amazon reviews that were written by members of the paid Amazon Vine program. By means of the program, manufacturers and publishers will receive reviews regarding their products in exchange for paying a fee to Amazon and providing products to Amazon Vine members, who are required to write a review.

In the project, after a dataset is extracted that contains reviews of a certain product, it is transformed to determine whether there is any bias in the dataset toward favorable reviews from Vine members.


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
