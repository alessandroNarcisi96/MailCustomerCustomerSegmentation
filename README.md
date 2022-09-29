# MailCustomerCustomerSegmentation

## Introduction
Customer segmentation is important for businesses to understand their target audience. Different advertisements can be curated and sent to different audience segments based on their demographic profile, interests, and affluence level.<br/>
The dataset that I am going to use is provided by Udacity.<br/>
We have some basic data about your customers like Customer ID, age, gender, annual income and spending score.
Spending Score is something you assign to the customer based on your defined parameters like customer behavior and purchasing data.<br/>

## Why could it be useful for a company?
Customer segmentation is an excellent way to gain insight into the market landscape.<br/> 
Customer segmentation is all about grouping customers into segments based on shared qualities or characteristics.<br/>
Once we have this information a company could lead more effective market campaign as they are built on a specific target.

## Milestone 1: EDA

### Does Gender affects the Spending Score?
Let's get started by describing the proportion between males and females.<br/> 
As we can see the dataset is quite balanced.<br/> 
There are 112 females and 88 males.<br/> 
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/gender_barplot.png)<br/>

If we compare the distribuition against the Spending score we can see that for a low level of Spending score there are more males.<br/> 
Apart that they are quite similar.<br/> 
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/spendingScore.png)
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/spendingScore_gender.png)<br/>
<p align="center">
  <img src="https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/boxplot_gender.png" alt="Sublime's custom image"/>
</p>


### Does Age affects the Spending Score?
At the plot shows below people who are younger than 40 years tend to spend more.<br/> 
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/Age_SpendingScore.png)<br/>

### Does Income affects the Spending Score?
Let's group the income in range.<br/> 
The small green triangle shows the mean and as we can see all the means are very close each other.<br/> 
We can conclude that the income is not a powerfull predictor to divide people in cluster but if we compare the variability of the 0,3 and 4 boxplot is very small.<br/> 
This could be interesting because it could mean that in those case there are some specific characteritics.<br/> 
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/IncomeRange.png)<br/>