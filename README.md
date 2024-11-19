
# Analyzing Book Data and Building Recommendation Systems with Python

_For a detailed look at the visualizations and insights from this project, you can check out my [blog](https://medium.com/@vpanh/analyzing-book-data-and-building-recommendation-systems-with-python-a81650625789) on Medium._


<br />


## 1. Introduction
With millions of books published each year, readers often struggle to find their next great read. This project aims to perform a comprehensive analysis of book-related data to uncover significant insights into the literary world. Using Python, we will delve into various aspects of books, such as their ratings, pricing trends, popular genres, and author contributions. Additionally, we will develop recommendation systems that will help readers discover books that match their interests and preferences.


<br />


## 2. Objectives
In particular, we will focus on uncovering the following:
* **_Rating Distribution:_** Exploring how ratings are distributed among various books.

* **_Most Popular Book Genres:_** Identifying which genres capture the most reader interest.

* **_Distribution of Book Prices:_** Analyzing the variations in book prices across different categories.

* **_Distribution of Ratings Count:_** Investigating how many ratings different books have received.

* **_Average Review Score by Book Price:_** Examining the relationship between the price of a book and its average review score.

* **_Top Publishers with Most Books:_** Finding out which publishers have released the highest number of titles.

* **_Most Reviewed Book:_** Highlighting the book that has garnered the most reviews from readers.

* **_Distribution of Published Years:_** Observing how the number of published books has changed over the years.

* **_Top Authors with Most Books:_** Identifying the authors who have published the most works.

* **_Word Cloud for Book Reviews:_** Visualizing common words and themes in book reviews.

* **_Word Cloud for Book Titles:_** Visualizing the most frequently used words in book titles.

* **_Recommendation Algorithms:_** Implementing two recommendation systems to provide personalized book suggestions for readers.


<br />



## 3. Data Documentation

### _Data Selection_
For this project, we utilized a combined dataset that includes two comprehensive sources:
* **Book Details:** This dataset contains information on **212,404 unique books**. It includes various attributes such as titles, authors, publication years, genres, and prices.
* **Book Reviews:** We also integrated a dataset comprising **142.8 million reviews**, covering a time span from **May 1996 to July 2014**. This dataset provides valuable insights into reader preferences, rating distributions, and sentiment towards various books, enhancing the depth of our analysis.


### _Data Ethics_
All datasets used in this project are sourced from publicly available resources with CC0: Public Domain license. This ensures that the data can be utilized for research and analysis.


<br />


## 4. Project Steps

### _1. Setting Up:_
Import libraries

### _2. Data Pre-Processing:_

Book Reviews Dataset:
* **_Anonymization:_** Replaced user IDs with hashed identifiers to protect privacy.
* **_Removed Columns:_** Deleted Profile Name and User ID columns to simplify the data.
* **_Null Handling:_** Dropped rows with missing titles (since the title is essential for recommendations).
* **_Duplicate Removal:_** Removed duplicate entries to ensure accuracy.
* **_Date Conversion:_** Converted Review Time to datetime format for consistency.

Book Details Dataset:
* **_Filled Missing Values:_** Addressed missing values to ensure completeness.
* **_Dropped Null Titles:_** Dropped rows without titles, similar to the reviews dataset.
* **_Removed Duplicates:_** Removed duplicates to ensure data quality.
* **_Standardized Dates:_** Unified Publication Date format and converted to datetime.
* **_Added New Columns:_** Added Publication Year and Average Rating columns.

Finally, both datasets were merged on the Title column to create a unified dataset for further analysis and recommendations.

### _3. Exploratory Data Analysis (EDA):_
   * Rating Distribution
   * Most Popular Book Genres
   * Distribution of Book Prices
   * Distribution of Ratings Count
   * Average Review Score by Book Price
   * Top Publishers with Most Books
   * Most Reviewed Book
   * Distribution of Published Years
   * Top Authors with Most Books
   * Word Cloud for Book Reviews
   * Word Cloud for Book Titles

### _4. Recommendation Systems:_
* Books Rated Highly by the Selected User
* Item-Based Collaborative Filtering
* Content-Based Filtering

### _5. Conclusion:_
* Key Insights
* Project Limitations
* Recommendations


<br />


## 5. Conclusion
The **EDA** has provided a comprehensive overview of the book dataset, uncovering notable trends and characteristics in publication patterns, genre popularity, author prominence, and reader reviews. Key insights include:

* **_Publication Trends:_** A major increase in published books from 2000 to 2015, which correlates with the rise of digital and self-publishing, indicating shifts in publishing dynamics.
* **_Genre and Author Popularity:_** Certain genres and authors dominate, with a few top names consistently contributing to high book counts and review volumes.
* **_Review Patterns:_** Frequent themes in reviews reveal readers' interests in specific topics such as personal growth, storytelling quality, and cultural significance.

The **recommendation algorithms** demonstrated differences in how Item-Based Collaborative Filtering and Content-Based Filtering serve user preferences.

* **_Item-Based Collaborative Filtering:_** concentrated on identifying similarities between books based on the ratings given by users. It recommended books that were highly rated by users who had similar interests, focusing on the collective patterns of book preferences rather than individual users. This method provided recommendations that reflected broader user behavior surrounding specific titles.

* **_Content-Based Filtering:_** focused on the attributes and content of the books that the user had previously rated highly. It recommended books with similar themes, genres, or characteristics to those the user had enjoyed, emphasizing the content of the books rather than user interactions. This approach ensured recommendations were aligned with the specific features of books the user was likely to enjoy based on their past ratings.

### Project Limitations
Despite the insights gained from the exploratory data analysis and recommendation systems, the project faced some limitations:
Limited Dataset Size for Recommendation Systems: To ensure efficient processing, the recommendation algorithms utilized a subset of the overall dataset.
Static Dataset: The analysis was conducted on a static dataset, meaning that it did not account for the dynamic nature of reader preferences and new book releases.

### Recommendations
For Publishers:
* Utilize the insights gained from the EDA to inform marketing strategies and focus on promoting genres that have shown significant growth and reader engagement.
* Highlight authors who resonate with current trends and encourage the exploration of lesser-known titles that fit established reader preferences.

For Improving Recommendation Algorithms:
* Continuously enhance the Item-Based Collaborative Filtering algorithm by integrating new user data to refine its predictive accuracy and responsiveness to changing user preferences.
* Expand the capabilities of Content-Based Filtering by incorporating more detailed metadata about books, enabling a deeper understanding of user interests and facilitating more personalized recommendations.