#### Homework 1

In Example 1.2 we evaluate the effects of the number of markers used on prediction accuracy. The data is partition at random into a training and a testing data sets. The training data set is used to build models and the testing data set is used to evaluate the ability of these models to predict phenotypes of individuals whose data was not used to build models (see [Piccard & Cook, 2912]( http://amstat.tandfonline.com/keyword/Optimism%20Principle) for further discussions about validation procedures ).

The models are build by first ranking markers based on GWAS and then estimating effects using OLS for the top 1, 2,….,300 markers. Each of these models are then evaluated based on their prediction accuracy in the testing set. The last plot shows how the correlation between y and yHat in the testing data sets varies as more markers are added to the model.

The curve generated by the example is an estimat. As with any other estimate there is uncertainty about it, namely that if we were able to go to the population and sample a different training and testing set we will obtain a different curve simply due to sampling variance.

Resampling methods can be used to assess uncertainty and to produce better estimates. We can try to ‘mimic’ the process of sampling from a population by executing example 1.2 multiple times each time with a different partition of the data into training and testing. This can be done by running, say, example 1.2 1,000 times, each time you store the curve (a vector of sqCorTST, for this you probably will need to create a matrix to store these curves as rows of that matrix) and then you plot all these curves in a single plot and also the average curve in a single plot.

**Assignment**:

	* Implement the re-sampling procedure above described
	* Submit by Monday 10:00am  a ppt or a pdf with your final plot and your code.

**Note**: I’ll randomly draw a name and this person will need to explain what he/she did and discuss the results.
