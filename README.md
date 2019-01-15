# Wikidata, Movies, and Success
In this project, we would like to know what makes a movie successful. In this particular case we would consider a movie is successful if it makes profit. For this project, we have the choice in using Python with Panda or Spark in Python. We ended up using Python with Panda, as there are not much data to process We used Jupyter Notebook as it is easier to display and check the result and graph.

### Summary of study and result
The first thing we tried to find out is whether the audience reviews and critics reviews correlate with each other. We used linear regression to see this, and to validate the result, we had to check if the residual of the two reviews are normally distributed. From our investigation, we know that the reviews are linearly correlated to each other and this statement is true as the residual is pretty much normally distributed. In the future, to ensure that it is indeed normally distributed, we have to do normality test.

The next question that we tried to understand is whether we can predict if a movie made profit just by using their average 'ratings'. We did supervised learning for this specific problem. We set the 'ratings' as the unlabeled observation X, and set the 'made profit' as the predicted labels y. We used three different models for the prediction which all three gave "good" accuracy at 0.8 range. We discovered that there is sample imbalance in this in which there are more movies that make profit which is about 80% of the total sample. We decided to fix this sample imbalance by dropping the sample that made profit, so that the percentage of both samples are about 50-50. After fixing this, we tried scoring the prediction again but unfortunately, the score could only reach 0.7 which is not good enough. We concluded that it is not possible to predict if a movie going to be successful just based on the ratings.

For the last part, we would like to know if the movies that made profit has higher rating. We used Mann-Whitney-U test on both ratings. The p-value was lesser than 0


### Dependancies
- Jupyter Notebook
- Pandas
- scikit-learn
- seaborn

### Data
- Wikidata Movies
- Rotten Tomatoes

### Running
The following command will open the web browser
```
 $ jupyter notebook project.ipynb
```
You would be able to run the project using the interface on a browser
