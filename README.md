### Abstract

Our project is called AP Poll Predictor for NCAA Basketball and was created for Northwestern University's EECS 349 Machine Learning course taught by Doug Downey. The creators of the project are Nicholas David, Justin Savin and Aaron Kamel, and if you would like to contact them please email justinsavin2019@u.northwestern.edu or nicholasdavid2019@u.northwestern.edu or aaronkamel2019@u.northwestern.edu.

College Basketball has quickly become a global pursuit. Every week, enthusiasts from around the world anticipate the release of the AP Poll, a ranking of 25 Division One Basketball teams, indicating the hierarchy in NCAA Division One Basketball. Often the best predictor in whether a team is to make the NCAA tournament, the AP Poll is an amalgamation of votes from hundred of sports writers, and is thus a data-rich set. Our project centered around the question: Is there a pattern to this data-rich set; specifically, can we model whether a team will be ranked at the end of the season--cementing their place at the top of the college basketball hierarchy--based on common traits of teams that have finished the season ranked?
	
To begin, we gathered data from DataWorld (https://data.world/mkearney/ncaa-mens-cbb-teams) that lists common metrics for evaluating teams:


school--Name of the Division One college basketball program.


conf--Name of the Division One college basketball conference a program is a part of. 


w--Number of games a Division One basketball team won in a specific year.


l--Number of games a Division One basketball team lost in a specific year.
 
 
wl--Win Loss Percentage, calculated by dividing the number of wins a Division One basketball team won in a specific year by the number of total games played.
 
 
srs--A ranking that takes into account average point differential and strength of schedule. The rating is denominated in points above/below average, where zero is average. Non-Division One games are excluding from the ratings.
 
 
sos--Strength of Schedule; a measure of how “difficult” a schedule is by denominating points over or under average, where zero is average. Non-Division One games are excluding from the ratings.
 
 
pts_for--Average points scored per game by a Division One basketball team.
 
 
pts_vs--Points scored against per game by a Division One basketball team.
 
 
pts_total--Summation of pts_for and pts_vs.
 
 
ap_pre--A number, 1-25 or 30 (not ranked) indicating whether a Division One basketball team was ranked to start the season and--if so--what a team’s rank was.

 
ap_high--A number, 1-25 or 30 (not ranked) indicating the highest rank on the AP Poll a Division One basketball team reached in a given season.
 
 
pts_diff--A difference between pts_for and pts_vs.
 
 

A multitude of steps were taken to best prepare this data for analysis. The first of which was to eliminate any extraneous variables—such as rk, ncaa_result, and coaches—not listed above so as to maintain accuracy, relevance, and functionality within Weka experiments. Additionally, to avoid oversimplification, we created a binary variable “ranked_final?” which displays a 1 if a Division One Basketball team is ranked following the final week of the regular season, and 0 if not. Inclusion of the ranked_final? attribute brings the total number of features to 14.  

After modifying the data and features, we divided our data into two subsets: Testing Data and Training Data. The Training Data records all entries for the teams recorded up through the 2013-2014 season, and consists of 5,827 entries. Similarly, the Testing Data records all entries in during the 2014-2015 and 2015-2016 seasons, and consists of 620 entries. 

To determine the best classifier for the data, we trained a variety of learners over the Training Data, evaluating their performance using 10-Fold cross validation. The results are summarized below:

![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/Screen%20Shot%202017-06-01%20at%204.34.54%20PM.jpg?raw=true)

As shown above, a J48 Decision Tree has the greatest accuracy, precision, and recall when trained over the data and evaluated via 10-Fold cross validation. We therefore chose to adopt a J48 Decision Tree with splits at the features “ap_high” and “l”; a graphic depiction of our tree, as well as quantitative results when applied to the Testing Data, are shown on the next page.

![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/Tree.jpg?raw=true)

From this, we can model a team’s likelihood of finishing a season ranked in the AP Poll consistent for 97.42% of our testing data. 

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).


