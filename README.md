# Data mining: Advanced assignment

Deadline: April 19, 2019 17:00

# Dataset and problem description

As a first step, let us look at the dataset we are faced with. The domain from which the dataset
originates is the domain of mental health. More and more smartphone applications are becoming
available to support people suffering a depression. These applications record all kinds of sensory data
about the behaviour of the user and in addition frequently ask the user for a rating of the mood.

The dataset contains ID’s, reflecting the user the measurement originated from. Furthermore, it
contains time-stamped pairs of variables and values.

Using this dataset, we would like to build a predictive model that is able to predict the average mood
of the user on the next day based on the data we obtained from the user on the days before. 

# Task 1: Pre-process the dataset (40 points)

Essentially there are two approaches you can consider to create a predictive model using this dataset:
(1) use an machine learning approach that can deal with temporal data (e.g. ARIMA, recurrent neural
networks) or you can try to aggregate the history somehow to create attributes that can be used in a
more common machine learning approach (e.g. SVM, decision tree). For instance, you use the average
mood during the last five days as a predictor. Ample literature is present in the area of temporal data
mining that describes how such a transformation can be made. We are going to focus on such a
transformation in this part of the assignment.

In the end, we end up with a dataset with a number of training instances per patient (as you have a
number of time points for which you can train), i.e. an instance that concerns the mood at t=1, t=2, etc.
Of course it depends on your choice of the history you consider relevant from what time point you can
start predicting (if you use a windows of 5 days of history to create attributes you cannot create training
instances before the 6th day). To come to this dataset, you need to:

1. Define attributes that aggregate the history, draw inspiration from the field of temporal data
mining.
2. Define the target by averaging the mood over the entire day.
3. Create an instance-based dataset as described in Figure 2.

Make an appointment with your TA to discuss your ideas before finalizing them. In the end, you
should describe and argue your choices clearly and back them up with scientific literature. Next,
perform a preliminary analysis (e.g. look at correlations) on the usefulness of the attributes you have
defined
