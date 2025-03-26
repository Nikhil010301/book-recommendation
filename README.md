# **Book-Recommendation-System**

<img src="Images\book3.png" alt="books" width="750" height="400">

#### **Authors**: 
[Alice Wamuyu](alice.wamuyu@student.moringaschool.com),
[Eva Moisasi](ava.moisasi@student.moringaschool.com),
[Fridah Kimathi](mailto:fridahnkirotekimathi@gmail.com) and
[Nicholus Magak](nicholus.magak@student.moringaschool.com).

## Overview
****
The project aims to develop a machine learning model that can provide personalized book recommendations to users based on their past ratings. The model will analyze the user’s ratings on books to identify patterns and preferences and recommend books that the user is likely to enjoy but has not read yet.

## Business Problem
***
<p>As a rapidly growing online retailer, Jumia has a vast collection of books. Most self-published authors sell 250 books or less, regardless of how many different books they write. Traditionally published books sell around 3,000 copies on average, with only 250 of those sales in the first year. It's rare that books sell over 100,000 copies and even rarer to sell more than a million</p>
<p>An attributing factor to the poor sales of potentially good books in the public’s eye is that there are too many books that major recommenders can read which can also be fueled by people sticking to specific authors rather than exploring due to the fear of reading a potentially different genre than what their tastes are accustomed to.</p>
<p>To address this issue, Jumia can implement an A.I model that uses a collaborative filtering technique. By doing so, they will not only recommend books based on the customers’ ratings but also suggest books that are similar to the ones that the customer has shown an interest in</p>

## Data
***
# **Data Understanding**

The Book Recommendation Data used in this project is from <a href='https://www.kaggle.com/datasets/rxsraghavagrawal/book-recommender-system'> Kaggle.</a>. The data contained three files: 

* **_Users.csv_**

Contained the users. Some of the features in this file include user IDs (User-ID) which have been anonymized and map to integers. Demographic data such as (Location, Age)  was also provided where it was available. Otherwise, these fields contained null values.

* **_Books.csv_**

Contained books. Books were identified by their respective International Standard Book Number(ISBN).Some content-based information given (Book-Title, Book-Author, Year-Of-Publication, Publisher), was obtained from Amazon Web Services. In the case of several authors, only the first was provided. URLs linking to cover images were also given, appearing in three different flavors (Image-URL-S, Image-URL-M, Image-URL-L), i.e., small, medium, large. These URLs point to the Amazon web site.

* **_Ratings.csv_**

Contains the book rating information. Ratings (Book-Rating) are either explicit, expressed on a scale from 1-10 (higher values denoting higher appreciation), or implicit, expressed by 0.

                    Visualizations:
***
                 i. Ratings
 <img src="Images\ratings.jpg"  width="750" height="400"> 

                 ii. Years vs. Number of books made
<img src="Images\years.jpg"  width="750" height="400">

                 iii. Average age of readers per country
 <img src="Images\avg_age.png"  width="750" height="400"> 
 
                 iv. Top 10 Authors
 <img src="Images\top10authors.jpg"  width="750" height="400"> 
 
                 v. Top 10 books
 <img src="Images\top10books.jpg"  width="750" height="400"> 
 
                 vi. Top 10 publishers
 <img src="Images\top10publishers.jpg"  width="750" height="400"> 
 
                 vii. Average Rating per Country
 <img src="Images\avg_rating.png"  width="750" height="400"> 
 
## Modelling
***
The modeling of this project consists of multiple recommender system implementations:

**Popularity Based Recommendation system:**

This focuses on getting the most positively rated books amongst the most viewers possible. It is a simple implementation, however, in most scenarios where knowing the users’ data and books’ information is not possible, this can apply due to the fact that it still will end up recommending books that will fit a good majority of the readers who rate.

**Model-Based Collaborative Filtering Recommendation system:**

We will be using the matrix factorization with SVD(Singular Value Decomposition) to ensure the latent features in our dataset will compare books and the users who rate them and produce a matrix that can produce estimates of books to better recommend them to potential readers.

## Evaluation
***
Recommender systems have become an essential tool for online businesses to provide personalized recommendations to their users. The performance of a recommender system is often evaluated based on various metrics, such as precision, recall, F1-score, and so on. However, some types of recommender systems, such as the popularity-based ones, lack a performance metric as they provide recommendations solely based on the popularity of the items.

Despite this limitation, the popularity-based recommender can be used as an initial model when individual user data is unavailable. For instance, in situations where a new user signs up for a service, and the system has no data on their preferences, a popularity-based recommender can provide a general sense of the most popular or commonly viewed items. This approach can help the system to learn more about the user's preferences and provide more personalized recommendations later on.

On the other hand, a book recommender system with an RMSE of 1.47 indicates that the system's predicted ratings deviate from the actual ratings by an average of 1.47 stars. While this may seem like a significant difference, it is relatively low compared to the range of possible ratings. For example, if the rating scale is from 1 to 5 stars, an RMSE of 1.47 implies that the system's recommendations are accurate within about one star, on average. This relatively low RMSE value suggests that the system is providing fairly accurate recommendations.

It is also noteworthy that the statement mentions the removal of implicit data. Implicit data refers to the data that the system gathers indirectly, such as the user's browsing history or search queries. While this data can be useful, it may also introduce biases and noise into the recommendations. Therefore, removing implicit data can improve the accuracy and fairness of the system's recommendations.

Overall, the evaluation suggests that the book recommender system is performing quite well, especially after accounting for the removal of implicit data. However, it is essential to keep in mind that the performance of a recommender system is not solely determined by a single metric, and other factors such as user satisfaction and system scalability should also be considered.

## Conclusion
***
A book recommender system that takes into account the individual preferences of each user is more likely to be effective than one that provides generic recommendations. Collaborative filtering, which involves analyzing the behavior and preferences of similar users to make recommendations, was used for building book recommender systems. The effectiveness of a book recommender system is heavily dependent on the quality of the data. For the model to run optimally the data fed to it should be  accurate, relevant, and up-to-date. The performance of a book recommender system was evaluated using the Root Mean Square Metric(RMSE). This metric was used to identify areas for improvement and optimize the system for better performance.

## Recommendations
***
* Ensure data quality. Ensure that the data used to train and test the model is accurate, relevant and up-to-date
* Incorporate more types of data, such as book genres and authors, to enhance the recommendation system's effectiveness.
* Regularly evaluate the performance of the book recommender system using appropriate metrics to identify areas for improvement and optimize the system for better performance.
* Develop a user interface that is intuitive and user-friendly, to improve user engagement and satisfaction.

## For More Information
***
See the full analysis in the [Jupyter Notebook](https://github.com/FridahKimathi/Book-Recommendation-System/blob/main/index.ipynb) or review this [presentation](https://github.com/FridahKimathi/Book-Recommendation-System/blob/main/Book%20Recommendation%20System.pptx.pdf).

## Repository Structure
***

```
├── Data
├── Images
├── Book Recommendation System.pptx.pdf
├── Jumia Book Recommendation System Data Report.pdf
├── README.md
└── index.ipynb
```
