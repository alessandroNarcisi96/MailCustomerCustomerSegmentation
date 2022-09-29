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
On the left we see the general distribuition whereas on the left we divide it by gender,red for females and green for males
As we can see they are quite similar,but the men's distribuition appears more uniform than the female's distribuition<br/> 
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/spendingScore.png)
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/spendingScore_gender.png)<br/>
The following boxplot it's important because we compare the mean of two groups.
It is indicated by the small green arrow.
They are on the same level so it means that the gender is not enough to cluster the data.
The only good news is that the lowest spending scores belong to men
<p align="center">
  <img src="https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/boxplot_gender.png" width="400" height="300" alt="Sublime's custom image"/>
</p>


### Does Age affects the Spending Score?
As the plot shows below people who are younger than 40 years tend to spend more.<br/> 
So in this case we have a very good feature to cluster people<br/> 
![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/Age_SpendingScore.png)<br/>

### Does Income affects the Spending Score?
Let's group the income in range.<br/> 
The small green triangle shows the mean and as we can see all the means are very close each other.<br/> 
We can conclude that the income is not a powerfull predictor to divide people in cluster but if we compare the variability of the 0,3 and 4 boxplot is very small.<br/> 
This could be interesting because it could mean that in those cases there are some specific characteritics.<br/> 
<p align="center">
  <img src="https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/IncomeRange.png" alt="Sublime's custom image"/>
</p>

## Milestone 2: Clustering
A very common algorithm to divide the datapoints in clusters is KMeans.<br/>
The image below explains the effect.<br/>
<p align="center">
  <img src="https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/cluster.png" alt="Sublime's custom image"/>
</p>
Basically the goal is dividing data in groups.<br/>
Inside of each cluster we find the centre of the cluster called centroid.<br/>

### How many clusters?
In this algorithm  we have to decide in advance the number of cluster.<br/>
Once we found it, KMeans will optimize the grouping by minimizing the sum of squares of the distance of the datapoints from the centroid.<br/><br/>

But the question is still there:how can we find the number of clusters?<br/>
A very famous method is elbow method.<br/>
The logic is explained by these lines of code<br/>

![alt text](https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/code.png)<br/>

we define a raange of cluster and we evaluated which one divide better the datapoints.<br/>
In this case to measure the goodness I will use the inertia.<br/>
It is the sum of squared distances of samples to their closest cluster center.<br/><br/>

Let's plot the result
<p align="center">
  <img src="https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/elbow.png" alt="Sublime's custom image"/>
    <img src="https://github.com/alessandroNarcisi96/MailCustomerCustomerSegmentation/blob/master/images/cluster3d.png" alt="Sublime's custom image"/>

</p>