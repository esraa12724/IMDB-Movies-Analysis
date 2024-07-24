# IMDB-Movies-Analysis
As my first Data Analysis Project. I created this project in order to  analyze movies data and come out with insights that may help producers to choose which type or language to choose for their upcoming movies, and who are the best actors to be chosen.
After analyzing the obtained data, we must be able to:
•	Have vision about which country produces the most movies
•	Know which language is viral in movies
•	Understand which movie genres are most produced
•	Indicate how movie gross change over time
•	Know which years saw the highest number of movies released
•	Detect the correlation between Number of movies produced in each country and IMDB score 

Data Life cycle we passed through
1_ Obtaining data from IMDB Website
2_ Scrubbing and cleaning data through three steps
•	Checking the validity of numeric data by using if condition (=IF(ISNUMBER(M3), "Number", "Not a Number"))
•	Checking duplicated data by using conditional formatting tool (profit column)
•	Checking missing values by using conditional formatting tool (language - plot keywords)
•	Filtering USA produced movies in English as both of them created outliers.
3_ Exploring Data and Interpreting
To explore data, we Had to transfer the project purpose into question and start exploration 

To answer which country produces the most movies?
To answer these questions, we created a pivot table contained (Countries – count of movies) , and the output showed that the united states has the highest number of produced movies (2792), which reflected the heights budget, gross and profit
And after filtering USA production in English UK came on the top of the list with 290 movie and USA produced only 17 in other languages.


To indicate which language is viral in movies produced?
To answer these questions, we created a pivot table contained (Languages – their count) , and the output showed that English has the highest number of produced movies (2792), which reflected the heights budget, gross and profit
And after filtering USA production in English it was 578 movie produced in other countries.
To know which movie genres are most produced
I used function =SUMPRODUCT(--(ISNUMBER(SEARCH("Comedy", SUBSTITUTE(A2:A1000, "|", " "))))), and replaced “comedy” with each category
And the data showed that Drama Category came in the first place with 1754 movie
Indicating how movies financial indicators change over time
And To know which time - range saw the highest number of movies released
To have clear clue about movies whole financial indicators I needed to calculate profit indicator using =SUM([@gross]-[@budget])
I had to classify the time series into time range contains 10 years in order to analyzing it easily, and for this I used function =INT(O3/10) *10 & "-" & (INT(O3/10) *10 + 9)
To answer these questions, I created a pivot table contained (Classified Years – Budget -Gross – Profit – Movie count) , and the output showed that the time – period (2000 – 2009) has the highest number of produced movies (1629), and through the chart we can see the growth of movies financial indicators over years 



 


To detect the relation between Number of movies produced in each country and IMDB score for this country movies
I had to calculate the correlation coefficient, and it was -0.67 which means negative relation between the two indicators, as the number of movies increases the avg of IMDB Score decreases 
 

As directors need to know who are the top actors to achieve gross in movies and attracts audience, 
To indicate this, I created pivot table and then filtered top 5 actors to achieve gross and Harrison Ford came on the top of the list
 

Problems Faced me 
•	I wanted to know which movie type is viral, but is was hard to use Counta function as the movie was classified into more than one category that is why I used SUMPRODUCT function as mentioned.

•	USA/ English was the top in language and countries producing movies and it was an outlier, so I filtered USA English movies production to be able to detected count of English movies produced by other Countries and USA productions in other languages

