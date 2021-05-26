[![ERDOS image](erdospic.PNG)](<https://www.erdosinstitute.org/>)   [![Big Data Bowl image](https://i.ytimg.com/vi/l-O24EqD4YI/maxresdefault.jpg)](<https://operations.nfl.com/gameday/analytics/big-data-bowl/>) 

# Erdos Institute + NFL Big Data Bowl 2021 Prediction Model
This is a stored repository of data and Python codes for the "Sports Analytics Project" group for the 2021 Erdos Institute.

This project was completed as part of the The Erdős Institute Data Science Boot Camp 2021 and will be submitted to compete in the National Football League’s (NFL) 2020-21 Big Data Bowl. NFL data from the 2018 season was analyzed to provide recommendations and summaries for optimal defensive coverages, first down analysis, and penalty analysis. To successfully create a prediction model that NFL teams can benefit from, it is important to understand football and its related data. This will allow data scientists to identify significant data for building a model.    

**Football for Non-Football Data Scientists**

Football is a sport where two opposing teams are competing over possession of the football and field position. The goal of the offense is to gain at least 10 yards every four downs (plays) to prevent turnovers and eventually score while the goal of the defense is to prevent these gains and secure turnovers. 

If a more in-depth overview is required, click the image below to watch an explanatory YouTube video provided by the NFL: 

[![Football Explanation Video](https://i.ytimg.com/an_webp/3t6hM5tRlfA/mqdefault_6s.webp?du=3000&sqp=CLDJuYUG&rs=AOn4CLBY4SnWw-IhXIwHTGD-BB979Kw5NA)](<https://www.youtube.com/watch?v=3t6hM5tRlfA>)

An explanation of the 4-3 vs 3-4 defense: 

[![Basic defensive schemes Explained](http://img.youtube.com/vi/watch?v=6s2QL0rn2UI.jpg)](https://www.youtube.com/watch?v=6s2QL0rn2UI)

Explanation of Coverage Schemes can be seen here: 

[![Coverage Schemes Explained](http://img.youtube.com/vi/watch?v=PdN7T_OzAKw/0.jpg)](https://www.youtube.com/watch?v=PdN7T_OzAKw)


# Goals

**1. Optimal Defensive Coverages:**

Passing plays are the most efficient way for the offensive team to gain field position. Over the course of its history, the NFL has increasingly become a passing focused league. The chart and table below show the increasing efficiency of pass plays vs run plays over the years:

![](Aspose.Words.0ca85fb4-e76c-4d3e-9a00-dc367f0e2769.001.png)


![](Aspose.Words.0ca85fb4-e76c-4d3e-9a00-dc367f0e2769.002.png)

Above data provided by: (<https://www.pro-football-reference.com/>)

NFL teams went from averaging 85 passing yards per game in the 1930s to 234 passing yards per game in 2010-2020. The increases in average passing yards occurred while average rushing yards have decreased at a stagnant rate. Because of this, it is important to find out which defensive coverages perform the best at limiting passing success. 

EPA is the difference between the Expected Points (EP) at the start of a play and the EP at the end of they play. EPA is the measure of a play’s impact on the score of the game. An individual player’s EPA is the sum of the EPA of the plays in which that player was directly involved. Being directly involved is defined as an offensive player who ran, threw, or kicked the ball, was targeted by a pass, or flagged for a penalty (<https://www.advancedfootballanalytics.com/index.php/home/stats/stats-explained/glossary>).

GOAL: 

Significant data from the 2018 NFL season will be analyzed to find out which defensive coverages result in the smallest EPA and smallest average passing yards to provide recommendations and summaries for optimal defensive coverages.


**2. First Down Analysis:**

As explained earlier, an offense has four downs or fewer to advance the 10 yards required to gain a first down, which allows them to maintain possession and earns them another four downs. The initial down in a series of downs is called a first down (<https://operations.nfl.com/learn-the-game/nfl-basics/terms-glossary/>). The goal of the offensive team is to secure first downs and eventually score, while the goal of the defensive team is to prevent first downs and to secure turnovers. Because of this, it is important to find out which offensive formations are best at securing first downs and which defensive formations are best at preventing first downs.

GOAL:

Analysis will consist of examining factors such as quarter, down, yards to go, play result, play type (pass or sack), and offensive and defensive personnel from the 2018 NFL season to find out the first down success percentage of different offensive and defensive formations. 

**3. Penalty Analysis:**

When either the offense or defense violates the rules of the game, they are assessed a penalty. The teams and fans know a penalty has been called when an official throws a yellow flag on the field (<https://operations.nfl.com/learn-the-game/nfl-basics/terms-glossary/>). Penalties award field position to either the offensive or defensive team based on which team committed the penalty. Penalties range from 5 yards, 10 yards, 15 yards, to potentially the entire length of the field when it comes to pass interference. Because of this, it is important to find out which formations are generally prone or averse to committing penalties. 

GOAL:

Analysis will consist of examining data from the 2018 NFL season to find out which offensive and defensive formations are more or less likely to commit penalties. Moreoever, we want to predict penalties based on week 1 player tracking data as well as predict defensive pass interference (DPI) using a more comprehensive approach. 

# Models

**1. Bagging:** machine learning process that takes several weak models and aggregates the predictions to select the best prediction. 

More info here: https://towardsdatascience.com/ensemble-methods-bagging-boosting-and-stacking-c9214a10a205. 

**2. Support Vector Machine (SVM):** The objective of the support vector machine algorithm is to find a hyperplane in an N-dimensional space(N — the number of features) that distinctly classifies the data points. 

More info here: https://towardsdatascience.com/support-vector-machine-introduction-to-machine-learning-algorithms-934a444fca47.

**3. K-Nearest Neighbors (KNN):** an algorithm that stores all the available cases and classifies the new data or case based on a similarity measure. It is mostly used to classifies a data point based on how its neighbours are classified. 

More info here: <https://towardsdatascience.com/a-simple-introduction-to-k-nearest-neighbors-algorithm-b3519ed98e>. 

**4. Logistic Regression:** uses a logistic function to model a binary dependent variable. 

More info here: <https://towardsdatascience.com/introduction-to-logistic-regression-66248243c148>. 

**5. Random Forest:** consists of a large number of individual decision trees that operate as an ensemble. Each individual tree in the random forest spits out a class prediction and the class with the most votes becomes our model’s prediction. 

More info here: <https://towardsdatascience.com/understanding-random-forest-58381e0602d2>. 

**6. Adaboost:** initially created to increase the efficiency of binary classifiers, it uses an iterative approach to learn from the mistakes of weak classifiers, and turn them into strong ones. 

More info here: <https://blog.paperspace.com/adaboost-optimizer/#:~:text=AdaBoost%20is%20an%20ensemble%20learning,turn%20them%20into%20strong%20ones>. 

And here: <https://towardsdatascience.com/understanding-adaboost-2f94f22d5bfe>. 



**7. Gradient Boosted Classifier:** each predictor tries to improve on its predecessor by reducing the errors, but instead of fitting a predictor on the data at each iteration it actually fits a new predictor to the residual errors made by the previous predictor. 

More info here: <https://towardsdatascience.com/gradient-boosting-classification-explained-through-python-60cc980eeb3d>. 

**8. LSTM Neural Net:** a specific recurrent neural network (RNN) architecture that was designed to model temporal sequences and their long-range dependencies more accurately than conventional RNNs. 

More info here: <https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21>. 

And here: <https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43905.pdf>. 

# Model Performance: 

**First Down Model**: 

**Penalties Model**: 

The gradient boosted classifier outperformed other models in terms of recall score. 
* **Logistic Regression**: Recall=0.71 with cutoff at 0.1
* **Random Forest**: Recall=0.75 
* **Gradient Boosted Classifier**: Recall=0.78 

Recall was the metric of choice due to the imbalanced target variable. We wanted to make sure that the model captured 
enough of the flagged target data. 

**DPI Model**: 
