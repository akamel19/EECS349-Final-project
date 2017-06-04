# AP Poll Ranking Learning Algorithm

Completed for Northwestern EECS 349, taught by Professor Doug Downey


Team Members: Justin Savin, Nicholas David, and Aaron Kamel


To contact us please email: justinsavin2019@u.northwestern.edu or nicholasdavid2019@u.northwestern.edu or aaronkamel2019@u.northwestern.edu

### Abstract

College Basketball has quickly become a global pursuit. Every week, enthusiasts from around the world anticipate the release of the AP Poll, a ranking of 25 Division One Basketball teams, indicating the hierarchy in NCAA Division One Basketball. Often the best predictor in whether a team is to make the NCAA tournament, the AP Poll is an amalgamation of votes from hundreds of sports writers, and is thus a data-rich set. Our project centered around the question: Is there a pattern to this data-rich set; specifically, can one model whether a team will be ranked at the end of the season--cementing their place at the top of the college basketball hierarchy--based on common traits of teams that have finished the season ranked?


To begin, we gathered data from [Data World](https://data.world/mkearney/ncaa-mens-cbb-teams) that lists common metrics for evaluating teams--such as win-loss percentage, total number of wins and losses, and strength of schedule--as well as qualitative features, such as school and conference. Using the machine learning software Weka, we ran a variety of classifiers--including ZeroR, Nearest Neighbor, Decision Trees and Naive Bayes. Ultimately the key finding was that the best results surprisingly came from a very simple J48 Decision Tree, consisting of splits at the features “total losses” and “season highest ap poll rank”, shown below. There was some concern that this simple decision tree was in fact a local minimum, and therefore we trained the decision again on the same data set but without the ap_high attribute. This resulted in a very complex tree, thus revealing that the simple J48 tree was not a local minimum. From the simple J48 tree, we can model a team’s likelihood of finishing a season ranked in the AP Poll consistent for 97.42% of the testing data.

![alt text](https://github.com/akamel19/EECS349-Final-project/blob/master/CutTree.jpg?raw=true)
A very simple J48 Decision Tree with splits at "total losses" and "season highest ap poll rank", learned over the data is shown above. This picture illustrates the surprisingly simple J48 Decision Tree which achieves a very high accuracy of 97.42% on the testing data.

You can download a more detailed report of our work here: [Final Report](https://github.com/akamel19/EECS349-Final-project/blob/master/AP%20Poll%20Ranking%20Learning%20Algorithm.pdf)

The project was broken down into smaller pieces:

Nicholas David completed the dataset manipulation and classification.

Aaron Kamel is the host and designer of the final project website.

Justin Savin is the author of final project report.



