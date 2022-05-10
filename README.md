**Assignment-1**

**Team No.**: 97

**Team Name**: Team Caffeine

**Team Members**: Gautam Ghai (2020101020), Lavisha Bhambri (2020101088)

**Task-1 : LinearRegression().fit()**

The LinearRegression() in sklearn module creates a linear prediction model by selecting a set of coefficients

w=(w1,…,wn)

and a bias b to minimise the residual sum of squares between the actual targets in the training dataset, and the targets predicted by linear approximation of the features.

LinearRegression() takes a few parameters which help to decide certain features of the linear model. The LinearRegression().fit() is the function which finds the optimal values of the intercepts where the arguments are the existing input(training dataset). It creates the model to fit the training dataset. The coefficients are initialised by the fit() method to the most optimum values by minimising the Mean Squared Error between the training data and the predicted data. The .fit() function fits any instance of linear regression.

**Task-2 : Calculating Bias and Variance**

The following graphs depict the predicted values against the original testing values. As can be seen from the following graphs, the worst overlap for predicted and original values is for polynomials of degrees 1 and 2 while it is the best for polynomials with degrees 3-5. So our prediction is that the function most likely represents a polynomial of degree 3 or 4 or 5.

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.001.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.002.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.003.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.004.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.005.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.006.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.007.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.008.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.009.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.010.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.011.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.012.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.013.png)![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.014.png)

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.015.png)

If we observe the bias and variance for polynomials from degree 1 to 15 we notice that the bias is high for degrees 1 and 2 (which implies underfitting) and then it abruptly falls for degree=3 and then it remains nearly constant for a while until it starts to slowly increase for higher degrees.

As for variance, it keeps on increasing from degree 1 (where we have an underfitting model) to 15 (where we have an overfitting model). We need to find the right tradeoff between variance and bias to avoid both underfitting and overfitting. From the following table we can infer that the right tradeoff will be for degrees 3 or 4 or 5.

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.016.png)

**Task-3 :  Calculating Irreducible Error**

Irreducible error is the error that cannot be reduced by creating good models. It is a measure of the amount of noise in the data.

E[(f (x) − f ˆ (x))2 ] = Bias2 + σ2 + Variance

σ2 = E[(f (x) − f ˆ (x))2] − (Bias2 + Variance)

where f (x) represents the true value,

f ˆ (x) represents the predicted value,

[E[(f (x) − f ˆ (x))2 ] is the mean squared error (MSE) and

σ2represents the irreducible error.

For almost all cases from degree 1 to 15, the irreducible error remains close to 0. Ideally irreducible error should be 0 but some small amount of error arises due to the presence of noise in virtually every data.

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.017.png)

**Task-4 : Plotting Bias2 − Variance graph**

We observe that the bias drops suddenly from degree=2 to degree=3 then remains about the same and then for higher degrees it starts increasing gradually. As for the variance it gradually increases from degree 1 to 15 and the error drops steeply from degree 2 to 3 and then increases. In short the model moves from underfitting to overfitting with the minimum error at degree=3. Thus we conclude that the data is best fitting for a model with degree=3 as the error is the least and it shows that a good tradeoff exists between bias and variance.

![](./images/Aspose.Words.29fcc3ea-4231-4c0a-bc75-1778a4f97f02.018.png)
