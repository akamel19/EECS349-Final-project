### Abstract

Our project is called AP Poll Predictor for NCAA Basketball and was created for Northwestern University's EECS 349 Machine Learning course taught by Doug Downey. The creators of the project are Nicholas David, Justin Savin and Aaron Kamel, and if you would like to contact them please email justinsavin2019@u.northwestern.edu or nicholasdavid2019@u.northwestern.edu or aaronkamel2019@u.northwestern.edu.
What is the task, and why is it important/interesting?
Describe your approach in high-level terms: what kind of learner(s) did you use, what types of features did you use?
Describe the key results (how well your solution performed in no more than a paragraph, along with your key findings, e.g. which learners performed best, which features were most important)?

### Our Task

College Basketball has quickly become a global pursuit. Every week, enthusiasts from around the world anticipate the release of the AP Poll, a ranking of 25 Division One Basketball teams, indicating the hierarchy in NCAA Division One Basketball. Often the best predictor in whether a team is to make the NCAA tournament, the AP Poll is an amalgamation of votes from hundred of sports writers, and is thus a data-rich set. Our project centered around the question: Is there a pattern to this data-rich set; specifically, can we model whether a team will be ranked at the end of the season--cementing their place at the top of the college basketball hierarchy--based on common traits of teams that have finished the season ranked?
	To begin, we gathered data from DataWorld (https://data.world/mkearney/ncaa-mens-cbb-teams) that lists common metrics for evaluating teams--such as win-loss percentage, total number of wins and losses, and strength of schedule--as well as qualitative features, such as school and conference. Using the machine learning software Weka, we ran a variety of classifiers--including ZeroR, Nearest Neighbor, and Naive Bayes--ultimately yielding the best results from a surprisingly simple J48 Decision Tree, consisting of splits at the features “total losses” and “season highest ap poll rank”, shown below:
	
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


