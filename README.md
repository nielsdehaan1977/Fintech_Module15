# Fintech_Module15

![roboAdvisor.jpg](https://github.com/nielsdehaan1977/Fintech_Module15/blob/main/Images/roboAdvisor.jpg)
---
# RoboAdvisors using AWS
---
## 


---
### This github repository is create to help create a Robo advisor in Amazon Lex and enhance the robo advisor with an Amazon Lambda function it with the Amazon Lambda function which can use Python code to for example validate the user's input and returns an investment portfolio recommendation.

---
The github account can help to create and to test Robo advisor build in Amazon Lex
* This Readme will go through on the following steps: 
1. Configure the initial robo advisor: Define an Amazon Lex bot with a single intent that establishes a conversation about requirements to suggest an investment portfolio for retirement.
2. Build and test the robo advisor: Make sure that your bot works and accurately responds during the conversation with the user.
3. Enhance the robo advisor with an Amazon Lambda function: Create an Amazon Lambda function that validates the user's input and returns the investment portfolio recommendation. This includes testing the Amazon Lambda function and integrating it with the bot.

---
## Table of Content

- [Tech](#technologies)
- [Usage](#usage)
- [Contributor(s)](#contributor(s))
- [License(s)](#license(s))

---
## Tech

This project leverages python 3.9 and Jupyter Lab with the following packages:

* `Python 3.7`
* `Amazon Lex`
* `Amazon Lambda'

* [Amazon_Lex](https://aws.amazon.com/lex/) - Build chatbots with conversational AIb

* [Amazon_Lambda](https://aws.amazon.com/lambda/) - Run code without thinking about servers or clusters

---

## Usage

To use the venture funding with deep learning jupyter lab notebook, simply clone the full repository and open the **venture_funding_with_deep_learning.ipynb** file in Jupyter Lab. 

The tool will go through the following steps:

### Establish a Baseline Perfomance
* import of data to analyze
* generate trading signals using short- and long-window SMA values
* split the data into training and testing datasets
* review classification report associated with the SVC model predictions
* create a predictions dataframe
* create a cumulative return plot that shows the actual returns vs the strategy returns

### Tune the baseline Trading Algorithm
* tune the training algorithm by adjusting the size of the training dataset
* tune the trading algorithm by adjusting the SMA input features.

### Evaluate a new machine learning classifier
* import a new classifier
* using the original training data as the baseline model, fit another model with the new classifier.
* backtest the new model to evaluate its performance.

## Contributor(s)

This project was created by Niels de Haan (nlsdhn@gmail.com)

---

## License(s)

MIT

---
# Evalution Report
---

## Baseline Performance

The baseline strategy performance was not impressive with a loss of about 30% based on historical data used. Strategy was based on generatinge trading signals using short- and long-window SMA values. Baseline SMA values were 4 periods for the short sma and 100 periods for the long sma. Strategy signals were set to 1 if return was equal or larger than 0 and -1 if return was smaller than 0. 

![Baseline_Strategy_returns.jpg](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/Baseline_Strategy_returns.jpg)

---

## Tune Baseline Trading Algorithm

While trying to improve the results of the baseline strategy, we adjusted the model's input features to find the parameters that result in better trading outcomes.
The following parameters were changed and the results are below:

The SVM model with 3M of training data and SMA_short at 4 periods and SMA_long at 100 periods for the most part of 2019 and 2020 performed better than the actual returns. Also when changing the amount of training data to 6M the strategy ultimately outperforms the actual returns. For the model with 6M training data the actual returns outperform the strategy returns for most of 2019, but outperforms the actual returns from March 2020 onwards. With a total return of about 80% whereas the model with 3M training data "only" produces about 50% return. 

1. adjusting the training window from 3 months to 6 months

While changing the training window from 3m to 6m:
* accuracy of the model increased by 1 point from  0.55 to 0.56. 
* Precision for -1 increased by 1 point from 0.43 to 0.44
* Recall for -1 decreased from 0.04 to 0.02

---
![Image_of_3m_class](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_class_report_3m_training_data_SMAFast_4_SMASlow_100.jpg)  ![Image_of_6m_class](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_class_report_6m_training_data_SMAFast_4_SMASlow_100.jpg)

![Image_of_3m_training](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_plot_3M_training_and_SMAFast_4_SMASlow_100.png)

![Image_of_6m_training](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_plot_6M_training_and_SMAFast_4_SMASlow_100.png)

---
2. adjusting the SMA input features 
---
2a. adjusting SMA short to 2 and SMA long to 50

While changing the SMA window to 2 and 50:
* accuracy of the model decreased by 1 point from  0.55 to 0.54. 
* Precision for -1 decreased by 4 points from 0.43 to 0.39
* Recall for -1 increased from 0.04 to 0.07

![Image_of_3m_class_2_50](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_class_report_3m_training_data_SMAFast_2_SMASlow_50.jpg)
![Image_of_3m_SMAFast_2_SMASlow_50](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_plot_3M_training_and_SMAFast_2_SMASlow_50.png)

---
2b. adjusting SMA short to 1 and SMA long to 25

While changing the SMA window to 1 and 25:
* accuracy of the model decreased by 1 point from  0.55 to 0.54. 
* Precision for -1 decreased by 1 points from 0.43 to 0.42
* Recall for -1 increased from 0.04 to 0.13

![Image_of_3m_class_1_25](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_class_report_3m_training_data_SMAFast_1_SMASlow_25.jpg)
![Image_of_3m_SMAFast_1_SMASlow_25](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/svm_plot_3M_training_and_SMAFast_1_SMASlow_25.png)

---

## Evaluate a New Machine Learning Classifier

For the evaluation of how a different machine learning classifier would perform compared to the provided baseline model, the logistic regression model was used for the comparison. and the model was ran with 3M of training data and SMA_short of 1 period and SMA_long of 25

While changing the SVM model to Logistic Regression Model (SMA 1 and 25):
* accuracy of the model was the same at 0.54. 
* Precision for -1 increased by 1 points from 0.42 to 0.43
* Recall for -1 increased from 0.13 to 0.16

![lr_class_report_3m_training_data_SMAFast_1_SMASlow_25.jpg](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/lr_class_report_3m_training_data_SMAFast_1_SMASlow_25.jpg)
![lr_plot_3M_training_and_SMAFast_1_SMASlow_25.png](https://github.com/nielsdehaan1977/Fintech_Module14/blob/main/Images/lr_plot_3M_training_and_SMAFast_1_SMASlow_25.png)

Based on the above evaluation methods, the model as is does not seem to have very good predictive capacities. All the changes to the orginal model did not have a very big impact overall, unfortunately the changes did not result in significant impovements. We cannot recommend using the model as is for algorithmic trading purposes. 