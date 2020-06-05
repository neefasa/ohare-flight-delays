# Classification Airline Delays

**Problem**   
Is there an underlying pattern to airline departure delays from flights leaving O'Hare International Airport?  

**Sources of Data**  
The first data source I used was from the [Bureau of Transportation Statistics](https://www.bts.gov/) website. This database contains a plethera of data on every flight passing through O'Hare, from airlines to reasons for delays. The data could be downloaded as CSVs, which I loaded into a Postrges server for easy retrieval.\
I also included weather data using  the [Dark Sky API](https://darksky.net/dev).  

**Modeling**  
The target for my model was whether a flight departed late. Specifically I defined this as leaving more than 5 minutes after the scheduled departure time. I tested several models, using the ROC AUC score to evaluate which model had the best preformance. This score is a quanitative way to evaluate the predictive power of the model. Scores range from 0.5 to 1. A score of 1 means the model make perfect predictions, while as score of 0.5 means the model is no better than a random guess. 
I settled on using Random Forest. From there I did some feature engineering to increase the preformance of the model.  
I ended with a model that had an accuracy of 74%.

