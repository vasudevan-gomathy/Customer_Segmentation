# ***Customer_Segmentation***

## **Problem Statement**

As an e-commerce platform, it is very important to profile your customers, dividing your clientele base into groups based on their needs and expectations. Grouping will help us come up with dedicated marketing strategies and will aid us in recommending products to different user bases. In this project, we are interested in analyzing the content of an E-commerce database that lists purchases made by ∼4000 customers over a period of one year (1/12/2010 to 9/12/2011). Based on this analysis, we would like to develop models to group the 4000 customers into different buckets. Such a model must take into account the similarity between the products purchased between the users (i.e. a user might purchase 2 different products which are very similar to each other), the spending patterns of a user, their meta information, etc.

## **Dataset**

**Data**

The customer segments data is included as a selection of app. 4000 data points collected on data found from an E-Commerce database, which was gotton from UCI Machine Learning Repository. You use this data in your local machine, you have to clone and unzip the data.csv file from this Repo.

**Features**

This dataframe contains 8 variables that correspond to:

* InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.

* StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.

* Description: Product (item) name. Nominal.

* Quantity: The quantities of each product (item) per transaction. Numeric.

* InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.

* UnitPrice: Unit price. Numeric, Product price per unit in sterling.

* CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.

* Country: Country name. Nominal, the name of the country where each customer resides.

**Dataframe**

![image](https://user-images.githubusercontent.com/85822284/209568412-63d80329-2001-47a9-b483-2a850542637d.png)



## **NLP Pipeline**

(1) Cleaning Text (Removing Characters other than Alphabets

(2) Converting text into Lower case

(3) Removing Stop Words

(4) Lemmitization

(5) Bag of words

## **Clustering**

Using K - Means cluster for segmenting the customers based on product description and used PCA (Principle Component Analysis) for dimensionality reduction.

### K-Means

K-Means Clustering is an Unsupervised Learning algorithm, which groups the unlabeled dataset into different clusters. Here K defines the number of pre-defined clusters that need to be created in the process, as if K=2, there will be two clusters, and for K=3, there will be three clusters, and so on. It allows us to cluster the data into different groups and a convenient way to discover the categories of groups in the unlabeled dataset on its own without the need for any training.

It is a centroid-based algorithm, where each cluster is associated with a centroid. The main aim of this algorithm is to minimize the sum of distances between the data point and their corresponding clusters. The algorithm takes the unlabeled dataset as input, divides the dataset into k-number of clusters, and repeats the process until it does not find the best clusters. The value of k should be predetermined in this algorithm.

The k-means clustering algorithm mainly performs two tasks:

* Determines the best value for K center points or centroids by an iterative process.
* Assigns each data point to its closest k-center. Those data points which are near to the particular k-center, create a cluster.

### PCA

Principal Component Analysis is an unsupervised learning algorithm that is used for the dimensionality reduction in machine learning. It is a statistical process that converts the observations of correlated features into a set of linearly uncorrelated features with the help of orthogonal transformation. These new transformed features are called the Principal Components. It is one of the popular tools that is used for exploratory data analysis and predictive modeling. It is a technique to draw strong patterns from the given dataset by reducing the variances.

PCA generally tries to find the lower-dimensional surface to project the high-dimensional data.

PCA works by considering the variance of each attribute because the high attribute shows the good split between the classes, and hence it reduces the dimensionality. Some real-world applications of PCA are image processing, movie recommendation system, optimizing the power allocation in various communication channels. It is a feature extraction technique, so it contains the important variables and drops the least important variable.

## **Data Exploration**

Getting the Centroids

![image](https://user-images.githubusercontent.com/85822284/209568986-734ed24f-ba32-499c-91c6-aa9795ac6a4c.png)


**Elbow Plot**

Used Elbow plot for hyperparameter tunning i.e. for finding the value of K. With the help of below elbow plot, I finalised the value of k = 4.

![image](https://user-images.githubusercontent.com/85822284/209569011-cff07b5d-cc92-4b0f-a15e-d22eac2d787a.png)

## ***Conclusion***

![image](https://user-images.githubusercontent.com/85822284/209569232-b9e8c338-a41e-40c9-813b-68b0d9d117d0.png)

From the above graph Customer Cluster 3 is having the maximum number of Customers and cluster 2 has the minimum number of customers.
