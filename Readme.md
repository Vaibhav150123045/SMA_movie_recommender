A Recommender System to show personalized movie recommendations based on
ratings given by a user and other users similar to them in order to
improve user experience.

**Dataset:[ ](https://drive.google.com/drive/folders/1qe3di-dDXC4uMZp8dGIv-J_bFHoKjrWi?usp=sharing)[https://drive.google.com/drive/folders/1RY4RG7rVfY8-0uGeOPWqWzNIuf-iosuv](https://drive.google.com/drive/folders/1qe3di-dDXC4uMZp8dGIv-J_bFHoKjrWi?usp=sharing)**

**Data Dictionary:**

RATINGS FILE DESCRIPTION  
=========================================================================  
All ratings are contained in the file "ratings.dat" and are in the
following format:  
UserID::MovieID::Rating::Timestamp

- UserIDs range between 1 and 6040

<!-- -->

- MovieIDs range between 1 and 3952

<!-- -->

- Ratings are made on a 5-star scale (whole-star ratings only)

<!-- -->

- Timestamp is represented in seconds

<!-- -->

- Each user has at least 20 ratings
  USERS FILE DESCRIPTION  
  =========================================================================  
  User information is in the file "users.dat" and is in the following
  format:  
  UserID::Gender::Age::Occupation::Zip-code  
  All demographic information is provided voluntarily by the users and
  is not checked for accuracy.Only users who have provided some
  demographic information are included in this data set.

<!-- -->

- Gender is denoted by a "M" for male and "F" for female

<!-- -->

- Age is chosen from the following ranges:

  - 1: "Under 18"

  <!-- -->

  - 18: "18-24"

  <!-- -->

  - 25: "25-34"

  <!-- -->

  - 35: "35-44"

  <!-- -->

  - 45: "45-49"

  <!-- -->

  - 50: "50-55"

  <!-- -->

  - 56: "56+"

<!-- -->

- Occupation is chosen from the following choices:

  - 0: "other" or not specified

  <!-- -->

  - 1: "academic/educator"

  <!-- -->

  - 2: "artist"

  <!-- -->

  - 3: "clerical/admin"

  <!-- -->

  - 4: "college/grad student"

  <!-- -->

  - 5: "customer service"

  <!-- -->

  - 6: "doctor/health care"

  <!-- -->

  - 7: "executive/managerial"

  <!-- -->

  - 8: "farmer"

  <!-- -->

  - 9: "homemaker"

  <!-- -->

  - 10: "K-12 student"

  <!-- -->

  - 11: "lawyer"

  <!-- -->

  - 12: "programmer"

  <!-- -->

  - 13: "retired"

  <!-- -->

  - 14: "sales/marketing"

  <!-- -->

  - 15: "scientist"

  <!-- -->

  - 16: "self-employed"

  <!-- -->

  - 17: "technician/engineer"

  <!-- -->

  - 18: "tradesman/craftsman"

  <!-- -->

  - 19: "unemployed"

  <!-- -->

  - 20: "writer"
    MOVIES FILE DESCRIPTION  
    =========================================================================  
    Movie information is in the file "movies.dat" and is in the
    following format:  
    MovieID::Title::Genres

<!-- -->

- Titles are identical to titles provided by the IMDB (including year of
  release)

<!-- -->

- Genres are pipe-separated and are selected from the following genres:

  - Action

  <!-- -->

  - Adventure

  <!-- -->

  - Animation

  <!-- -->

  - Children's

  <!-- -->

  - Comedy

  <!-- -->

  - Crime

  <!-- -->

  - Documentary

  <!-- -->

  - Drama

  <!-- -->

  - Fantasy

  <!-- -->

  - Film-Noir

  <!-- -->

  - Horror

  <!-- -->

  - Musical

  <!-- -->

  - Mystery

  <!-- -->

  - Romance

  <!-- -->

  - Sci-Fi

  <!-- -->

  - Thriller

  <!-- -->

  - War

  <!-- -->

  - Western
    **Concepts Tested:**

<!-- -->

- Recommender Engine

<!-- -->

- Collaborative Filtering (Item-based & User-based Approach)

<!-- -->

- Pearson Correlation

<!-- -->

- Nearest Neighbors using Cosine Similarity

<!-- -->

- Matrix Factorization
  **What does “good” look like?**

<!-- -->

- Reading the data files, formatting them into a proper workable format
  and merging the data files into one single dataframeEg:
  pd.read_fwf('../input/zeemovie/movies.dat', encoding='ISO-8859-1'

<!-- -->

- Performing exploratory data analysis like checking the structure &
  characteristics of the dataset and cleaning the data

<!-- -->

- Performing feature engineering steps type conversions and deriving new
  features like ‘Release Year’

<!-- -->

- Visualizing the data with respect to different categories to get a
  better understanding of the underlying distribution

<!-- -->

- Grouping the data in terms of Average Rating and No. of Ratings given

<!-- -->

- Creating a pivot table of movie titles & user id and imputing the NaN
  values with a suitable value

<!-- -->

- Follow the Item-based approach and

  - **Pearson Correlation**

    - Take a movie name as input from the user

    <!-- -->

    - Recommend 5 similar movies based on Pearson Correlation

  <!-- -->

  - **Cosine Similarity**

    - Print the item similarity matrix and user similarity matrix

      - Example: An user-user similarity matrix just for
        demonstration.Screenshot_2022-11-08_at_5.35.47_PM.png ¬

  <!-- -->

  - Create a CSR matrix using the pivot table.\[**Optional**, This is an
    extended
    approach, **[link](https://docs.scipy.org/doc/scipy/reference/generated/scipy.sparse.csr_matrix.html)** to
    example implementation\].

  <!-- -->

  - Write a function to return top 5 recommendations for a given item

  <!-- -->

  - **\[sklearn optional\]** Take a movie name as user input and use KNN
    algorithm to recommend 5 similar movies based on Cosine Similarity.
    \[**[link](https://scikit-learn.org/stable/modules/neighbors.html)** to
    sklearn Nearest Neighbor documentation\]

<!-- -->

- **Matrix Factorization**

  - Use **cmfrec/Surprise** library to run matrix factorization. (Show
    results with d=4).

  <!-- -->

  - Evaluate the model’s performance using RMSE and MAPE.

  <!-- -->

  - **Bonus** - how can you do a train test split for MF?

<!-- -->

- **Embeddings for item-item and user-user similarity**

  - Re-design the item-item similarity function to use MF embeddings
    (d=4) instead of raw features

  <!-- -->

  - Similarly, do this for user-user similarity

  <!-- -->

  - **Bonus**: Get d=2 embeddings, and plot the results. Write down your
    analysis from this visualisation. (Compare with other visualization
    techniques)

<!-- -->
