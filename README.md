# Hi, 

In this repository, I worked on movie recommender system via applying collaborative filtering. I used MovieLens 100K dataset. 

It can be concluded from Exploratory Data Analysis that;

  :clapper: There are accumulations on integer rating means. Some movies have 1 rating count and rating means are 1,2,3,4,5.
  
  ![](https://github.com/M-Rasit/Movie-Recommender-System-Collaborative-Filtering/blob/master/images/rating%20means%20barchart.png)
  
  :clapper: Movies with higher rating means and higher rating counts are mostly between 2-4.5 rating
  
  :clapper: Most of the movies have less than 300 rating numbers.
  
  ![](https://github.com/M-Rasit/Movie-Recommender-System-Collaborative-Filtering/blob/master/images/rating%20count%20barchart.png)
  
  
  
### Corrwith
Applying pivot table on dataset get each user's rate for each movie. Then, I choosed "Star Wars" and "Air Force One" movies for further process.
With using pandas.DataFrame.corrwith, I got similarity matrix that has the correlation of other movies' user rate and movies that I choosed. At last, sorting similarity matrix based on correlation and higher rating gets movie recommendations.

:flashlight: There is one important step that filtering movies on rating count will be more effective on accurate results. 

  :movie_camera: Movies recommended for Star Wars
  
![](https://github.com/M-Rasit/Movie-Recommender-System-Collaborative-Filtering/blob/master/images/Star%20Wars%20-%20Corrwith.png)

  :movie_camera: Movies Recommended for Air Force One
  
![](https://github.com/M-Rasit/Movie-Recommender-System-Collaborative-Filtering/blob/master/images/Air%20Force%20One%20-%20Corrwith.png)



### Nearest Neighbor
In this technique I used pivot table DataFrame and used them as input for csr_matrix. This process turned movies into data points. Then applying cosine metric in Nearest Neighbors module gave us distances and indices. From movie indices, we got the movies.

  :movie_camera: Movies Recommended for Star Wars
  
![]()

  :movie_camera: Movies Recommended for Air Force One
  
![](https://github.com/M-Rasit/Movie-Recommender-System-Collaborative-Filtering/blob/master/images/Star%20Wars%20-%20Nearest%20Neighbor.png)


