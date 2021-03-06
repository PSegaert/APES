# The Simpson Paradox - an example

As we discussed in class already (i.e., dataset on lung capacity: models predicting LungCap depending on Smoke habits, and eventually getting opposite estimates of the effect of smoke depending on whether we included confounding factors or not), here we deal with another example of the Simpson paradox.

To learn more about the Simpson paradox, see https://en.wikipedia.org/wiki/Simpson%27s_paradox


# Example 1 - part I.

Load the dataset (regrowth1A)

```r
setwd("~/TEACHING IN FREIBURG/11 - Statistics with R fall 2015/11_the Simpson paradox")
regrowth = read.delim("regrowth1A.txt")
head(regrowth)
```

```
##   Fruit  Grazing
## 1 59.77 Ungrazed
## 2 60.98 Ungrazed
## 3 14.73 Ungrazed
## 4 19.28 Ungrazed
## 5 34.25 Ungrazed
## 6 35.53 Ungrazed
```

Experiment details:
Our worked example concerns an experiment on the impact of grazing on the fruit production of a biennial plant. 
Forty plants were allocated to two treatments, grazed and ungrazed, and the grazed plants were exposed to rabbits during the first two weeks of stem elongation. They were then protected from subsequent grazing by the erection of a fence and allowed to regrow. At the end of the growing season, the fruit production (dry weight in milligrams) was recorded on each of the 40 plants.
Two columns in the dataset:
Grazing: 2 levels (Grazed, with rabbits), (Ungrazed, no rabbits)
Fruit: weight of fruits produced by the plant (dry weight in milligrams)

Question 1. Identify the predictor (independent variable) and the response variable. Make a plot to visualize the relationship between these two variables.


Question 2. Run a proper statistical procedure to disentangle the effect of the indipendent variable on the response.



Question 3. How do you interpret the results you just obtained?





#Example 1 - part II.

Well. Let's say that we collected a confounding factor in this experiment.
Because initial plant size was thought likely to influence fruit production, the diameter of the top of the rootstock was measured before each plant was potted up.
Root: diameter of the rootstock right before the beginning of the experiment
Now load the proper dataset with the full experiment.

Load the dataset (regrowth1A)

```r
setwd("~/TEACHING IN FREIBURG/11 - Statistics with R fall 2015/11_the Simpson paradox")
regrowth = read.delim("regrowth1B.txt")
head(regrowth)
```

```
##    Root Fruit  Grazing
## 1 7.225 59.77 Ungrazed
## 2 6.487 60.98 Ungrazed
## 3 5.219 14.73 Ungrazed
## 4 5.130 19.28 Ungrazed
## 5 6.417 34.25 Ungrazed
## 6 5.359 35.53 Ungrazed
```

```r
attach(regrowth)
```

Question 1. 
You now have Root, Fruit, and Grazing. What affects what?


Question 2. 
Fit a proper statistical procedure which takes the structure Y ~ x1 + x2, where Y is the response (dependent) variable, x1 and x2 are the independent predictors.
Plot the predictions of the model without using the effects library




Simone Ciuti, Uni Freiburg. 29.10.2015. Dataset (modified) taken from Mick Crawley, The R Book, Second Edition.



