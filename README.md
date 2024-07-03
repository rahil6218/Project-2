# Analysis of IMDB Dataset. 
### Table of Content 
-[Project Overview](#project-overview)

-[Data Sources](#data-sources)

-[Tools](#tools)

-[Data Preparation](#data-preparation)

-[Exploratory Data Analysis](#exploratory-data-analysis)

-[Data Analysis](#data-analysis)

-[Results](#results)
### Project Overview 

This project involves analyzing a dataset from IMDb to extract meaningful insights about movies. The analysis focuses on various aspects such as highest average voting, highest revenue, average rating of directors, comparison of movies released in particular years, comparison of largest and smallest runtime, and identifying the exact genre of movies.

### Data Sources

-IMDB Developer [LINK](https://developer.imdb.com/non-commercial-datasets/)

-The dataset used in this project is an IMDb dataset in CSV format. Ensure you have the CSV file saved in the data/ directory.


### Tools
- Python(Pandas,Matplotlib,BeautifulSoup) [Download](https://www.python.org/downloads/)
- Anaconda [Download](https://www.anaconda.com/download)
- Jupitar Notebook [Download](https://jupyter.org/install)
- Excel [Download](https://www.microsoft.com/en-us/microsoft-365/excel)

### Data Preparation 
The initial extraction phase we performed following tasks :
1. Import CSV file into jupitar notebook.
2. Import all Pyhton libraries used in it.
3. Analyse data using this libraries.

###  Exploratory Data Analysis
1. From this Analysis we analysed that the Star wars Episode VII has the maximum revenue i.e 936.63(millions$)
2. We analysed that people are liking Action,Adventure more than other genre.
3. We also analysed that some director have less movies but they are massive hits as compared to other.

### Data Analysis

1.	Highest Average Voting: Identifying movies with the highest average votes.
	2.	Highest Revenue: Finding movies with the highest revenue.
	3.	Average Rating of Directors: Calculating the average rating of movies by each director.
	4.	Comparison of Movies by Year: Comparing movies released in specific years.
	5.	Runtime Comparison: Comparing movies with the largest and smallest runtime.
	6.	Genre Analysis: Identifying and analyzing movie genres.

 ```python
import pandas as pd

IMDB=pd.read_csv(r"Desktop/IMDB.csv")

IMDB["Revenue (Millions)"]=IMDB[("Revenue (Millions)")].fillna(m)

IMDB[IMDB['Runtime (Minutes)']>=180][["Title","Runtime (Minutes)"]]

IMDB.nlargest(1,'Rating')[["Title","Rating"]]


def classs(x):
    if x>=7.0:
        return "EXCELLENT"
    elif x>=5.0:
        return "GOOD"

    elif x<5.0:
        return "BAD"
```

### Results

This section summarizes the results and conclusions drawn from the analysis of the IMDb dataset. The analysis covers various aspects such as highest average voting, highest revenue, average rating of directors, comparison of movies released in particular years, comparison of largest and smallest runtime, and identifying the exact genre of movies.

1. Highest Average Voting

Result

The movies with the highest average voting were identified. These movies received the highest average ratings from IMDb users.

Conclusion

Movies with the highest average voting are generally critically acclaimed and popular among audiences. They tend to have strong storytelling, high production values, and excellent performances.

2. Highest Revenue

Result

The movies with the highest revenue were determined. These movies generated the most income at the box office.

Conclusion

Movies with the highest revenue are often blockbuster hits. They typically feature popular actors, high budgets, and extensive marketing campaigns. High revenue also suggests a strong audience appeal and widespread distribution.

3. Average Rating of Directors

Result

The average rating of movies by each director was calculated. This analysis provided insights into which directors consistently produced highly rated movies.

Conclusion

Directors with high average ratings are usually recognized for their expertise and vision in filmmaking. They often have a distinctive style and a track record of delivering quality movies. This information can be valuable for identifying influential directors in the industry.

4. Comparison of Movies Released in Particular Years

Result

Movies released in specific years were compared based on various metrics such as average rating, revenue, and genre distribution.

Conclusion

Certain years stood out as particularly strong for the movie industry, with higher average ratings and revenues. This analysis helps identify trends and shifts in the movie industry over time, including changes in audience preferences and industry practices.

5. Comparison of Largest and Smallest Runtime

Result

Movies with the largest and smallest runtime were compared to understand their impact on audience reception and revenue.

Conclusion

Movies with extremely long or short runtimes can have unique challenges and benefits. Longer movies may offer more in-depth storytelling but can risk losing audience engagement. Shorter movies might be more accessible but may struggle to develop complex narratives. Understanding these dynamics can help filmmakers optimize runtime for their target audience.

6. Genre Analysis

Result

The exact genres of movies were identified and analyzed to determine their popularity and impact on ratings and revenue.

Conclusion

Certain genres, such as action, drama, and comedy, tend to be more popular and have higher average ratings and revenues. This analysis helps understand the genre preferences of audiences and can guide future movie production to align with these preferences.
