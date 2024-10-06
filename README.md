# Predicting Listing Gains in the Indian IPO Market using TensorFlow

## Project Overview:

This project involves building a deep learning classification model to predict listing gains in Initial Public Offerings (IPO) in the Indian market. Listing gains refer to the percentage increase in the share price of a company from its IPO issue price on the day of listing. The goal of the model is to determine whether an IPO will list at a profit based on historical data.

The dataset used for this project was sourced from Moneycontrol and contains information about past IPOs in the Indian market. We followed the standard modeling pipeline: starting with exploratory data analysis, visualizing key variables, and creating a deep learning classification model using TensorFlow.

## Steps Involved

**1. Loading the Data**
We loaded the dataset containing details of past IPOs, which includes key variables such as the issue price, retail subscription, and whether the IPO resulted in a listing gain.

**2. Exploring the Dataset**
During exploratory data analysis, we observed that:

- 55% of the IPOs listed at a profit.

- The data is relatively balanced, with a near-equal number of profitable and non-profitable IPOs.

- We also dropped variables that may not carry predictive power.

**3. Data Visualization**
Key findings from data visualizations:

- Outliers are present in the data, which required outlier treatment.

- The boxplot of Issue_Price with respect to Listing_Gains_Profit showed more outliers for IPOs that listed at a loss.

- A correlation was observed between Retail Subscription and Total IPO Subscription via a scatterplot.

**4. Outlier Treatment**

We used the interquartile range (IQR) method for outlier identification and treatment. The values of the affected variables were clipped between their respective upper and lower bounds to mitigate the effect of outliers. Other outlier treatment methods could also be explored.

**5. Setting the Targets and Predictor Variables**

We set up the dependent variable as target_variable (whether an IPO lists at a profit or not) and created a list of predictor variables. Given the varied distributions of the predictors, we applied normalization to scale all variables between 0 and 1 to ensure consistency during model training.

**6. Holdout Validation Approach**

We split the dataset using the **holdout validation** approach, with a **70:30 ratio**:

- 70% of the data was used for training.

- 30% of the data was reserved for testing the model on unseen data.

**7. Defining the Deep Learning Classification Model**

We used TensorFlow’s Keras Sequential API to define the deep learning model. The model includes:

- Four hidden layers using the ReLU activation function.

- A sigmoid activation function in the output layer for binary classification (profit vs. non-profit).

Feel free to experiment with different architectures, activation functions, and numbers of nodes in each layer.

**8. Compiling the Model**

We compiled and trained the model on the training data using binary cross-entropy as the loss function, optimizing with the Adam optimizer.

**9. Model Evaluation**

The model achieved an accuracy of:

- 75% on the training set.
- 74% on the test set.

The close accuracy values between the training and test sets indicate the model's consistency and its ability to generalize well to unseen data.

## Conclusion 

In this project, we built a deep learning classifier using TensorFlow’s Keras API to predict listing gains in Indian IPOs. The model achieved a solid accuracy of 75% on training data and 74% on test data, showing consistent performance. This classifier provides a promising approach for investors to assess whether an IPO will result in a profit on its listing day.

## Tools and Library 

TensorFlow and Keras for building and training the deep learning model.
Pandas, NumPy, Matplotlib, and Seaborn for data exploration and visualization.

## Contact

[Email](@pratikshabj77@gmail.com)

[LinkedIn](https://www.linkedin.com/in/pratikshabajpai29/)










































