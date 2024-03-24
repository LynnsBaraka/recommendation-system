# Smart Retail Solutions Limited
![image](https://github.com/LynnsBaraka/recommendation-system/assets/143871178/731a2324-fef0-4372-b054-251a0d6f2545)

## Problem statement
A retail company aims to improve customer engagement and increase sales by implementing a Customer Segmentation & Recommendation System using Machine Learning (ML) techniques. The company wants to divide its customer base into distinct segments based on their purchasing behavior and preferences. 
Additionally, they want to develop a recommendation system that provides personalized product recommendations to customers within each segment.

## Objectives

* To segment customers into meaningful groups based on their purchasing behavior, and other relevant factors.
* To develop a recommendation system that suggests products tailored to the preferences and interests of each customer segment.
* To enhance customer experience and increase sales by providing targeted and personalized recommendations.
* To evaluate the performance of the segmentation and recommendation system through metrics such as customer engagement, conversion rates, and revenue growth.

By addressing this business problem, the retail company can leverage machine learning technology to segment its customer base, deliver personalized recommendations, and drive business growth through enhanced customer engagement and sales.

## Research questions
Through extensive analysis we were able to answer the following research questions:
* How can customer segmentation techniques (clustering algorithms) effectively divide the customer base into distinct segments?

* What are the characteristics and preferences of each customer segment, and how do they differ?

* How can User-based collaborative Filtering and Content based Filtering be integrated to provide more accurate and diverse recommendations to a customer?

* How can the recommendation system address the cold start problem for new users or items with limited interaction history?

## Procedure Overview:
### Data Preparation: 
Clean and preprocess the data, handling missing values, outliers, and inconsistencies. 
### Customer Segmentation:
Utilize K-means clustering algorithms to segment customers based on their purchasing behavior and 
preferences. Evaluate the clustering algorithms and determine the opƟmal number of segments using 
metrics such as silhoueƩe score or within-cluster sum of squares. 
### Recommendation System:
Develop a recommendation system that generates personalized product recommendations for each 
customer segment. Implement content-based filtering to suggest products tailored to individual 
preferences within each segment. 
### Model Evaluation:
Use evaluation metrics and techniques to assess the effectiveness, relevance, and impact of your 
recommendation system in providing personalized and engaging recommendations to users.

## Expectations of the Project
1. Improved Customer Engagement: The project aims to enhance customer engagement by 
providing personalized recommendations tailored to the preferences and interests of individual 
customers. 
2. Increased Sales and Revenue: The ultimate goal of the project is to drive business growth by 
increasing sales and revenue. By delivering targeted and relevant product recommendations, the 
expectation is to boost conversion rates and encourage repeat purchases, resulting in higher 
transaction volumes and increased revenue for the company.
3. Enhanced Customer Experience: The project seeks to improve the overall customer experience 
by delivering a personalized and seamless shopping experience. The expectation is to provide 
customers with relevant product recommendations that match their preferences and needs, 
leading to higher levels of satisfaction and loyalty.
4. Effective Customer Segmentation: The project aims to segment the customer base into 
meaningful groups based on their purchasing behavior and preferences. The expectation is to 
identify distinct customer segments with unique characteristics and preferences, allowing the 
company to offer recommendations that meet the needs of each segment. 

## Correlation Analysis
In the below image we Looking at the heatmap, we can see that there are some pairs of variables that have high correlations: 

![image](https://github.com/LynnsBaraka/recommendation-system/assets/143871178/09927434-3d6a-4049-bc9e-023ecf541d0d)
This high correlations indicate that these variables move closely together, implying a degree of multicollinearity.can see that

## Dimensionality Reduction(PCA)
In the below image the plot and the cumulative explained variance values indicate how much of the total variance in the dataset is captured by each principal component, as well as the cumulative variance explained by the first n components.

Here, we can observe that:

    The first component explains approximately 28% of the variance.

    The first two components together explain about 49% of the variance.

    The first three components explain approximately 61% of the variance, and so on.

To choose the optimal number of components, we generally look for a point where adding another component doesn't significantly increase the cumulative explained variance, often referred to as the "elbow point" in the curve.

From the plot, we can see that the increase in cumulative variance starts to slow down after the 6th component (which captures about 81% of the total variance).

Considering the context of customer segmentation, we want to retain a sufficient amount of information to identify distinct customer groups effectively. Therefore, retaining the first 6 components might be a balanced choice, as they together explain a substantial portion of the total variance while reducing the dimensionality of the dataset.ge we get to see 

![image](https://github.com/LynnsBaraka/recommendation-system/assets/143871178/f2a66e48-0e99-4d4b-9bf2-6abac79e53fe)


## K-Means Clustering

KMeans algorithm, I will set the init parameter to k-means++ and n_init to 10. To determine the optimal number of clusters, I will employ the elbow method and silhouette analysis. 
Additionally, it might be beneficial to explore the use of alternative clustering algorithms such as GMM and DBSCAN in future analyses to potentially enhance the segmentation results.
### Determination of the optimal number of clusters
## Elbow Method

Optimal k Value: Elbow Method Insights

The optimal value of k for the KMeans clustering algorithm can be found at the elbow point. Using the YellowBrick library for the Elbow method, we observe that the suggested optimal k value is 6. 
However, we don't have a very distinct elbow point in this case, which is common in real-world data. From the plot, we can see that the inertia continues to decrease significantly up to k=6, indicating that the optimum value of k could be between 4 and 8. 
To choose the best k within this range, we can employ the silhouette analysis, another cluster quality evaluation method. Additionally, incorporating business insights can help determine a practical k value.

![image](https://github.com/LynnsBaraka/recommendation-system/assets/143871178/bccd4756-aa02-4c3e-9618-bed4cb4e3afc)

## Clustering Evaluation
3D Visualization of Top Principal Components

![image](https://github.com/LynnsBaraka/recommendation-system/assets/143871178/dfca3a57-96b0-4005-90e9-64085af53c7a)


Cluster Analysis and Profiling
Using a Radar Chart Approach

![image](https://github.com/LynnsBaraka/recommendation-system/assets/143871178/e0b25492-15ca-4f74-b28b-4db5e24e1a8f)
* Cluster 0 has a high number of total transactions and total products purchased
* Cluster 1 has a high number of average days between purchases and days since last purchase.
* Cluster 2 has high number of the days of the week purchased. 


## RECOMMENDATION SYSTEM
### Based on Frequently bought products:
### Cluster 0 Recommendations:
1. JUMBO BAG RED RETROSPOT
2. WHITE HANGING HEART T-LIGHT HOLDER
3. LUNCH BAG RED RETROSPOT
4. REGENCY CAKESTAND 3 TIER
5. PARTY BUNTING
6. ASSORTED COLOUR BIRD ORNAMENT
7. SET OF 3 CAKE TINS PANTRY DESIGN 
8. LUNCH BAG  BLACK SKULL.
9. LUNCH BAG SUKI DESIGN 
10. LUNCH BAG SPACEBOY DESIGN 
### Cluster 1 Recommendations:
1. WHITE HANGING HEART T-LIGHT HOLDER
2. REGENCY CAKESTAND 3 TIER
3. ASSORTED COLOUR BIRD ORNAMENT
4. PARTY BUNTING
5. REX CASH+CARRY JUMBO SHOPPER
6. POSTAGE
7. JUMBO BAG RED RETROSPOT
8. NATURAL SLATE HEART CHALKBOARD 
9. PAPER CHAIN KIT 50'S CHRISTMAS 
10. HEART OF WICKER SMALL
### Cluster 2 Recommendations:
1. WHITE HANGING HEART T-LIGHT HOLDER
2. REGENCY CAKESTAND 3 TIER
3. ASSORTED COLOUR BIRD ORNAMENT
4. REX CASH+CARRY JUMBO SHOPPER
5. SET OF 3 CAKE TINS PANTRY DESIGN 
6. HEART OF WICKER SMALL
7. PARTY BUNTING
8. HEART OF WICKER LARGE
9. NATURAL SLATE HEART CHALKBOARD 
10. PAPER CHAIN KIT 50'S CHRISTMAS

## Adressing cold start
### Top Products Recommendations for Customers from the UK:
1. WHITE HANGING HEART T-LIGHT HOLDER
2. REGENCY CAKESTAND 3 TIER
3. PARTY BUNTING
4. ASSORTED COLOUR BIRD ORNAMENT
5. SET OF 3 CAKE TINS PANTRY DESIGN 
6. JUMBO BAG RED RETROSPOT
7. NATURAL SLATE HEART CHALKBOARD 
8. JAM MAKING SET WITH JARS
9. SET OF 6 SPICE TINS PANTRY DESIGN
10. PACK OF 72 RETROSPOT CAKE CASES
### Top Products Recommendations for Customers not from the UK:
1. POSTAGE
2. ROUND SNACK BOXES SET OF4 WOODLAND 
3. PLASTERS IN TIN CIRCUS PARADE 
4. ROUND SNACK BOXES SET OF 4 FRUITS 
5. REGENCY CAKESTAND 3 TIER
6. SPACEBOY LUNCH BOX 
7. PLASTERS IN TIN SPACEBOY
8. RED TOADSTOOL LED NIGHT LIGHT
9. PLASTERS IN TIN WOODLAND ANIMALS
10. LUNCH BAG WOODLAND
## Content based filtering - Recommendation based on items a user bought
###User 12353.0 bought the following item(s):
- NOVELTY BISCUITS CAKE STAND 3 TIER (Stock Code: 22890)
- MINI CAKE STAND WITH HANGING CAKES (Stock Code: 37446)
- CERAMIC CAKE STAND + HANGING CAKES (Stock Code: 37449)
- CERAMIC CAKE BOWL + HANGING CAKES (Stock Code: 37450)

### Recommendations for User 12353.0
1. SWEETHEART CERAMIC TRINKET BOX (Stock Code: 21231)
2. RED HANGING HEART T-LIGHT HOLDER (Stock Code: 21733)
3. HANGING HEART MIRROR DECORATION  (Stock Code: 22227)
4. MINI CAKE STAND T-LIGHT HOLDER (Stock Code: 22893)
5. ASSORTED COLOUR METAL CAT  (Stock Code: 84192)
## Conclusion
1. Effective Segmentation: The use of K-means clustering along with dimensionality reduction techniques like PCA proved effective in segmenting customers based on their purchasing behavior and preferences. The clustering identified a total of three segments.
2. Feature Engineering : The use of RFM(Recency, Frequency and Monentary) allowed us to establish customer behaviour and preferences.
3. Recommendation System: The developed recommendation system, based on frequently bought products within each cluster and other related items to what the ustomer bought, provides personalized recommendations tailored to the preferences of individual customer segments.
4. Cold Start: The Model used demographic information for initial recomendations for users who have not yet interacted with the system.
## Recommendations
1. Evaluation Metrics: Continuously monitor and evaluate the performance of the segmentation and recommendation system using relevant metrics such as customer engagement, conversion rates, and revenue growth.
2. Cold Start Problem: Address the cold start problem for new users or items with limited interaction history by asking for more personalised information about the users as they register on the system.
3. Feedback Mechanism: Implement a feedback mechanism to collect data on the effectiveness of recommendations and their purchases and use this feedback to continuously improve the recommendation system's performance.




