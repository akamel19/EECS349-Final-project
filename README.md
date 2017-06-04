### Abstract

College Basketball has quickly become a global pursuit. Every week, enthusiasts from around the world anticipate the release of the AP Poll, a ranking of 25 Division One Basketball teams, indicating the hierarchy in NCAA Division One Basketball. Often the best predictor in whether a team is to make the NCAA tournament, the AP Poll is an amalgamation of votes from hundreds of sports writers, and is thus a data-rich set. Our project centered around the question: Is there a pattern to this data-rich set; specifically, can we model whether a team will be ranked at the end of the season--cementing their place at the top of the college basketball hierarchy--based on common traits of teams that have finished the season ranked?


To begin, we gathered data from DataWorld (https://data.world/mkearney/ncaa-mens-cbb-teams) that lists common metrics for evaluating teams--such as win-loss percentage, total number of wins and losses, and strength of schedule--as well as qualitative features, such as school and conference. Using the machine learning software Weka, we ran a variety of classifiers--including ZeroR, Nearest Neighbor, and Naive Bayes--ultimately yielding the best results from a surprisingly simple J48 Decision Tree, consisting of splits at the features “total losses” and “season highest ap poll rank”, shown below:

![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/Screen%20Shot%202017-06-01%20at%204.34.54%20PM.jpg?raw=true)

As shown above, a J48 Decision Tree has the greatest accuracy, precision, and recall when trained over the data and evaluated via 10-Fold cross validation. We therefore chose to adopt a J48 Decision Tree with splits at the features “ap_high” and “l”; a graphic depiction of our tree, as well as quantitative results when applied to the Testing Data, are shown on the next page.

![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/Tree.jpg?raw=true)


![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/Weka%20Tree.jpg?raw=true)

From this, we can model a team’s likelihood of finishing a season ranked in the AP Poll consistent for 97.42% of our testing data.

Nicholas David — Dataset manipulation and classification

Aaron Kamel — Host and Designer of final project website  

Jusitn Savin — Author of final project report



