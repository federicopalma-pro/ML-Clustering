# ML-Clustering

## Introduction

This repository contains examples of best practices for solving Machine Learning Clastering problems throughout the entire machine learning product life cycle, from data analysis to placing the final machine learning model in production. The code is organized into Jupyter notebooks, with each notebook focusing on a specific classification technique or dataset.

My goal is to provide a clear and concise set of examples that can help you learn how to effectively tackle clastering problems, and to guide you through each step of the process, from data exploration and model training to deployment and monitoring. I believe that understanding the entire process of developing a machine learning model, from data cleaning and preprocessing to deploying and maintaining the model in a production environment, is crucial for creating successful machine learning products.

In addition to the notebooks, I've also included a set of scripts and utilities that can help you automate common tasks in the machine learning product life cycle. These tools are designed to help you streamline your workflow and save time, allowing you to focus on building better models.

Whether you're just getting started with Machine Learning or you're a seasoned practitioner, I believe you'll find something of value in this repository. I encourage you to explore the notebooks, try out the code for yourself, and let me know if you have any questions or feedback.

## Dataset

The dataset used in this project is the "Wine" dataset, obtained from OpenML, which is designed for clustering machine learning problems. This dataset contains information on three different cultivars of wine (Cultivar 1, Cultivar 2, and Cultivar 3) and their chemical composition such as alcohol content, malic acid concentration, and flavonoid levels.

The wine dataset is an excellent alternative to commonly used datasets like Iris or MNIST for clustering tasks. With 178 rows and 13 columns, it provides sufficient data for meaningful analysis while still being manageable. Additionally, the inclusion of multiple cultivars allows for more sophisticated clustering techniques that cannot be performed on the Iris or MNIST datasets.

## 1 - Preprocessing dataset

The first step in solving a machine learning clustering problem is to preprocess the dataset. Using the Pandas library, we load the "wine.csv" file and then analyze it to determine which features are numerical and which are categorical. It's essential to identify and handle any missing values or NaNs in the dataset, either by replacing or removing them. In our case, since there are no NaNs, we can go further.

The next step is to scale numerical features using Standarscaler. After completing these preprocessing steps, we can save the datasets ready for use by the Sklearn machine learning libraries.

## 2 - Classification lab

After preprocessing the wine dataset, we can run a series of clustering algorithms to determine the optimal number of clusters. This is achieved using the Elbow method. Once we have found the optimal value of k, we build our model based on K-means and make predictions to assign the predicted label to each record.

## 3 - Pipeline for production

In the final step, we reconstruct the pipeline of our model by including the necessary input data transformations. We can then train the pipeline one last time on the X data of our wine dataset and save it to disk using the joblib library.

At this point, our clustering predictive model is ready to be integrated into any production application. The pipeline can be easily deployed to a cloud environment, such as Amazon Web Services (AWS), Google Cloud Platform (GCP) or Microsoft Azure, or to an on-premises server. Once deployed, the pipeline can receive input data and provide predictions in real-time, enabling us to make accurate decisions and automate processes based on the predictions made by our machine learning model.

## Final notes

You can use these three steps outlined in the Jupyter Notebook worksheets for any clustering work. Of course, these should be understood as a solid starting point that needs to be adapted to the needs of your project. However, from personal experience, they can significantly accelerate the workflow for the entire life cycle of the predictive machine learning model.

Happy clustering!
