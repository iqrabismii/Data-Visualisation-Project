 # :clapper: Analysis on Netflix Movies 
 
 ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) 
 ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white) ![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) 
 
 ## Introduction 
 This dataset contains more than 8,500 Netflix movies and TV shows, including cast members, duration, and genre. It contains titles added as recently as late September 2021. This case study was taken from DataCamp. Link to DataCamp workspace is given below. 
 
<a>
<a href="https://app.datacamp.com/workspace/w/886521ec-f152-464e-b2b1-6a13f258d5a6/edit "><img align="left" src="https://img.shields.io/badge/Datacamp-05192D?style=for-the-badge&logo=datacamp&logoColor=03E860" alt='Iqra Bismi | DataCamp'width="110px"/>
</a> 
<br>
 
 
 
 ## Challenges
 
🗺️ Explore: How much variety exists in Netflix's offering? Base this on three variables: type, country, and listed_in. <br>
📊 Visualize: Build a word cloud from the movie and TV shows descriptions. Make sure to remove stop words!<br>
🔎 Analyze: Has Netflix invested more in certain genres (see listed_in) in recent years? What about certain age groups (see ratings)?<br><br>
Scenarios are broader questions to help you develop an end-to-end project for your portfolio:<br>

A talent agency has hired you to analyze patterns in the professional relationships of cast members and directors. The key deliverable is a network graph where each node represents a cast member or director. An edge represents a movie or TV show worked on by both nodes in this undirected graph. You can limit the actors to the first four names listed in cast. The client is interested in any insights you can derive from your Netflix network analysis, such as actor/actor and actor/director pairs that work most closely together, most popular actors and directors to work with, and graph differences over time.

You will need to prepare a report that is accessible to a broad audience. It will need to outline your motivation, analysis steps, findings, and conclusions.

## Data Preprocessing
Removed null and duplicate values from the dataset. There were around 2634 missing values for director, around 800 missing values for cast. All these values were dropped from using dropna on axis =0 (row). Datatype for date column was changed to datetime using pd.to_datetime. Lastly data quality report was created for both numeric and categorical variables showing missing, cardindality, mode, median etc. 
Genre, director and cast was present as multiple values in one column. pandas explode function was used to unpack these values

## Exploratory Data Analysis (EDA)
Barplot, countplot were created to show top ten directors, actors, movies, tvshow and genre. Line graph was created to show trend for movies, tv show for last ten years. Also, network graph using plotly was created to show frequency between director and actors as shown below <br>
![download (1)](https://user-images.githubusercontent.com/108056063/211174922-9a29d24a-b6dd-449d-89ca-35394894cb9f.png)


## Outcome (EDA)
It was observed that movies were more popular as compared to tv shows. Also Internal movies are most watched movies. Most of the Tv shows had season 3 or less than 3. USA followed by India watched most number of shows where Canada had the least frequency. 
Distribution for duration followed a multimodel distribution. Word cloud was created for movies and most common words were love,family and life whereas for tv show common words were family, world, journey, life. Lastly, used plotly to create networkgraph. and it was observed that most of the directors worked with different four actors in movies and tv shows. 
