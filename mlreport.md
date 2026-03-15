# Intro to Machine Learning 

Machine Learning (ML) is everywhere today, from YouTube recommendations to self-driving 
cars. To understand the basics, I watched two beginner-friendly videos: "A Gentle 
Introduction to Machine Learning" by StatQuest and "How is Data Prepared for Machine 
Learning?" by AltexSoft. Both were easy to follow and gave me a solid foundation of how 
ML actually works.

## What is Machine Learning?

At its core, Machine Learning is about making predictions and classifications by learning 
patterns from data. A simple example from the video illustrates this using a 
**Decision Tree** — a model that asks a series of yes/no questions to arrive at a 
conclusion, much like how we naturally make decisions in everyday life.
![alt text](<Screenshot 2026-03-14 104309.png>)
## Training vs Testing Data

Another example from the video involves data showing that people who eat more yams tend 
to run faster in a 100-meter dash. Two lines are drawn to fit this data:
![alt text](<Screenshot 2026-03-14 121446.png>)
- A **black straight line** — simple and does not follow every data point closely
- A **green squiggly line** — complex and bends to match every single data point perfectly

At first glance the green line seems better since it fits the training data (red dots) 
more closely. However, Machine Learning is not just about fitting existing data — it is 
about making accurate predictions for new, unseen situations.
![alt text](<Screenshot 2026-03-14 121500.png>)
When new testing data (blue dots) is introduced, the black line actually outperforms the 
green line by predicting values more accurately. The green line, despite fitting the 
training data perfectly, produced much larger prediction errors on the testing data. 
This phenomenon is known as **overfitting** — where a model learns the training data 
too well but fails to generalize.Thats why its mentioned that machine learning is all 
about making most accurate predictions based on the data that the model has been trained on.

> No matter how complex or impressive a Machine Learning model looks, what truly matters 
> is how well it performs on testing data.

## Types of Machine Learning

- **Supervised Learning** — the model learns from labeled data where both the input and 
the correct answer are provided
- **Unsupervised Learning** — the model finds hidden patterns in data without any labeled 
answers
- **Reinforcement Learning** — the model learns through trial and error, guided by a 
reward and penalty system

## Loss and Error

The measure of how far off a model's predictions are from the actual values is called 
the **loss** or **error**. In models like Linear Regression, the differences between 
predicted and actual values are squared before being summed up. This is done to prevent 
positive and negative errors from cancelling each other out, giving a true measure of 
the model's overall performance.


# How is Data prepared for Machine Learning?
## Data Preparation – Insights from AltexSoft

The AltexSoft video focused on something easy to overlook: data preparation. It turns out 
that preparing data is often more work than training the model itself. No matter how 
powerful an algorithm is, if the data fed into it is messy or irrelevant, the results 
will be poor.
![alt text](<Screenshot 2026-03-14 111338.png>)
## Data Collection

A natural question that comes up early is — **how much data is actually enough?** The honest 
answer is to collect as much as possible, since it is difficult to predict which samples 
will turn out to be the most valuable. The amount needed largely depends on the complexity 
of the project. However quantity alone is not enough — quality matters just as much. 
Inaccurate or poorly collected data leads to unreliable models, and the data must always 
be relevant to the specific task being solved.

## Labelling

In supervised Machine Learning, data goes through a process called **labelling** — where 
the model is shown the correct answers by attaching corresponding labels to the dataset. 
The model also needs measurable characteristics called **features** that describe the data 
to it. Once the model has seen enough labelled examples, it learns to recognize patterns 
and can start making decisions on new, unseen inputs on its own.

## Data Reduction

Real world datasets often contain far more information than is actually useful for a 
given model. Each column in a dataset represents a **dimension** and a potential feature 
input. When too many dimensions are present and several of them carry little or no 
meaningful variation, the model's performance can degrade — a problem known as the 
**curse of dimensionality**. **Dimensionality reduction** tackles this by retaining only 
the features that genuinely contribute to the model's understanding of the problem.

For very large datasets, training can become slow and resource intensive. **Sampling** 
offers a practical solution by selecting a smaller, representative subset of the full 
dataset for training, reducing computational load without significantly sacrificing 
model quality.

## Data Wrangling

Before data can be fed into a model it often needs to be cleaned and restructured — 
a process called **data wrangling**. This transforms raw, inconsistent data into a 
format that accurately represents the problem at hand. The two key techniques involved 
are:

- **Formatting** — standardizing data collected from different sources so that it is 
- **Normalization** — rescaling feature values so that no single feature dominates 
model training due to its larger numeric range. **Min-Max normalization** is a widely 
used technique that compresses all values into a fixed range, ensuring every feature 
contributes equally to the model's learning process
consistent and compatible with the ML system being used.
![alt text](<WhatsApp Image 2025-09-08 at 01.00.34.jpeg>)

## Feature Engineering
In the given dataset you start making your own set of data by performing mathematical operations or concatenating two columns so that your sample space is extended.

## The Big Picture

Building a Machine Learning model is like cooking — the **algorithm** is the chef, 
but the **data** is the ingredient. No matter how skilled the chef is, a great dish 
can only come from fresh, well-prepared ingredients. **Garbage in, garbage out.**