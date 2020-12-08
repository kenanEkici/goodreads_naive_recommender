# Naive recommender system Goodreads dataset

The following repository contains two projects:

## Goodreads dataset cleaning, transformation and analysis

In the Python notebook, you can find the steps to reproduce the dataset used in the next project. Here, the following dataset https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/books containing over 2.3million books (and corresponding authors and genres) is cleaned and transformed into a format more convenient to load into a PostgresQL (or any SQL) database. After cleaning and formatting, the Books, Authors, and Genres data (and their corresponding relations) are parsed into both a JSON and Numpy format. The latter was necessary to significantly speed up data retrieval and computation with Numpy rather than relying on SQL queries or Pandas. 

<b>You do not have to run this notebook, the resulting datasets have already been included in the next project. If you want to run the notebook yourself, it is advised to do so with Google colab.</b>

## Naive recommender system API with Flask, Postgres and Numpy

The next project in this repository is a naive recommender system that retrieves books based on novel user preferences such as favorite genres, authors, amount of pages, amount of reviews. The recommender system calculates a match score based on similarity of user preferences to each book "profile". Depending on the match score threshold that the user has set, a set of books will be recommended to the user when they exceed the threshold.

The algorithm will look for matches naively. In order to speed this process up significantly, we use multithreading to traverse books on different data points simultaneously. Additionaly, we used Numpy to retrieve and process data much faster. 

### Install guide

### API guide






