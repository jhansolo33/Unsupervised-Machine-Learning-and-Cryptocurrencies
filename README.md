# Unsupervised-Machine-Learning-and-Cryptocurrencies

## Overview of the project
A large investment bank is interested in offering a new cryptocurrency investment portfolio for its customers. They have requested that our company create a report that includes cryptocurrencies that are on the trading market be grouped together to create a classification system for this new investment. We had to process the data to fit the machine learning models. Understanding there is no know output, we made the decision to use unsupervised learning. To group the cryptocurrencies, the decision to use clustering algorithm was established. To demonstrate our analysis, we will use data visualizations to share the findings with the board.

###  Three technical analysis and a written report covering:
Preprocessing the Data for PCA

Reducing Data Dimensions Using PCA

Clustering Cryptocurrencies Using K-means

Visualizing Cryptocurrencies Results

An Analysis Report and a proposal for further statistical study


###  Resources:
• Data Source: crypto_data.csv

• Data Tools: crypto_clustering_starter_code.ipynb.

• Software: Python, Visual Studio Code, Anaconda , Jupyter Notebook, Pandas

• Libraries: SKLearn/Scikit-learn, Pandas, Plotly, Maptplotlib, hvPlot

• Environment: Python 

• Unsupervised Machine Learning and Cryptocurrencies

• Using Unsupervised Learning to Discover Unknown Patterns

###  Step 1: Reprocessing the Data for PCA
####  Data Selection
Before moving data to our unsupervised algorithms, complete the following steps for preparing data to avoid any errors and to ensure we are getting the right results. Data selection entails making good choices about which data will be used. Consider what data is available, what data is missing, and what data can be removed. For example, say we have a dataset on city weather that consists of temperature, population, latitude and longitude, date, snowfall, and income. After looking through the columns, we can readily see that population and income data don't affect weather. We might also notice some rows are missing temperature data. In the data selection process, we would remove the population and income columns as well as any rows that don't record temperatures.

####  Data Processing
Data processing involves organizing the data by formatting, cleaning, and sampling it. In our dataset on city weather, if the date column has two different formats—mm-dd-yyyy (e.g., 01-23-1980) and month-data-year (e.g., jan-23-1980)—we would convert all dates to the same format.

####  Data Transformation
Data transformation entails transforming our data into a simpler format for storage and future use, such as a CSV, spreadsheet, or database file. Once our weather data is cleaned and processed, we would export the final version of the data as a CSV file for future analysis.

####  Requirements for a useable dataset are as follows:
• Null values and missing data: Unsupervised learning models can't handle null values or missing data. Drop null or missing values or decide and drop the entire column.

• Datatype: All data must be converted to numerical data type.

• Duplicates: Remove duplicates, they aren't telling us anything new and can skew the results.

• Scaled values: Data has been manipulated to ensure that the variance between the numbers won't skew the results. When features have different scales they can have disproportionate impact on the model. The unscaled value could lead to messy graphs. Therefore, it is important to understand when to scale and normalize data. For example, if four columns of data are single digits, and the fifth column is in the millions, we would need to scale the fifth column to align the other four columns.

##  Results:
Crypto DataFrame looks like the image below prior to the “get_dummies() method” to create variables for the two text features, using the “StandardScaler fit_transform()” function to standardize the features.
![Screenshot (A)](https://github.com/jhansolo33/Unsupervised-Machine-Learning-and-Cryptocurrencies/assets/119264589/d52efba5-a22c-4ad7-bb4b-ddcea0470705)

Result after the fit and transforming:

![Screenshot (B)](https://github.com/jhansolo33/Unsupervised-Machine-Learning-and-Cryptocurrencies/assets/119264589/cc5af10c-b74b-449f-b0a1-730279004e8e)

##    Step 2: Feature Elimination, Feature Extraction & Reducing Data Dimensions using PCA

Cluster DataFrame image:

![image(C)](https://github.com/jhansolo33/Unsupervised-Machine-Learning-and-Cryptocurrencies/assets/119264589/cbd9d90f-6f91-4b47-8f2b-69e920d1434e)

##  Step 3: Clustering Cryptocurrencies Using K-means and finding the Best Value using Elbow Curve

• Clustering is a type of unsupervised learning that groups data points together. K-means is an unsupervised learning algorithm used to identify and solve clustering issues. K represents how many clusters there will be. These clusters are then determined by the means of all the points that will belong to the cluster. The K-means algorithm groups the data into K clusters, where belonging to a cluster is based on some similarity or distance measure to a centroid. The centroid is found by taking the mean of all the x-values in the cluster, and the mean of all the y-values in a cluster. Elbow Curve is an easy method for determining the best number for K-means. To create the elbow curve, two values are needed - a list of K values and a list of inertia values. Loop through the 10 values for K, for example and determine the inertia: range (1, 11). • Inertia is one of the most common objective functions to use when creating an elbow curve. The inertia is measuring the amount of variation in the dataset. The inertia measuring the amount of variation in the dataset. Inertia is the objective function to plot K values against.

![Elbow Curve](https://github.com/jhansolo33/Unsupervised-Machine-Learning-and-Cryptocurrencies/assets/119264589/285c74f7-7850-4d78-adbd-e5892aaeb762)

##  Step 4: Visualizing Cryptocurrencies Results and Interpretation
• Visualizing the clusters helps to graphically understand how they are arranged.

• 3D graph and PCA visualization for 3D visualization we used 3D scatter plot with Plotly Express. Three principal components (on x, y, and z axis), that were created with PCA algorithm are plotted on the graph. These 3 components contains most of the information in the original large data set. As we can see the form of the graph, cryptocurrency is clustered in 4 groups with similar characteristics. When we hover over the specific element the graph shows label with Coin Name and its Algorithm.

• 2D visualization and correlation between Total Coins Supply and Total Coins Mined For 2D visualization I used hvPlot, a graphing library that allows deeper exploration of the data. This graph has Total Coins Supply on y-axis and Total Coins Mined on x-axis. From the graph we can see correlation between those two components. Different colors indicate different classes that crypto coins belong to. When we hover over the specific element the graph shows labels with Coin Name and its Class.


![hvplot_scatter](https://github.com/jhansolo33/Unsupervised-Machine-Learning-and-Cryptocurrencies/assets/119264589/b83f5d4a-6e64-4c47-a090-12dc9c90e492)

![image (F)](https://github.com/jhansolo33/Unsupervised-Machine-Learning-and-Cryptocurrencies/assets/119264589/83439bb5-505e-4fdb-b321-914db45802af)

