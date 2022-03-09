# Customer-Segmentation-Project

# I - Introduction
### Problem Statement
[Project Proposal](https://github.com/aliatabay1/Customer-Segmentation-Project/blob/main/Capstone%20Two%20-%20Project%20Proposal.pdf)

The marketing team is struggling to determine how to create personalized campaigns according to customers’ needs. As the data team, our goal is to gain insights from the customer data and eventually cluster them accordingly to help the marketing team develop more personalized campaigns. 

![This is an image](https://www.segmentify.com/wp-content/uploads/2021/08/Top-Customer-Segmentation-Examples-every-Marketer-Needs-to-Know.png)

### II - Data Wrangling

[Data Wrangling](https://github.com/aliatabay1/Customer-Segmentation-Project/blob/main/Notebooks/Data%20Wrangling.ipynb)

This project used customer data from Kaggle. The dataset contains 2240 customers and 29 features. Initially, some cleaning needed to be done to make the dataset more coherent. The income column had some missing values so they were filled with the mean of this column. 

Also, some feature engineering was made. Expenses on different products were combined under the new column Total_Expenses. The age column was generated using customers’ date of birth information. Values in Education and Relationship Status columns were edited to ease the analysis. 

Finally, Age and Income column had some outliers which were removed to achieve more statistically significant results. 

### III - Exploratory Data Analysis

[EDA](https://github.com/aliatabay1/Customer-Segmentation-Project/blob/main/Notebooks/Exploratory%20Data%20Analysis.ipynb)

<img src="https://user-images.githubusercontent.com/91096434/157329732-a022f966-2db1-4069-9879-5e4287ba4e9b.png" width="400">

The graph indicates that  %72.8 of customers didn't accept any promotion at all, 16.5% of customers accepted a promotion in the first offer. This shows that current promotions are not effective. Our goal is to increase this effectiveness by creating more personalized and data-driven campaigns.

<img src="https://user-images.githubusercontent.com/91096434/157329954-9620fdc3-3399-42a5-9ac2-c9b39757b9e5.png" width="400">

Interestingly, there is a negative correlation between the number of children in a household and total expenses. The reason behind this might be having products more suitable for single people. 

![image](https://user-images.githubusercontent.com/91096434/157502553-d4fffb22-b188-4cdd-9419-887ea1d55e0e.png)

Another surprising correlation is between the number of monthly web visits and total expenses. Customers visiting the company’s website more, spend less on the products. The reason may stem from ineffective online sales and marketing strategies.



### IV - Modeling
[Modeling](https://github.com/aliatabay1/Customer-Segmentation-Project/blob/main/Notebooks/Modeling.ipynb)

After getting insight and interesting information from data in EDA, the next step was applying unsupervised learning algorithms to form clusters. 

After comparing silhouette scores for k-means and hierarchical clustering, I found that k-means performs better and decided to proceed with it.     

To find out what is the optimal k value for my algorithm, I used elbow and the silhouette methods. 

<img src="https://user-images.githubusercontent.com/91096434/157326027-4677f8dd-3ef4-4e06-9cb0-216421cbf780.png" width="400"> <img src="https://user-images.githubusercontent.com/91096434/157326724-6f7874b3-c735-4cc3-94ef-63d8e4e2abc0.png" width="400">

Both graphs indicated that 2 is the optimal number of clusters.

After clustering customers, I explored different features to decide what are the most important features we should focus on to produce more personalized marketing campaigns.

![image](https://user-images.githubusercontent.com/91096434/157330948-96e762cd-57d9-4fc3-9be0-ebead1c464de.png)![image](https://user-images.githubusercontent.com/91096434/157330968-6d4ec8fb-ddc6-4cab-b4e6-a7bef8709e80.png)
![image](https://user-images.githubusercontent.com/91096434/157331016-c1a0f26e-b199-4c3b-9f72-7f858efd4264.png)![image](https://user-images.githubusercontent.com/91096434/157331077-f6df1ff5-c5b2-445b-827b-90ce0d0f0e16.png)
![image](https://user-images.githubusercontent.com/91096434/157331102-7875b9e4-e930-4ebb-a433-b46194e609ba.png)![image](https://user-images.githubusercontent.com/91096434/157331121-6e7d775c-bba4-41fc-bc04-cbda5058a8ed.png)
![image](https://user-images.githubusercontent.com/91096434/157331133-69dd0cd6-eef0-4e30-8f4d-5933fe4c0c7f.png)![image](https://user-images.githubusercontent.com/91096434/157331156-3ce8a9d6-d3d5-44a3-a967-6dd530d79779.png)
![image](https://user-images.githubusercontent.com/91096434/157331195-180fef66-22fa-469f-bd3a-e7a97c301215.png)![image](https://user-images.githubusercontent.com/91096434/157331226-b6ec3104-220d-4ab8-8bd3-d2aa7d771115.png)


### Cluster 0 
- High socioeconomic status
- Very high total expenditure
- Moderate marketing campaign acceptance rate
- More web purchases
- Less monthly web visits
- Fewer discount purchases
- More store purchases
- Slightly more educated
- Relatively older population
- 
### Cluster 1:
- Lower socioeconomic status
- Significantly lower total expenditure
- Low marketing campaign acceptance rate
- Fewer web purchases
- More monthly web visits
- More discount purchases
- Fewer store purchases
- Slightly less educated
- Relatively younger population

### V - Conclusion

### Cluster 0 - Marketing Strategy 
- Promoting company’s website
- Emailing the information of newly arrived items
- Creating customer loyalty rewards program 
- Ask them why they are choosing our products


### Cluster 1 - Marketing Strategy 
- Increasing the customer experience on the website and making the purchasing process less time consuming
- Promoting the discounted items by sending emails and displaying them in the main page of the website
- Advertising how our products different from the competitors by using feedback of Cluster 0


Image Source: https://www.segmentify.com/blog/top-customer-segmentation-examples-every-marketer-needs-to-know
