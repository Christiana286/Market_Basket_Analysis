## Market_Basket_Analysis with Apriori

# Overview
Market Basket Analysis or MBA targets buying patterns of items. Going through sales transactions over time for a business, MBA answers the question of 'what are the likely items customers would purchase together in a set when they come in the store?'

![image](https://github.com/Christiana286/Market_Basket_Analysis/assets/139984557/b42474d5-2500-44aa-8a88-effe83121c3c)

# Problem Statement
The introduction of MBA is to provide business optimisation for the grocery store by finding associations between the product items on sale and promote cross selling between them. Cross selling is a marketing tactic used to improve sales by offering the customer itemsets that complement or are compatible with each other.

# Data Preparation
The data for this project was prepared for analysis by a number of steps;
- Loading the Python libraries required
- Exploring the data information to understand the object types as well as checking for null values if any
- Conversion of 2 nos columns data types from integer/object to string

# Pre-Processing
The data was further processed by the addition of a new column 'uniqueTransaction' to group customer transactions after which the frequency of each purchases / transactions was computed using 'cross tabulation'.

# Introducing the Apriori algorithm
To enable analysis of the 'Basket' created from the cross tabulation, the dataset was transformed with 'binary encoding' into a sequence of 'ones' and 'zeroes'. This encoding is used in the implementation of the Apriori algorithm. The Apriori engaged the metric of minimum support at 0.005% to filter the frequently purchased itemsets for useful 'association rules'; a sort of mining process.

# Evaluation, Visualisation and Recommendations
For the purpose of this project, another association rules measure, the 'zhangs_metric' was used for sorting and evaluation of the purchased itemsets. This measure or metric assesses the strength of association of the 'antecedent' and 'consequent' items, both positive and negative.
A heatmap is used for visualisation, showing the items associations in varying color intensity. All of the zhangs' measures with positive values after sorting have the higher intensity confirming the positive associations for those itemsets when purchased together. This informs the recommendations for items pairings made to the grocery store.
