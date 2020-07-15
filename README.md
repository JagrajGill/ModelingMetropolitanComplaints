# Modeling Metropolitan Complaints

Introduction

The intent of this project was to create a predictive model of service complaints to optimize resource allocation in metropolitan settings. The motivation behind this undertaking
was rooted in curiosity as to how a major metropolis' non-emergency service system may be able to benefit -fiscally and through increased efficiency- via an AutoRegressive Integrated 
Moving Average (ARIMA) machine learning forecaster and simple time-series analysis. 

Method and Dataset

For this project, the New York City "311 Service Requests from 2010 to Present" dataset was used, which may be downloaded and referenced from the NYCOpenData Initiative here: 
https://nycopendata.socrata.com/en/Social-Services/311-Service-Requests-from-2010-to-Present/7ahn-ypff 

I have broken down the project into four separate exercises (Click to view code) :

1)[Determining the areas with the most issues](./BigIssueAreas.ipynb) ,

2)[Determining the most common type of complaints](./CommonComplaints.ipynb) ,

3)[Determining the common characteristics of the most frequent complaint](./CommonProperties.ipynb),

and,

4)[Predicting the frequency of future complaints](./PredictingFutureComplaints.ipynb)

Conclusion

Quantitatively New Yorkers in the Bronx are having issues with Hot Water in the Winter!

![picture](/Bar.png)
![picture](/Plot.png)

Using a Pearson Correlation Matrix, we explored what were some common characteristics of the complaints:

![picture](/Pearson.png)

We see that the most important features are :

BldgDepth: The depth of the structure or structures, which is the effective perpendicular distance.
ResidFAR: The maximum allowable residential floor area ratio.
NumFloors: The number of floors of the structure.
ZipCode: The specific zip code of the structure.

Here's our Q-Q plot and Seasonal ARIMA model:

![picture](/QQ.png)

We see that a normal distribution is followed from the histrogram and that the Normal QQ follows linearly also suggesting that the residuals follow the normal distribution.

![picture](/ARIMA.png)

An auto regressive model (ARIMA) may be used to predict future number of complaints, but the large confidence interval means that we can alter the parameters further that will allow us to better predict complaints that will arise further down the time series. It does provide sufficient prediction power as to allow for the department to prepare their resources to tackle upcoming issues.
