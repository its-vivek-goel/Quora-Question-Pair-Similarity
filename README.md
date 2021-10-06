# Quora-Question-Pair-Similarity

1. Business Problem


1.1 Description
Quora is a place to gain and share knowledge—about anything. It’s a platform to ask questions and connect with people who contribute unique insights and quality answers. This empowers people to learn from each other and to better understand the world.

Over 100 million people visit Quora every month, so it's no surprise that many people ask similarly worded questions. Multiple questions with the same intent can cause seekers to spend more time finding the best answer to their question, and make writers feel they need to answer multiple versions of the same question. Quora values canonical questions because they provide a better experience to active seekers and writers, and offer more value to both of these groups in the long term.

Problem Statement --
Identify which questions asked on Quora are duplicates of questions that have already been asked.
This could be useful to instantly provide answers to questions that have already been answered.
We are tasked with predicting whether a pair of questions are duplicates or not.
Source -
Source : https://www.kaggle.com/c/quora-question-pairs

1.2 Real world/Business Objectives and Constraints

a.The cost of a mis-classification can be very high.
b.You would want a probability of a pair of questions to be duplicates so that you can choose any threshold of choice.
c.No strict latency concerns.
d.Interpretability is partially important.

2. Machine Learning Probelm

2.1 Data Overview

Data is in a file train.csv
train.csv contains 6 columns : id , qid1 , qid2 , question1 , question2 , is_duplicate
Size of train.csv - 58.7 MB
Number of rows in Train.csv = 404,290

2.2 Mapping the real world problem to an ML problem

a. Type of Machine Leaning Problem
It is a binary classification problem, for a given pair of questions we need to predict if they are duplicate or not.

b. Performance Metric
Source: https://www.kaggle.com/c/quora-question-pairs#evaluation

Metric(s):

log-loss : https://www.kaggle.com/wiki/LogarithmicLoss
Binary Confusion Matrix

2.3 Train and Test Construction

We build train and test by randomly splitting in the ratio of 70:30 or 80:20 whatever we choose as we have sufficient points to work with.
