# Review Helpfulness Prediction using ML
 Helpfulness Prediction of Product Reviews Using Machine Learning. ( M. Tech. Dissertation of Kagolanu Trishul )

Customers express their opinion on products through reviews. Since there will be a lot of reviews that will be posted, only those reviews which are helpful to the customer need to be identified and should be accessible to the customer. Hence, helpfulness of review needs to be predicted. In this work, the helpfulness votes received by review is taken as a validator for helpfulness and this score is predicted. The features are divided into three categories namely reviewer features, review text features and review meta data features. Machine Learning is used for prediction of helpfulness using these features. The algorithms Linear Regression, Random Forests and Extreme Gradient Boosting are used for prediction and the problem is taken as a regression problem. It is observed that rating of a review has the highest influence on predicting helpfulness followed by user average rating deviation, difficult words and positive words. The work defines features such as stem sim length and lem sim length which are derived from the product description which also have performed reasonably well. Certain readability features of review text had high inter-feature correlation among themselves. In most of the cases Extreme Gradient Boosting showed the best performance. Using all the features with Extreme Gradient Boosting algorithm for prediction gave the best performance in automatically predicting helpfulness. The work also defines an Inter-feature Correlation Graph which helps in feature-set size reduction which in turn leads to optimization. The revised feature-set performed almost as good as the total features in predicting helpfulness. 

A Glimpse of the project can be seen in the file **Demo.ipynb**.

The Dissertation Report can be accessed in the file **DISSERTATION REPORT.pdf**.

### Data Collection
 * Amazon Reviews Data
 * Collected From : http://jmcauley.ucsd.edu/data/amazon
 * Reviews with atleaset 10 votes

Categorized the features into Reviewer, Review Text & Review Meta Data

Linear Regression, Random Forests, Extreme Gradient Boosting, XGBoost with customized Grid Search used for prediction

![image](https://user-images.githubusercontent.com/34864308/121798607-eebae400-cc44-11eb-9aaa-179fe58732ea.png)

### Features Extracted
![image](https://user-images.githubusercontent.com/34864308/121798628-10b46680-cc45-11eb-9a1f-1b317f794c33.png)

### Stem Sim Length and Lem Sim Length
These features measure the ability of the review to comment on the product or aspects of the product. Here, the goal is to find out to what extent the review talks about the product and its aspects. The first stage deals with the product description. The second stage deals with the review text.

![image](https://user-images.githubusercontent.com/34864308/121798721-802a5600-cc45-11eb-9e51-285885b06b36.png)
![image](https://user-images.githubusercontent.com/34864308/121798736-8fa99f00-cc45-11eb-8022-055767444db4.png)

The third stage deals with the comparison of the description and the review. Here, a set intersection is done between the stemmed words of review and the stemmed list of the corresponding product description. The length of this set is the feature stem sim length. Similar procedure is applied for lemmatized words and the feature lem sim length is also extracted.

### Inter-feature Correlation Graph
* It is a Graph with the features being the vertices. There will be an edge between two vertices (features) if the correlation between the features is greater than or equal to 0.8.

![image](https://user-images.githubusercontent.com/34864308/121798789-f929ad80-cc45-11eb-8c17-232a32d9ef59.png)

* No of Features after feature reduction : 13
![image](https://user-images.githubusercontent.com/34864308/121798859-50c81900-cc46-11eb-9abb-0e5a350365c8.png)
* Feature-set reduction : 38%



