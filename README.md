## Data Science Project Clustering : Airlines Customer Segmentation and Analysis Overview
* Build an Unsupervised Model to cluster and help segment Airlines customers in which what cluster / categories they fall into.
* Implementing K means algorithm as base clustering model with a various thresholds number of K / Cluster Number.
* Using An Airlines data, we analyze differents characteristics, provides specialized services for each respective customer categories , and formulate Corresponding marketing strategy.
* Customer segmentation plotting helps us gives better insight of how each customer clusters differ to one another.
 
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

* Shape of Dataset consists of 62.988 observations and 23 features.
* With a total dimension size is 1448724.

### Features Types

* There are 8 categorical features, notably Gender, Origin of Country, Workplace and Province to name a few.
* While for numerial features there are 15, Age of customers, Flight count, Total Points and Discount earned by the customers.

### Dataset Inspection
* Dataset inspection suggests that there are a handful of missing values for a certain features. With Work Province and City having the most numbers of missing values, almost 6 percent of missing data out of total.
* Aside from missing values aswell, there are abnormal value, in which certain values contains unnecessary symbol, also in work city / province features. We will consider this as also a missing values.

### Data Cleaning
* 
