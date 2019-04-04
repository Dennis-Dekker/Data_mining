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

# Task 2: Learn using the dataset (40 points)

In the next step, we are going to use our dataset to create a predictive model. You can make your own
choice whether you want to create individual models per patient or a single model for all patients. You
will need to study three variants of predictive models:

1. A variant where you use the pre-processed dataset you identified in Task 1 in combination with a
machine learning technique you consider appropriate.
2. A variant where you apply a learning algorithm that is able to cope with this temporal data (e.g.
ARIMA, recurrent neural networks, etc.).
3. Implement a benchmark: predict the mood on the next day by just saying it is the same as the
previous day.

Define a proper performance metric and create a solid evaluation setup. Describe and argue your
choices again and show the results you have obtained. Create graphs to illustrate the performance in an
insightful way.

# Task 3: Evaluate and reflect on your results (20 points)

Finally, analyse the results in detail both using a more statistical view and by means of your
interpretation. Argue what the pros and cons of the different approaches are.
Report
We would like you as a group of 3 to prepare a report with the following in mind:

• The report should be submitted via Canvas by 19/04/2019 17:00. This is a strict deadline, please
try to respect that, otherwise points will be deducted.
• Please format the document according to the lncs guidelines. The lncs format is used for scientific
papers published by the Springer, where lncs stands for Lecture Notes in Computer Science, see
http://www.springer.com/computer/lncs?SGWID=0-164-6-793341-0, Note that you don't need to
include an abstract in your report. The paper should not exceed 8 pages. With the 8 pages limit, my
aim is to challenge you to report only what is necessary.
• Make sure we can identify your report, i.e., at least a subset of the (name, student number, vunetID) triplet should be in the document’s header.
• Make an attempt to make the report look professional. Have a short introduction of your document,
use appropriate language, etc. Let’s say, if you gave your report to the manager of your DM
project at a company, they would need to be able to understand it and conclude that it’s a good
project start.

# Grading

Marking will be based on the tasks as reflected by quality of the report (so content, style, etc. all
matter). You can get maximum 100 marks for this assignment. You will need at least 55 to pass. You
will receive 10 bonus points on top of your assignment grade for choosing the advanced assignment.
Also, 100 points are only given to students whose reports are of exceptional quality, and they also
should report something we did not specifically ask for (in other words, we value proactivity and
creativity).
