# British_Airlines_Customer_Reviews_Analysis
## Getting Started
### Web scraping and analysis

This Jupyter notebook includes some code to get you started with web scraping. We will use a package called `BeautifulSoup` to collect the data from the web. Once you've collected your data and saved it into a local `.csv` file you should start with your analysis.

#### Scraping Review Data from Skytrax

If you visit [https://www.airlinequality.com] you can see that there is a lot of data there. For this task, we are only interested in reviews related to British Airways and the Airline itself.

If you navigate to this link: [https://www.airlinequality.com/airline-reviews/british-airways] you will see this data. Now, we can use `Python` and `BeautifulSoup` to collect all the links to the reviews and then to collect the text data on each of the individual review links.

#### First of all, we scrap Review data from Skytrax. 
Then we scrap the `Route` data and then the `Seat Type`, some `Numerical` data and `Score` data from the website.

Finally, we save it as `BA_DataSet.csv`.

## Analyze
### Organizing Data

* First of all, we separate `Approval_Status` and `Review`.
* We remove unwanted parts from `Approval_Status`. 

### Data Analysis 1 - Review Analysis - Good/Bad/Neutral Discrimination

We analyze sentiment using the `TextBlob` library and look at its distribution in the graph.

![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/667d77dd-affe-40eb-8024-e311e4df7bab)

### Data Analysis 2 - Route Analysis - From/To

* According to the `to` we divide the routes into `From` and `To`. 
* According to `via` we separate `Transfer` data.
* To avoid complexity in the `From` and `To` columns, we reduce data that may represent the same thing to one data.
* We look at which data is redundant and support it with a graph.

![output](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/f8e553f1-e260-4db3-a94d-93f04010d901)
![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/b6f0c3e2-33a3-45b8-b4c4-a01bc568d55c)
![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/e672674b-87b7-4c5f-aa9b-781da29cd4fc)


### Data Analysis 3 - Seat Type Analysis

Graphing how much the `Seat_Type` data is.

![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/17cd9432-ef9a-4686-b7e9-aa31d1507f53)


### Data Analysis 4 - Correlation Analysis

We examine the correlation of `Numerical` data with `Score`. Then we also examine the correlation between them.

![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/88cc166a-60d0-4de5-a553-c41759e8c9f7)


### Data Analysis 5 - Seat_Type and Review_Type Charts

* Visualization of the average `Score` data according to `Seat_Type` and `Review_Type` data with a graph.
* Examine how many of which data according to `Review_Type` and `Seat_Type`. 
* Then examining its relationship with other `Numerical` data.

![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/e7181fda-25c4-4121-bc67-f3eaebbb1a70)
![image](https://github.com/TolgaKilinckaya/British_Arilines_CustomerReviews_Analysis/assets/119072606/bd5cdfca-c143-47ee-9173-67aedce9fb2f)


### Saving The Clean DataSet

Finally, we save it as `BA_Clean_DataSet.csv`.

## Score Prediction
