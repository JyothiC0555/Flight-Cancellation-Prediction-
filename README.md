# Flight-Cancellation-Prediction-
Flight cancellations and delays are becoming a serious concern since they result in resource inefficiency, increased expenditures, and disruptions in passengers travel arrangements, all of which lead to consumer dissatisfaction. To tackle this, we'll use the "flights.csv" dataset to discover what variables influence flight cancellations.
#

<p align="center">
  Team Members  <br>
  <strong> Jyothi Chandrakanth </strong> <br>
  <strong> Eknath Chunduri  </strong> <br>
  <strong> Pavan Kumar  </strong>
</p>

<p align="center">
College of Professional Studies, Northeastern University <br>
  ALY6110: Data Management and Big Data

</p>

<p align="center">
  <strong> Introduction </strong> 
</p>

<p align="justify">Flights spend less time on the road when commuting. Flight cancellations and delays are becoming a serious concern since they result in resource inefficiency, increased expenditures, and disruptions in passengers travel arrangements, all of which lead to consumer dissatisfaction. According to Lukacs, the US government lost 33.0 billion dollars in 2019 due to airline cancellations and delays (2019). Cancelled flights and delays are caused by a variety of circumstances including weather, security, and technical faults with the aircraft. If airlines do not provide quality service, that has an impact on their image in the aviation business. To tackle this, we&#39;ll use the &quot;flights.csv&quot; dataset to discover what variables influence flight cancellations.

<p align="justify">Technology is radically altering how organizations communicate with their consumers, make business decisions, and create workflows. Airlines are transforming their activities from pre-flight through post-flight, including booking, extra legroom, luggage, boarding, and transportation services, with the use of data. Big data analytics&#39; ultimate benefits include quicker reactions to current and future market needs, enhanced planning and closely aligned decision making, and crystal-clear grasp and monitoring among all major performance drivers relevant to the aviation business. Unplanned maintenance accounts for over 30% of total time delay; airlines suffer large expenditures owing to delays and cancellations, which include maintenance costs and compensation for travelers detained at airports.

<p align="justify">In Data Analysis, Machine Learning, and Data Science, cluster analysis has become one of the most essential methodologies. Clustering is a technique that divides a collection of items with similar characteristics into groupings called clusters. Since the dataset which we have is imbalanced in nature we will be utilizing Random Forest and Decision Tree, classification algorithms to predict the factors affecting the cancellation of flights.

<p align="center"> 
  <strong> Exploratory Data Analysis  </strong> 
  
**Data Cleaning**
<p align="justify">During the data cleaning procedure, we identified all variables with missing values and the percentage associated with them. The variables with more than 25% missing values were eliminated, while the ones with fewer missing values were imputed with the mean of the variable.

<p align="justify">We are trying to answer the below questions to achieve the goal of the assignment.

1. The trends of cancellation based on day of the week and the month

2. Delays Caused due to various factors

<p align="justify">To perform Exploratory Data Analysis, we have extensively used Tableau and produced the below graphs to address the objective of the project.

We performed initial analysis that shows the delays and the cancelation trends

Determining the airtime of each flight
<p align="justify">We have tried to identify the airtime for each flight to and converted them into hours for better understanding. Southwest (WN) has the highest airtime followed by American Airlines (AA) and Delta Airlines (DL). The least amount of airtime was found for Empire Airlines (EM) and Peninsula Airways (KS).

<p align="justify">Southwest (WN) and American Airlines (AA) have the highest airtime and the highest cancellation of flights. Although Envoy Air (MQ) has flown for lesser duration when compared the Southwest and American Airlines.

<p align="justify">The report contains the cancellation trend for each month, The cancellation is high at the beginning of the year. January, February and April have the greatest number of cancellation, October and November months have the least cancellation.


<p align="justify">The The report contains cancellation trend based on day of the week. Tuesday and Sunday have the maximum number of cancellation while Friday and Thursday have the minimum cancellation.

<p align="justify">Delays that are under the control of the National Airspace System (NAS), such as non-extreme weather conditions, airport operations, heavy traffic volume, air traffic control, and so on, are shown in the graph below. United Airlines is the carrier with the most NAS delay, followed by American Airlines.


<p align="justify">Security delays caused by evacuation of a terminal or concourse, re-boarding of aircraft due to a security breach, malfunctioning screening equipment, and/or long waits at screening areas are depicted in the graph above. Southwest Airlines is the airline with the longest security delays, followed by American Airlines.


<p align="justify">The report contains the  delay due to various weather conditions. The arrival delay at an airport caused due to the late arrival of the same aircraft at a former airport is depicted in the graph below. Southwest Airlines is the airline with the latest arrivals, followed by American Airlines.

<p align="center"> 
   <strong> Data Modeling </strong> 

<p align="justify">Because the data we have is imbalanced, we decided to utilize Random Forest and Decision Tree to model the data and find the factors that are significant in causing the flight cancellations in the dataset. &quot;CANCELLED&quot; was used as a predictor variable, while all other factors were used as outcome variables. We excluded the variables that are associated with delays because our goal is to forecast flight cancellations, not delays.

1. **Random Forest**

<p align="justify">We have split the dataset into train and test with a ratio of 70:30 and fit the model and then transformed all the variables to numerical values for faster computation.

The confusion Matrix obtained for the Random Forest Model is shown in the report 

The Accuracy, Recall, Precision and F1 score for the Model is shown in the report 

2. **Decision Tree**

We have fit the model using Decision Tree Classifier

The confusion matrix obtained for the decision tree model shown in the report 

The Accuracy, Recall, Precision and F1 score for the Model is shown in the report 

Decision Tree Plot shown in the report 

<p align="center"> 
   <strong> Model Comparison </strong>

<p align="justify">Based on the confusion matrix, we may conclude that the decision tree outperformed the random forest. Despite the fact that both models have high accuracy, the decision tree model was able to forecast False Positive and False Negative those accounts equal to 0, eliminating Type I and Type II errors. Hence Decision Tree model can be used to forecast the cancellation of flights.

<p align="center"> 
   <strong> Recommendation  </strong>

<p align="justify">The most significant factors that contribute to flight cancellations, as indicated in the above feature selection plot obtained by running the Decision Tree, are _Arrival Time_ and _Diverted_. To reduce passenger flight cancellations, the aviation industry must emphasize on these factors in order to boost revenue and improve customer satisfaction.

<p align="center"> 
   <strong> Conclusion </strong>

<p align="justify">The analysis on the &#39;_flights&#39;_ dataset was performed using python and Tableau. The exploratory data analysis using Tableau gave us insights on the patterns of the cancellations, we were able to identify the airlines that flew most frequently, the airlines that has the maximum number of delays and determined top five airlines with the maximum amount of cancellation. Python was used for cleansing the data, for data imputation of data and to identify missing values. Furthermore, we leveraged python for modeling. We used Random Forest and Decision Tree to predict the factors that affected the cancellation of the flights. A

**References**

Yanying, Y., Mo, H., &amp; Haifeng, L. (2019, December 31). _A classification prediction analysis of flight cancellation based on Spark_. Procedia Computer Science. Retrieved December 13, 2021, from https://www.sciencedirect.com/science/article/pii/S1877050919320241.

_(PDF) Flight Delay Prediction based on Deep Learning and ..._ (n.d.). Retrieved December 13, 2021, from https://www.researchgate.net/publication/346539839\_Flight\_delay\_prediction\_based\_on\_deep\_learning\_and\_Levenberg-Marquart\_algorithm.

_Secondary navigation_. Aviation Data &amp; Statistics. (2021, April 12). Retrieved December 13, 2021, from https://www.faa.gov/data\_research/aviation\_data\_statistics/.

Pathak, P. P. (2021, July 18). _Decision trees and random forests - explained with python implementation._ Medium. Retrieved December 19, 2021, from https://towardsdatascience.com/decision-trees-and-random-forests-explained-with-python-implementation-e5ede021a000
