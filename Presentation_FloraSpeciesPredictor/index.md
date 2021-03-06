---
title       : Flora Species Predictor
subtitle    : Developing Data Products - Course Project  
author      : Jovan Sardinha
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : prettify  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
github:
     user: JovanSardinha
     repo: DevelopingDataProducts_PeerAssesment/Presentation_FloraSpeciesPredictor
---

## Background & Purpose of this Project

**Background:**
The American botanist Edgar Anderson meticulously collected data on three species of iris in the early 1930s. Since then, the data set (or one of its variations) has been used to test hundreds, if not thousands, of machine learning algorithms.

Why has the iris data set become so popular? Fisher's selecting it to illustrate a discrimination algorithm brought it to peoples attention, and the fact that the data set contains three classes, only one of which is linearly separable from the other two, makes it interesting.


**Purpose:**
To build a web application that allows users to get a prediction for a flora species based on entered specifications in line with the Iris dataset. 

--- .class #id 

## About the Application

Link to the application: http://www.google.ca

The image below shows the various parts of the application and a sample output

<img src="assets/img/ApplicationScreenshot2.png"/>


--- .class #id 

## Machine Learning Model Used


```r
library(caret)
data(iris)
modFit <- train(Species ~ ., method="rpart", data=iris)
print(modFit$results)
```

```
##     cp Accuracy  Kappa AccuracySD KappaSD
## 1 0.00   0.9382 0.9065    0.02579 0.03875
## 2 0.44   0.7027 0.5703    0.15306 0.21410
## 3 0.50   0.5271 0.3105    0.13709 0.20415
```


--- .class #id 


## More Information about the Project

More information can be foind here: https://github.com/JovanSardinha/DevelopingDataProducts_PeerAssesment
