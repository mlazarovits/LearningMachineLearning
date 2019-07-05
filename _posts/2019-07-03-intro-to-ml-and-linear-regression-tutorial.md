---
title: "7/3/19: Intro to ML and Linear Regression Tutorial"
---

This week, we split our time between learning about the mathematical basis of machine learning with Professor Chris Rogan and applying this basis in a Python tutorial with Dr. Sadia Khalil.

Professor Rogan gave a brief review of Bayes' theorem from last week, reiterating the purposes of the prior and likelihood. He then introduced the idea of error. One way to calculate the error between the true value and the predicted value is with the mean squared error (MSE). This error is the sum of the squared difference between the true and predicted values. 

Two concepts that relate to the error (or loss) of the model we are testing are variance and bias. Variance tells us how well the model can be generalized to data it has not seen before. Bias tell us how closely the model fits the data we are testing it on. Complicating the model (ie going from a linear to a quadratic model) can reduce the bias by more closely fitting the model to the test data. However, the more a model fits the test data, the less likely it is able to be generalized to new data. Therefore, there is a trade off betweeen the bias and variance. A good model should fit the test data well, but not well enough that it cannot be generalized to more data. This balance introduces the concept of overfitting, which is a potential downfall of machine learning techniques.

{% capture fig_img %}
![Foo]({{"/assets/images/ML4timing_NNdiagram.png" | relative_url}})
{% endcapture %}

<figure>
	{{fig_img | markdownify | remove: "<p>" | remove: "</p>"}}
	<figcaption>A neural network diagram from a talk Margaret gave on using neural networks for precision timing purposes at the CMS detector.</figcaption>
</figure>

After discussing these mathematically-rooted machine learning concepts, we turned to a more concrete example of machine learning, specifically the neural netowkr (NN). A neural network is comprised of nodes (or neurons) where inputs are summed with specific weights. This sum is transformed by a non-linear activation function before it is outputted from this node and combined with other outputs into the next layer, and so on. The most popular activation functions are the sigmoid and rectified linear unit (ReLU) functions. The goal of a neural network is to learn the optimal weights to apply to each input at each node. Loss functions, like the MSE, are functions that tell us how close our NN predictions to the true values.

Next, Dr. Sadia Khalil walked us through [two linear regression tutorials](../../../MLresources), which are both in Jupyter notebooks under the Tutorials section of the ML resources page. [The first](https://github.com/skhalil/DataScience/blob/master/Regression/LinearRegressionTutorial/linearRegIntro.ipynb) is a simple linear regression that calculates the predicted values by minimizing the MSE to create a linear model. You can play around with the input data to see how more linear data changes the MSE and R^2 values. [There is another tutorial](https://github.com/skhalil/DataScience/blob/master/Regression/LinearRegressionTutorial/linearRegSklearn.ipynb) that performs a linear regression to real world data from the S&P 500 Index. This is a good, economics-focus application of one of machine learning's most fundamental concepts.