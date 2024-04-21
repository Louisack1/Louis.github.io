# [Capstone-Case-Competition](https://github.com/Louisack1/Louis.github.io)
Demand Analysis & Forecasting

# Swire's Product Demand Forecasting
Project Overview
This project is designed to accurately forecast the demand for Swire's limited-release products. By predicting sales volumes accurately, Swire can prevent overproduction and out-of-stocks, ensuring optimal production quantities that align with consumer demand trends.

# Business Problem
The primary challenge is to develop robust predictive models using historical sales data to forecast product demand effectively, which will help Swire to enhance revenue growth and operational efficiency.

# Solution Overview
Our approach combines exploratory data analysis (EDA) with several predictive modeling techniques, including linear regression, K-nearest neighbors (KNN), decision trees, and ARIMA forecasting implemented in R to determine future product demand.

# Recommendation
6-month demand for Diet Energy Moonlit Cassava 2L Multi Jug:

Demand Prediction: 15,000 units
Production Recommendation: 11,000 units

# Contributions
**Louis Ackumey:** Handled the Business problem statement, KNN modeling and contributed to the EDA.

# Business Value
The project enables Swire to minimize production costs and optimize inventory levels, leading to better resource management and enhanced profitability.

# Challenges Encountered
Dealing with sparse data for some product categories was challenging for model training.
Balancing technical model complexity with ease of interpretation for non-technical stakeholders was critical.

# Learnings
The project enhanced our understanding of advanced forecasting techniques and their application in solving real-world business problems. It also underscored the importance of teamwork and effective communication in data science projects.



# [Business Problem and Benefits](https://github.com/Louisack1/Louis.github.io)
The primary business problem is to accurately forecast demand of Swire’s limited-release products, preventing both out-of-stocks and overproduction, and ensuring optimal production quantities that align with evolving consumer preferences. Achieving this goal will help Swire drive revenue growth and cost savings, expand market reach, and maintain a competitive edge in response to evolving consumer preferences and industry dynamics.

# Success Metrics 
Success metrics may evolve pending discussion with Swire. Preliminarily, the metrics below will be used, and compared to the performance of a model using the data’s average demand.
### 1. Forecast Accuracy
●	Evaluate precision using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE), providing insights into the predictive model’s accuracy.
### 2. Cost Optimization
●	Assess the reduction in costs due to production inefficiencies and overproduction
●	Assess the revenue impact of improved production planning and inventory management

# Analytics Approach
This problem is a supervised regression problem, where the target variable is demand over a period of time. The questions posed by Swire vary in character, but are all based on a desire to predict product performance (demand) over a period of time. The EDA and modeling process will explore the data available and a variety of modeling methods (ARIMA, linear regression, etc.) to determine the most useful inputs and methods. 

# Scope
Swire has provided seven different questions (tabulated below) they hope to have answered. Group 1 has chosen to focus on Questions 2, 4, 6, and 7 to provide specific answers. These questions will be answered using an analytical model developed using the data provided by the Swire team. Depending on the performance of the model on test data, other questions may also be answered.. An output that may be added is a sensitivity of demand to the input factors, allowing the company to understand the model more - similar to an explainable-AI approach.

# Question
1. Which 13 weeks of the year would this product perform best in the market?
2. Swire plans to release this product 2 weeks prior to Easter and 2 weeks post Easter. What will the demand be, in weeks, for this product?
3. Which 13 weeks of the year would this product perform best in the market?
4. Swire plans to release this product for the duration of 1 year but only in the Northern region. What will the demand be, in weeks, for this product?
5. Swire plans to release this product for 13 weeks, but only in one region. Which region would it perform best in?
6. Swire plans to release this product for 6 months. What will the demand be, in weeks, for this product?
7. Swire plans to release this product in the Southern region for 13 weeks. What will the demand be, in weeks, for this product?

# Details and Milestones
This project will be executed by the members of Group 1 within the Capstone Completion class, MSBA program at the University of Utah. This project will be presented on April 21, 2023, with intermediate milestones of an EDA summary (February 25), and a completed model with performance metrics (March 24). 

# [Exploratory Data Analysis.html](https://github.com/Louisack1/Louis.github.io)
### Summary
The EDA focusing on the geographical aspects of the dataset gave us insights into the sales and consumer behavior across different regions. Here’s a summary of the key findings:

Population Distribution: The Western region has the largest population, followed by the Southwest, with the Northern region having the smallest population among the three. This demographic information sets the stage for understanding the market potential in each region.

Price Variation by Market Key: The analysis indicates that there is not much variation in the price of products when segmented by market keys across different regions. This suggests that pricing strategies might be consistent across regions or that market keys do not significantly influence pricing variations.

Regional Price Differences: Despite the overall consistency in pricing, the Northern region has the highest average price for products. This could be indicative of different consumer preferences, higher willingness to pay, or a different mix of products being more popular in the Northern region compared to others.

Sales vs. Population Size: The sales volume in the Southwest, despite having almost double the population of the Northern region, does not have proportionally higher sales. This suggests that customers in the Northern region might be more valuable.

Consumption Patterns of Diet vs. Regular Products: There wasn’t a significant difference in the consumption patterns between diet and regular versions of products. This was surprising, as it was expected that regular variants would greatly outpace diet. This finding could reflect broader consumer trends towards healthier lifestyles or suggest that diet products have gained notable (and possibly changing) acceptance among the population.

The higher average price and relatively strong sales in the Northern region, despite its smaller population, highlight an opportunity to focus on high-value customers and premium product offerings in this area. Meanwhile, the widespread acceptance of both diet and regular products suggests that there is a broad market for various product types, and strategies should not necessarily favor one over the other without further market research. These geographical insights, combined with further analysis of seasonal trends, can help in crafting more more accurate forecasts for Swire.

## Graph Interpretation:
### Insight from Box Plot Analysis:
The box plot analysis of the average unit prices reveals intriguing patterns. Primarily, it indicates that the average price is significantly influenced by the order quantity and the type of packaging used. Notably, energy soda emerges as a higher-priced item compared to other types. The presence of outliers in the data suggests extreme values that are genuine variations rather than errors, providing important cues for accurate prediction without the need for imputation.
![](/images/Boxplot-Average%20Price%20for%20top%203%20Package%20Categories.png)

### Average price was highest in the Northern region:
![](/images/Average%20Price%20By%20Region-Graph.png)

### Sales over time by Region:
![](/images/Sales%20Over%20Time%20by%20Region%20graph.png)

### Count of Caloric Segment by Region:
![](/images/Count%20of%20Caloric%20Segment%20by%20Region-Graph.png)

### Forecasts from Region with ARIMA(0,0,0)(0,1,0)[52) errors:
![](/images/ARIMA%20forecast-Graph.png)

# [Models.html](https://github.com/Louisack1/Louis.github.io)
