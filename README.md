# product_match
Matching is the task of searching and pairing two objects from different datasets. 
New batches of products with slight variations in characteristics are added to the inventory, technically treated as entirely new items but essentially the same as products already on the marketplace.
# task
Develop an algorithm that for all items in validation.csv, suggests several options for the most similar items from the base dataset.
Evaluate the algorithm's performance using the accuracy@5 metric
# Data: Source

base.csv: An anonymized set of products, each represented by a unique id (0-base, 1-base, 2-base) and a 72-dimensional feature vector.
train.csv: Training dataset where each row corresponds to a product, known by a unique id (0-query, 1-query, …), a feature vector, and the id of the product from base.csv that is deemed most similar to it.
validation.csv: Dataset containing products (unique id and feature vector) for which the most similar products from base.csv need to be identified.
validation_answer.csv: Correct answers for the previous file.

# Conclusion

Despite persistent challenges in the kernel environment, including potential issues with Faiss and kernel stability, the code can be used for data preprocessing, scaling, and building an index for nearest neighbor search. The intention is to deploy this code on Kaggle, where it may encounter a more stable and supportive environment.

The analysis on the initial dataset reveals a robust structure with well-handled data types, no missing values, and an absence of outliers or anomalies. However there are certain imbalances in certain feature values, potentially impacting the model's performance (i.e. feature #25).

