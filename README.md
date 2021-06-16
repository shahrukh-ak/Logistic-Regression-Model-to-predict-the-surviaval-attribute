# Logistic-Regression-Model-to-predict-the-surviaval-attribute-
Performing analysis on Famous Titanic Data and fitting Logistic Regression to predict the survival attribute.

## Libraries Used
<ul>
  <li>pandas</li>
  <li>numpy</li>
  <li>matplotlib</li>
  <li>seaborn</li>
</ul>
## Exploratory Data Analysis
Let's begin some exploratory data analysis to check out missing data!

## Missing Data
Seaborn is used to create a simple heatmap to see where we are missing data!

![1](https://user-images.githubusercontent.com/55116845/122254443-8ee36800-cee6-11eb-8387-2ff2a1d115de.png)

Roughly 20 percent of the Age data is missing. The proportion of Age missing is likely small enough for reasonable replacement with some form of imputation. Looking at the Cabin column, it looks like we are just missing too much of that data to do something useful with at a basic level. We'll probably drop this later, or change it to another feature like "Cabin Known: 1 or 0"

Let's continue on by visualizing some more of the data!

![2](https://user-images.githubusercontent.com/55116845/122254866-01ecde80-cee7-11eb-981b-5064bd054bd8.png)

![3](https://user-images.githubusercontent.com/55116845/122255137-44162000-cee7-11eb-8e5a-6cc39dde7565.png)

![4](https://user-images.githubusercontent.com/55116845/122255261-65770c00-cee7-11eb-90c1-a15234a8b8ec.png)

![5](https://user-images.githubusercontent.com/55116845/122255453-8e979c80-cee7-11eb-8cf6-72175c95f436.png)

![6](https://user-images.githubusercontent.com/55116845/122255485-99523180-cee7-11eb-885d-eebf65932820.png)

![7](https://user-images.githubusercontent.com/55116845/122255518-a2db9980-cee7-11eb-8c36-db57f3c5cce1.png)

![8](https://user-images.githubusercontent.com/55116845/122255565-b0911f00-cee7-11eb-8c72-fea55efcc582.png)

## Cufflinks for plots

Let's take a quick moment to show an example of cufflinks!

## Data Cleaning
We want to fill in missing age data instead of just dropping the missing age data rows. One way to do this is by filling in the mean age of all the passengers (imputation). However we can check the average age by passenger class. For example:

![9](https://user-images.githubusercontent.com/55116845/122256527-986dcf80-cee8-11eb-99de-a9997c869ccb.png)

Wealthier passengers in the higher classes tend to be older, which makes sense. Used these average age values to impute based on Pclass for Age.

Now let's check that heat map again!

![10](https://user-images.githubusercontent.com/55116845/122257227-3e213e80-cee9-11eb-9fa6-45a0cb350a2e.png)

Now dropped the Cabin column and the row in Embarked that is NaN.

## Converting Categorical Features
Converted categorical features to dummy variables using pandas. Otherwise our machine learning algorithm won't be able to directly take in those features as inputs.

![T2](https://user-images.githubusercontent.com/55116845/122259777-f3ed8c80-ceeb-11eb-8b94-5bb674586b23.PNG)

Now our data ready for our model!

## Building a Logistic Regression model
<ul>
  <li>Splited our data into a training set and test set .</li>
  <li>Training and Prediction of model.</li>
  <li>Model Evaluation</li>
  </ul>
  
## Results
Checking precision,recall,f1-score using classification report!

![R1](https://user-images.githubusercontent.com/55116845/122260661-f69cb180-ceec-11eb-91c7-49e2ce33b274.PNG)













