# Predict-DVD-sales

# Read the DVD sales data in a file 
dvdsales <- read.csv("dvdds.csv", header = T)

#Since attractiveness is a factor, converting it to a factor 
dvdsales$attractiveness <- as.factor(dvdsales$attractiveness)

#Picking up a random sample for training data 
set.seed(1)
dvdds <-sample(nrow(dvdsales), nrow(dvdsales)*.3)
x1<-sample(200,200*.7)

#dvd_train is a data set to train our model
dvd_train <- dvdsales[dvdds,]

#dvd_test is a data set to test the model
dmod1 <- lm(sales~.,data=dvd_train)











