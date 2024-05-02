# Olist Store Exploratory Data Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Tools](#tools)
- [Plan of Action](#plan-of-action)
- [Model View](#model-view)
- [Final Report](#final-report)
- [Review Insights](#review-insights)
- [Delivery Insights](#delivery-insights)
- [Recommendations](#recommendations)

### Project Overview

Olist Store is the largest department store in Brazilian marketplaces, connecting small businesses across Brazil to various channels with ease. We have been provided with a public dataset of orders made at Olist Store from 2016 to 2018, and our task is to explore and analyse this data and provide insights as well as data-backed recommendations for the client. We will accomplish this by creating a Power BI report/dashboard with visualisations that answer key questions like the company’s customer demographics, sales trends, orders by categories, order changes by year, etc.

### Tools

- Power BI

### Plan of Action

The area I chose to cover was order changes by year and, more specifically, the reviews and delivery sections. I loaded the nine csv files from Kaggle one by one to the Power BI desktop app. I then transformed and cleaned each of the nine tables using the Power Query editor and loaded them into Power BI. The insights I was looking for were: what was the cause of the 1-star reviews, and what was the main cause of the late deliveries? To answer these questions and develop insights, I used data from order reviews, orders, order items, product category name translation, customers, and geolocation tables. In cases where a table didn’t have the exact data I was looking for, I created a calculated column or a new measure to get specific values. Some of the measures I created included total reviews, number of sellers, and total orders. To make sure that I could create a graph from data in multiple different tables, in the model view, I changed all cross-filter directions to both directions.

### Model View

Many of the tables were automatically connected to each other. The only two that weren’t were the geolocation table and the product category name translation table. Using the schema, I connected these to the correct tables.
![image](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/e81184e4-6151-4e10-89cf-27d26eda37fb)
<br>
<br>

# Final Report
![Screenshot 2024-03-18 101439](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/b8b79f50-f279-410b-9714-5325ced0782d)

![Screenshot 2024-03-18 112126](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/da385058-436e-40a9-b67f-2432b3d067f5)

![Screenshot 2024-03-18 101532](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/0189c399-93ac-4446-8f93-2c55aa1ec3c4)

![Screenshot 2024-03-18 112226](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/b12bae3f-f707-4a1b-9fff-43e6ae5c048a)

![Screenshot 2024-03-18 101626](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/e266811c-6698-4451-bead-f345cd3550de)
<br>
<br>

### Review Insights
![image](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/7e13a52e-51b4-4d1e-a477-fc28ef243e87)
The total amount of reviews for the Olist ecommerce site was 99K. The average review score of all the products sold was 4.09 which is on the higher end of the scale and indicates that Olist have good quality products and a good customer experience. However, this number isn’t a perfect 5, suggesting there’s still room for improvement. The percentage of 5-star reviews took up the majority with 58% of the total 99K reviews. The second highest was 4-star reviews with 19% and then surprisingly 1-star reviews with 11% and then 3-star and then 2-star. This makes sense as people tend to have extreme opinions about products, either loving or hating them which is reflected in the tree map. The average review score in 2016 was 3.54 as the company was just starting out. This number grew to 4.09 in 2017 and was maintained in 2018. Overall, this number reflects the company’s growth and improved customer satisfaction.

![image](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/48895aa5-36d9-4924-b98c-64bd73423518)
I created a column chart showing the count of orders from 2016 to 2018. Along with this I plotted a line chart of the number of 1-star reviews given in the same time frame. The results show a very similar trend in both the graphs. The most popular period for orders were in 2017 Q4, 2018 Q1, and 2018 Q2. The same goes for the line chart. You can see as the demand for products skyrocketed, more people were getting unhappy maybe due to a product being out of stock, it not being delivered on time/received, or the seller cutting corners and the product not being up to quality which caused more 1-star reviews. The product not being received was confirmed by the tree map on the left which shows the top 30 comments for 1-star reviewers. The most popular kinds of comments translated to “nao recebi o product” which means “I didn’t receive the product”. There is a very clear need for Olist to work on their delivery system.


### Delivery Insights

![image](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/2099fe62-b56b-4714-8180-d0ac2f485fa5)
The total amount of orders was 113K over the three years. The total amount of product deliveries was 96.46K. The average delivery time from the product being purchased to the customer getting it was 12 days. The average order processing time was 11.5 Hours. This number is quite good and can lead to higher customer satisfaction as customers generally appreciate quick order processing. The total amount of carrier late deliveries was 7827. This last number is quite significant as it is 8% of the total amount of deliveries which can affect a lot of customers. The line chart shows the average number of shipping days versus the review score from 1 to 5. There is a strong negative correlation between the two. As the average number of shipping days decreases, the review score increases. This makes sense as people tend to review the whole experience and delivery is a part of this. Therefore, a quicker delivery means a happier customer.

![image](https://github.com/faray003/Data-Analyst-Project-2/assets/167533153/c5e5ef7a-3aea-4aae-9f6d-cab01490b573)
To find out what parts of the year these late deliveries were happening I created a column chart that showed the count of orders by year and quarter. I then created a donut chart that showed the percentages of late deliveries versus early deliveries. I used the column chart to filter through the donut chart. The results showed that 74% of late deliveries occurred in the 3 highest peaks of the column chart where the rate of orders was the highest. As the number of orders were so high, the delivery companies weren’t as efficient or optimised as they could be and couldn’t keep up with the demand which led to a lot more late deliveries.


### Recommendations

Reviews Recommendations:
- The number one step is to look at all the 1-star reviews and what people have to say. The people who dislike your product will tell you exactly what parts they dislike which you can then take into consideration and use to improve your product. Once you solve that issue all those negative reviews will turn into positive reviews as you will have solved their major pain point. Dashboards can be used to identify patterns in customer review messages which can then alert you if it becomes too significant. This is much more efficient than manually sifting through thousands of comments week by week. Lots of customers were complaining that their orders never arrived, so if the live dashboard picked up on this you can communicate with the delivery company on why that happened, or you can switch to a more reliable carrier company through mindful research.

Delivery Recommendations:
- To improve, Olist can introduce delivery drop off points (product lockers) in each state. Instead of deliveries having to find optimum routes for each customer’s house location, they can go to a centralised location where all products are dropped off. The customer can then be notified with a code that their order has arrived and travel to the drop off point to collect it. This will significantly decrease the delivery time as the carrier has only one route they always take, and the customer will be a lot more satisfied with this fast drop off and pick up.
