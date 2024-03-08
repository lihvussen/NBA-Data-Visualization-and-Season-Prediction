This project consists of two parts. 

In the first one, 'NBA', NBA data from Kaggle (https://www.kaggle.com/datasets/nathanlauga/nba-games/data) is visualized in details, in various ways. Particular stats leaders 
in both sums and averages are presented, teams' performances in last 20 years are also shown and compared. The visualization provides a very deep impact
on the main actors and phenomena in the most powerful basketball league in the world. The visualizations are preceded by extensive data cleaning and preprocessing process.

The second part 'Season_prediction' aims at predicting outcome of 2021/2022 regular season by predicting the outcome of each game. The analysis starts with the same preprocessing steps.
Then, new valuables are created, such as performance of each team in last games, win percentage in last 2 seasons, normalized strength while playing at home or away, etc.. The model is trained
on the data from last 20 seasons. The architecture of the model is deep neural network created with the use of keras and tensorflow libraries. The prediction is obtained in 2 different ways.

The first one simply predicts the outcome of each game with the factual temporal data - the accuracy obtained by this model is around 70% and the mean average error for the number of wins
of each team is around 8.5 which is not bad considering the 82-games season in the NBA. Some teams win number is computed almost perfectly, however sometimes this error is significant.

The second prediction pattern is more complex. After each gameday it updates the features which describe current state of each team, such as last game performance. This, however biases further
predictions as some teams, probably the ones who were 'expected' to win many of the intial games, are predicted to win almost every game while others to lose vast majority of them.
Mean average error in this case reaches 24, which is significant and proves that this approach, without important adjustments, might be errouneous.
