# App_name_matching
Building a crosswalk which matches Apple apps to their Google Play counterparts. There is no simple solution, because the counterpart app sometimes differ in app_name and publisher_name.

Dataset 1 consists of 500 rows with columns [platform  app_id  app_name  publisher_name  categories],
Dataset 2 shows the matching pairs of Dataset 1. Dataset 3 is the test-dataset, with the same shape as Dataset 1,
for which the model will make predictions.

For the feature engineering part, i'm using fuzzywuzzy and spacy to get a similarity-score of the app_names and the publisher_names. I hardcoded the mapping of the categories.

I used a random forest with no special hyperparameter as prediction model.
