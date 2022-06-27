## Data Science Project Clustering : Airlines Customer Segmentation and Analysis Overview
* Build an Unsupervised Model to cluster and help segment Airlines customers in which what cluster / categories they fall into.
* Implementing K means algorithm as base clustering model with a various thresholds number of K / Cluster Number.
* Using An Airlines data, we analyze differents characteristics, provides specialized services for each respective customer categories , and formulate Corresponding marketing strategy.
* Customer segmentation plotting helps us gives better insight of how each customer clusters differ to one another.

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/667307.jpg) <br>
 
Customer segmentation is the process by which we divide our customers up based on common characteristics – such as demographics or behaviours, so you can market to those customers more effectively.These customer segmentation groups can also be used to begin discussions of building a marketing persona. Customer segmentation is typically used to inform a brand’s messaging, positioning and to improve how a business sells – so marketing personas need to be closely aligned to those customer segments in order to be effective.The marketing “persona” is by definition a personification of a customer segment, and it is not uncommon for businesses to create several personas to match their different customer segments.But for that to happen, a business needs a robust set of customer segments off of which to base it. Which leads us to the next section, distinguishing the difference between customer segmentation and market segmentation, so that the segmentation is as accurate as possible.

### Business Question:
* How is the customer divided / differ?
* What services best suit each customer categories, for a better customer retention for the company?

### Unsupervised Machine Learning Model Framework:
* Dataset Profiling
* Dataset Inspection, Missing values and anomaly values checking
* Dataset Cleaning, Handling the missing values and anomaly values
* Descriptive Statistic Plotting
* Pre processing Data
* K means model implementation

### Library and Resources Used:
* `Packages` : pandas, numpy, matplotlib, seaborn, sci-kit learn, pycaret.

### Dataset Profiling
![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-32-11%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

* Shape of Dataset consists of 62.988 observations and 23 features.
* With a total dimension size is 1448724.

### Features Types
![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-32-30%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

* There are 8 categorical features, notably Gender, Origin of Country, Workplace and Province to name a few.
* While for numerial features there are 15, Age of customers, Flight count, Total Points and Discount earned by the customers. <br>

### Dataset Inspection
* Dataset inspection suggests that there are a handful of missing values for a certain features. With Work Province and City having the most numbers of missing values, almost 6 percent of missing data out of total. <br>

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-32-48%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

* Aside from missing values as well, there are abnormal values in which certain values contains unnecessary symbol, also in work city / province features. We will consider this as missing values.

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-33-49%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

### Data Cleaning
* The step begins by first, cleaning the missing values. For categorical features, we can simply use siple imputer with `most-frequent` as the method. This will allow the missing values to e replaced by a values in which are most frequently occuring in that specific features. 
* Whilst for numerical ones, we can use also simple imputer however `median` will be the method we used to replaced missing values.
* Lastly for abnormal values, we are limited to only dropping the entire row.
* Cross checking missing values.

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-33-06%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

* Dataset has been cleaned.

### Descriptive Statistics
![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-34-26%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png)

* At a glance, we can see that, on average Customer's Fare Revenue on 1st Year and 2nd Year (SUM_YR1 & SUM_YR_2) are similar around 5300 to 5500.
* Total Fare Revenue 
* Customer's average interval from last flight to newly booked one are around 176 days.
* Average customer Total flight (by KM) is around 17128 km.

### Numerical Distribution
![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/index.png) <br>

* Quick look at the plot, majority of features are rightly skewed, while only 2 that are in what we called 'normal' sitribtuion. Notably Average Discount and Age of customers.

### Pre Processing Data
* Preparing data for unsupervised clustering model. With the help of pycaret built-in processing algorithm, we can simplifie the process. Here the parameters:

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-35-08%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

### K Mean Cluster Modeling and Evaluation
* First we make a default 4 different groups / cluster. AFter, we will evaluate the model performance using elbow method.
* The Elbow method is a heuristic used in determining the number of clusters in a data set. The method consists of plotting the explained variation as a function of the number of clusters, and picking the elbow of the curve as the number of clusters to use. The same method can be used to choose the number of parameters in other data-driven models, such as the number of principal components to describe a data set. 
* Elbow method provides us the means to evaluate K cluster and determine which clusters is the most optimum. For this dataset, the optimum is 5 clusters. 
* Build 2 different models, one with k = 4 and k = 5.

### Feature Selection / Parameters 
* The step is very necessary due to the amounts of features available. It is also worth noting that K means only accepts numerical features. 
* Correlation plot helps us determine fchosen features

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/Screenshot%202022-06-28%20at%2006-34-56%20Airflight%20Customer%20Segmentation%20and%20Analyis%20-%20Jupyter%20Notebook.png) <br>

* Features chosen for parameters are : Total Flight Count, Total KM, Total Fare Revenue, Average Interval and Last to End.

### Cluster Comparison using Radar Plot
![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/index4.png) <br>

From the plots we can infer:
* When the k is 4, we can clearly see the difference amongst each clusters, in terms of all the selected parameter features, Average Interval, Fare Revenue and DIstance between last flight and recent new booking. 4 clusters are very different, and are easily distinguishable.  
* While k is 5, is similar to the previous one, however the one newly added cluster is completely similar to the fourth cluster, and the clustering is slightly redundant. 
* So, 4 clusters is the best for this dataset. Further analysis on each cluster are follows.

### Cluster Analysis
* Cluster 1 consists of 1918 customers, the least of all clusters. This group of customers flew using the airlines services very frequently, evident by Total Fare revenue generated and total Flight attended are the highest, also distance KM traveled is the largest. Their average interval are also the lowest. They are the loyal value customers who needs to be well maintained.
* Cluster 2 consists of 28790, the most out all of clusters. Characterized by a low count of flight, fare revenue generated and low distance traveled. THe average iterval of flight booking is the highest of all. This gorup of people is the occasional / seeanal customer. They book flight on a occasion or during specific holiday season. For them, it to be mainatain as awell aside on top of stimulate consumptiton.
* Cluster 3 consists of 19255. This group of people is what we considered the lost customers. Characterised by the low count of amount of flight, distance traveled, and fare revenue generated. This group of customers have the longest last to end, meaning the last time they used the company's services is a long time since. Possibly, they had taken flight numerous times in the past, but then decided to stop using the services. For them, should try to grasp the latest information of these customers, maintain interaction with them, and adopt certain marketing methods like preferential measures and cross-selling to restore such customers. 
* Cluster 4 consists of 12983. Characterized by an average amount of all aspects and parameters. They are what we called the regular customer. They also need to be maintained and stimulate cnosummption albeit not to an extent like the previous cluster.

### Conclusion
* Cluster 1 are the loyal customers, they are those whoo needs to be maintained as best as possible.
* Cluster 2 are seasonal customers, in terms of number they are the most of all. Needs to be maintained and give stimulus consumption.
* Cluster 3 are the lost customers, they need further interaction and possibly certain market strategies to attarct them back using the services.
* Cluster 4 are the regular customer, like the previous ones, the also need stimulus consumoptions.
* Airlines conpany should take notes on 2nd cluster as they are likely to churn. By providing discounts at certain holidays seasos cnan help stimulate their consumption. 

