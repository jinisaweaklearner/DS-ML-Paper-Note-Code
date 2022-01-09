```
calculate the score
for user in users:
  for item in user_historical_items:
    get the (cosine) simialrity between target item and users' historical item one by one.
    get the rating as weights
    
score = totally sum of weighted simlarity / sum of weights  
```
- Item-Based Collaborative Filtering in Python https://towardsdatascience.com/item-based-collaborative-filtering-in-python-91f747200fab
- knn example https://github.com/KevinLiao159/MyDataSciencePortfolio/blob/master/movie_recommender/src/knn_recommender.py
