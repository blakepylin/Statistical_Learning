## Problem 1: What Causes What?

1.  There’s a causality problem, it’s hard to come to a clear conclusion
    just by looking at police force size. Cities with higher than
    average crime rate might hire more police than an average city, this
    might lead to a false conclusion that police are ineffective at
    solving crime. On the other hand, having more police means that
    crime gets more easily detected, this might lead someone to conclude
    crime rates are higher when in fact that might be the same as any
    other city with a smaller police force. Simply put, it’s hard to
    conclude what effect increased policing has on crime.

2.  Basically, the researchers added an IV variable by using the terror
    alert system. High Terror alert means that there will be an
    increased police presence regardless of the amount of crime that’s
    happening in a given area. In their first regression they found that
    a high terror alert is predicted to lower the number of crime by
    about 7 crimes. In the second regression, controlling for metro
    ridership, the high terror alert is predicted to lower the crime
    rate by about 6 crimes.  

3.  The researchers decided to control for metro ridership to make sure
    that the lower crime rate caused by the high terror rate wasn’t
    simply a matter of a smaller amount of people being out and about on
    the street. The researchers were trying to capture the effect that a
    high terror rate could have on the amount of people in the city.

4.  The first column comprises of a linear model using robust regression
    with three coefficients. One of the coefficients looks at the effect
    of a high terror rate solely within the first police district area,
    meaning the national mall. This is because if terrorists were to
    attack Washington, D.C. they would probably focus on this area. The
    next coefficient is the effect of the high alert on the rest of the
    police district areas within DC. The third coefficient is the log of
    midday metro ridership. Basically this regression is showing that
    the high alert (and therefore an increased number of police) lowers
    crime mostly in the National Mall area, the effect in the rest of
    the city isn’t as profound as it is in the other area, even though
    it still lowers crime by a small amount. However, the regression
    still shows strong evidence that more police lowers crime, this is
    because during a high alert the DC police force is probably going to
    increase police the most in district one.

## Problem 2 Tree Modeling: Dengue Cases

### Part 1: CART

![](exercise_3_files/figure-markdown_strict/2-1.png)

The model above shows the un-pruned CART Tree, we will proceed to prune
and then calculate RMSE.

    ## 21.59013  RMSE for Pruned CART Model

### Part 2: Random Forest

![](exercise_3_files/figure-markdown_strict/2%20cont%20again%20-1.png)

This plot shows the out of bag MSE as a function of the number of trees
used. Let’s proceed to look at the RMSE compared to the testing set.

    ## 19.22685  RMSE for Random Forest

### Part 3: Gradient Boosted Trees

![](exercise_3_files/figure-markdown_strict/2%20boosted%20-1.png)

    ## [1] 44

This plot shows the error curve of the Gradient Boosted Model, with the
optimal number of trees listed as output. Let’s now check the RMSE for
the Gradient Boosted Trees Model.

    ## 19.45091  RMSE for Gradient Boosted Trees

Looking at the RMSE results from the three models, it appears that
random forest would be the best choice for this particular set of data.
The next section shows the partial dependency plots for the Random
Forest Model.

### Part 4: Partial Dependency Plots

![](exercise_3_files/figure-markdown_strict/2%20PD%20plots-1.png)![](exercise_3_files/figure-markdown_strict/2%20PD%20plots-2.png)![](exercise_3_files/figure-markdown_strict/2%20PD%20plots-3.png)

### Wrap Up:

Looking at the PD plots, most seem to make sense in the context of the
science of mosquito breeding. Mosquitos require standing water in order
to make baby mosquitos, it makes sense that as precipitation increases,
the number of mosquitos increases, the increased number of mosquitos
leads to more cases of Dengue. The same seems to be true of humidity.
Humidity is a measure of how much evaporated moisture there is in the
air, higher humidity would seem to indicate that there is a higher
amount of water on the ground, and thus the amount of mosquito breeding
grounds. Our wild card PD plot looks at the Average Diurnal Temperature
Range. It shows that as DTR increases, the amount of predicted Dengue
cases decreases. This makes sense as well, it’s possible that
temperature shocks kill mosquitos which leads to less Dengue cases.

## Problem 3: Green Certification

### Introduction

This question asks us to quantify the effect of green certifications on
revenue per square foot in buildings with such a certification. Green
certifications clearly have an environmental impact, but do they also
make buildings more attractive to potential renters, and people pay
attention when buidlings recieve a green certification? We attempt to
answer these concerns below.

### Analysis

#### Data Cleaning

Since we focused on the revenue of the property, we generated a new
variable `revenue` as the product of `Rent` and `leasing_rate`. We
created green\_rating to see the overall impact of green certificate
instead of using both `LEED` and `EnergyStar` (`green_rating` is a
collapsed version of these two ratings). Other important factors that
will affect energy usage are the cooling degree days and the heating
degree days, in our model we used `total_dd_07` to represent this
factor.

#### Modeling

We tried three different models to see which one will yield the best
out-of-sample RMSE, they are CART, random forest, and gradient-boosted
model. We split the data set into training and testing sets, and we
trained all of the three models on training data using all of the
variables.

To tune the gradient-boosted model, we first created a grid that
specifies `shrinkage`, `interaction.depth`, `n.minobsinnode`, and
`bag.fraction`. then ran the gbm across all different combination of
these parameters. After narrowing the tuning grid 2 times, the average
RMSE across 10 folds is still higher than random forest. The final
comparison are shown below.

#### Model performacne

The out-of-sample RMSE of the models: CART: 772.38 Random Forest: 609.07
Gradient-boosted: 683.56

So we decided to use random forest as our best predictive model.

#### Plots

This is the variable importance plot for our random forest model. As you
can see, size, market rent, and age seem to be the biggest factors in
predicting. Our green rating variable is actually show to have the
lowest importance out of all of the parameters.
![](exercise_3_files/figure-markdown_strict/Q3%20-%20VI%20plot-1.png)

As you can see, it appears that green rating is only estimated to
increase revenue by fifty dollars.
![](exercise_3_files/figure-markdown_strict/partail%20plot-1.png)

### Wrap up

After testing three models, we decided to employ random forest. Using
our predictive modeling, we found that green certification doesn’t
really lead to a dramatic increase in revenue. According to our partial
dependence plot, a green certification is only expected to increase
yearly rent revenue (per square foot) by fifty dollars.

## Problem 4: California Housing

#### Modeling

Again in this question we will compare CART, random forest, and gbm to
get the best predictive model. After tuning the gbm model, we get a
out-of-sample RMSE that is smaller than random forest. So the best
predictive model we will use here would be gbm.

Now, we use the gbm model to produce a plot of prediction and a plot of
model’s residuals.

#### Plots

To produce the three plots, first we set up the base plot of California
using the data from the package `maps`.

The plot displays the median house value in California with the colors
becoming brighter as the house value increases. The plot clearly
displays the higher home values of the Los Angeles and San Francisco Bay
Area (including coastal suburbs), having the most concentrated
collection of homes with high values.

![](exercise_3_files/figure-markdown_strict/Q4%20-%20plot%201-1.png)
This plot displays the predicted median house value from our model. As
you can see, compared to the actual data, our model appears to do a good
job at predicting house value.

![](exercise_3_files/figure-markdown_strict/Q4%20-%20plot%202-1.png)
This plot shows the absolute value of the residuals between actual and
predicted values. It appears that most of the errors from our model are
small.
![](exercise_3_files/figure-markdown_strict/Q4%20-%20plot%203-1.png)
