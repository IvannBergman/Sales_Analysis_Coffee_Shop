# **Data Analysis For Coffee Vending Machine's Sales Data**

## Intro
In this project, I took a deep dive into the sales data of a coffee vending machine for a 6 month period.

The dataset contains 1208 unique transactions spanning from 2024/03/01 to 2024/08/08 with the below attributes:
  * Transaction date
  * Transaction date & time
  * Transaction type (Cash or Card)
  * Card number
  * Sales amount
  * Product name

Link to Kaggle dataset: [Coffee Sales](https://www.kaggle.com/datasets/ihelon/coffee-sales?resource=download)

I'll use _Python_, _Microsoft SQL Server_ and _Microsoft PowerBI_ to ingest, process, visualize and analyze the dataset to answer key business questions relevant to the sales performance, product performance and the customer base's behaviour.

## Goals
  * To create an end-to-end solution for ingesting, storing and surfacing the data.
  * To expand the dataset by inferring additional dimensions to further slice the data.
  * To provide metrics to articulate the performance of the vending machine in an easy to understand format.
  * To answer key business questions.
   
## Analysis
 ### Sales Overview:
 
  *Page Preview:*
   ![image](https://github.com/user-attachments/assets/e5f5b18b-8c22-436a-8370-819e1768c3e6)

   *Q:* What is the total revenue? How many customers did it serve? How many beverages did it sell?

   *A:* From March 2024 to August 2024 the machine sold a total of 1208 beverages to 564 different customers which equated to a total revenue of 39.66k. These figures average out to 201 beverages, 94 customers and 6.61k revenue monthly.

   *Q:* What is the sales trend for the period? And, given the trend, what will the next few days look like? - And next month?

   *A:*  
   ![image](https://github.com/user-attachments/assets/0f01494e-4fb1-4633-a67b-d9a8fbb44052)

   The trend fluctuates between March and May, with May being a clear outlier on the high-end. The trend stabilizes in June and July with a difference of 10 units between the periods.

   ![image](https://github.com/user-attachments/assets/c02b4e24-838b-401e-91e1-8331361452ee)

   For the remainder of August, the forecast is positive, indicating an increase of sales around the 19th through to the 28th.

   ![image](https://github.com/user-attachments/assets/18766d72-aee3-40fd-864b-39ee03aa171a)

   The forecast indicates that September returns to the June/July plateau.

   *Q:* What's the vending machine's performance compared to the previous month? Is the machine's sales growing?

   *A:*  
   ![image](https://github.com/user-attachments/assets/32da1d12-c9e1-49ee-9ed2-b650a63e895a)

   Overall, growth is positive with an average of 17% month-on-month and in terms of performance, it achieves 16% over target month-on-month.

   *Q:* What is the machine's busiest day? And time of day?

   *A:*  
   ![image](https://github.com/user-attachments/assets/ce999c2f-9a38-46b5-a59e-68646ced7594)

   Thursdays and Fridays are the busiest overall and Tuesdays the slowest. The difference between the slowest and busiest days are around 23%.

   Afternoons - 12pm to 4pm are the busiest, and Nights - 8pm to 11pm, are the slowest with the difference between highest and lowest being 123%

 ### Product Overview:
  *Page Preview:*
   ![image](https://github.com/user-attachments/assets/86022476-8923-4bf5-a645-5fa499a61c2b)

   *Q:* Which products are the best and worst sellers?

   *A:*  
   ![image](https://github.com/user-attachments/assets/bc02747d-a18e-4ce3-9594-c8cc59c74bbf)

   Americanos is the best seller and Espressos, the worst. Interestingly, Americanos with milk are more favoured than without, and that beverages without milk are less favoured across the board.

   *Q:* When does it sell what product the most?

   *A:*  
   ![image](https://github.com/user-attachments/assets/67c7f30d-577f-48fa-9d42-a9d7e66a8350)

   Americanos both in the Morning - 7am to 11am, and Afternoons - 12pm to 4pm, are the best seller and converesely, Cocao being the worst seller across all time groups.

   *Q:* How much did the prices change over time? How was the sales volume affected by the changes?

   *A:*  
   ![image](https://github.com/user-attachments/assets/5539a58d-ff46-41f9-a678-9d01a934d924)

   Between March and June, the average price of beverages was more-or-less consistent, July saw a relatively large drop-off at around 5 _Currency_ which remains consistent in August.

   With the stable average price of beverages, and the fluctuations in volume from March to June, and the subsequent decrease in price, and slight increase in volume for July: it would seem that the influence of product price is low to none on the volume of sales made.

 ### Customer Behaviour:
  *Page Preview:*
   ![image](https://github.com/user-attachments/assets/81fb64fe-8e89-4be2-92ce-0a2c8efb5af8)

   *Q:* Who purchases the most?

   *A:*  
   ![image](https://github.com/user-attachments/assets/27eb2fc4-5f32-4fab-ac3d-d69298bbcff7)

   There are 179 customers who purchased from the vendiing machine more than once, with the top 10 purhcasing 12 or more times.

   *Q:* How consistent is the customer's purchasing habits?

   *A:*  
   ![image](https://github.com/user-attachments/assets/5cc6cb6e-e38f-4ed3-b8e7-89036a84ef97)

   Relatively consistent with the average purchase consistency being around 76%, and average visits per customer being 3 over the period.

   *_Purchase consistency is measured how often the customer bought their most frequently purchased product and visits being measured as how many times a customer returned on different dates_*

   *Q:* Can we recommend similar products to returning customers?

   *A:*  
   ![image](https://github.com/user-attachments/assets/18214214-4b3b-4503-b235-355d236be102)

   Yes, the recommendations is based off the dimensions of a customer's frequent product purchases and recommends the most popular product fitting the same dimensions and time of purchase.
