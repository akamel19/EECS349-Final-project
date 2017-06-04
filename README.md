### Abstract

College Basketball has quickly become a global pursuit. Every week, enthusiasts from around the world anticipate the release of the AP Poll, a ranking of 25 Division One Basketball teams, indicating the hierarchy in NCAA Division One Basketball. Often the best predictor in whether a team is to make the NCAA tournament, the AP Poll is an amalgamation of votes from hundreds of sports writers, and is thus a data-rich set. Our project centered around the question: Is there a pattern to this data-rich set; specifically, can we model whether a team will be ranked at the end of the season--cementing their place at the top of the college basketball hierarchy--based on common traits of teams that have finished the season ranked?


To begin, we gathered data from DataWorld (https://data.world/mkearney/ncaa-mens-cbb-teams) that lists common metrics for evaluating teams--such as win-loss percentage, total number of wins and losses, and strength of schedule--as well as qualitative features, such as school and conference. Using the machine learning software Weka, we ran a variety of classifiers--including ZeroR, Nearest Neighbor, and Naive Bayes--ultimately yielding the best results from a surprisingly simple J48 Decision Tree, consisting of splits at the features “total losses” and “season highest ap poll rank”, shown below. From this, we can model a team’s likelihood of finishing a season ranked in the AP Poll consistent for 97.42% of our testing data.

![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/CutTree.jpg?raw=true)
A J48 Decision Tree with splits at "total losses" and "season highest ap poll rank", learned over the data

Nicholas David — Dataset manipulation and classification

Aaron Kamel — Host and Designer of final project website  

Jusitn Savin — Author of final project report



