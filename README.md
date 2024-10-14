# **Customer Lifetime Value (CLV) Prediction Model for the Motor Industry**

This article explores the **Customer Lifetime Value (CLV) Prediction Model** with detailed numerical explanations and interpretations of key metrics. We’ll look at **model performance, actual vs. predicted CLV**, and how different variables—such as **purchase channels, loyalty, and average spend—impact CLV**.

---


![image](https://github.com/user-attachments/assets/3eb6e0c1-5cd2-4a49-bb61-0eb4719126f0)


## **Table of Contents**

1. [Introduction](#introduction)  
2. [Objectives](#objectives)  
3. [Key Insights](#key-insights)  
4. [Data Overview](#data-overview)  
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
6. [How the Model Works](#how-the-model-works)  
7. [Model Results & Performance](#model-results--performance)  
8. [Business Insights & Recommendations](#business-insights--recommendations)  
9. [Conclusion](#conclusion)  
10. [Next Steps](#next-steps)  
11. [How to Share This Report](#how-to-share-this-report)

---

## **Introduction**

Customer Lifetime Value (CLV) is a **key metric** for businesses, especially in the **motor industry**. It helps predict **the total revenue a customer will generate** over their lifetime. With this prediction, companies can:

- **Identify high-value customers** and focus on retaining them.  
- **Forecast revenue** and plan operations efficiently.  
- **Optimize sales channels** for better customer engagement.  

---

## **Objectives**

The main objectives of the CLV prediction model are:  

1. **Predict future spending** by customers to estimate their lifetime value.  
2. **Segment customers** based on loyalty and spending behavior.  
3. **Optimize marketing and service strategies** for higher revenue.  
4. **Compare purchase channels** to identify the most profitable ones.  

---

## **Key Insights**

1. **High-Value Customers are Critical for Revenue**  
   - Over **80%** of the customers in the dataset are classified as **high-value**.  
   - **Focus on loyalty programs** to retain these customers.

2. **Dealerships Outperform Other Channels**  
   - **Median CLV at dealerships** is higher compared to online and direct sales.  
   - **Insight**: Investing in dealership services will drive long-term revenue.

3. **Seasonality Impacts Customer Spend**  
   - **Spending is higher in Q1 and Q4**, suggesting that **seasonal promotions** during these periods could increase revenue.

---

## **Data Overview**

The following table summarizes the key features in the dataset:

| **Feature**               | **Description**                                  |
|---------------------------|--------------------------------------------------|
| **Customer ID**            | Unique identifier for each customer              |
| **Age**                    | Customer's age                                   |
| **Vehicle Type**           | Car, truck, motorcycle, or bus                   |
| **Usage Type**             | Personal or commercial use                       |
| **Average Order Value**    | Average transaction value                        |
| **Total Spend**            | Total amount spent by the customer               |
| **Transaction Frequency**  | Number of completed transactions                 |
| **Warranty Status**        | Active or expired warranty                       |

![image](https://github.com/user-attachments/assets/d9b85d8a-d5aa-42e8-9484-9ecab926ac87)

---

## **Exploratory Data Analysis (EDA)**

### **Distribution of Key Features**

![Distribution of Key Features](file-47iPPwQ9rDg6xARNK0Bn8It1)

- **Vehicle Types**:  
  - Cars and motorcycles are the most common.  
  - **Commercial vehicles** tend to generate higher CLV due to frequent servicing.

![image](https://github.com/user-attachments/assets/593c53df-0b8b-4037-b75a-721bb79a6594)

---

### **Loyalty and Total Spend**

![image](https://github.com/user-attachments/assets/a9f76a44-125d-4a8e-acc4-7626e1f4eeee)

- **Loyal Customers** spend ~300,000 units, compared to ~250,000 units for non-loyal ones.  
  **Insight**: Programs focused on increasing loyalty will significantly impact revenue.

---

### **Quarterly Trends in Spending**

![image](https://github.com/user-attachments/assets/ad9a5029-5d4b-46c0-bfe7-55ba19be526d)

- **Highest Spend**: Q1 (~255,000 units)  
- **Lowest Spend**: Q2 (~230,000 units)  
  **Insight**: Launching targeted campaigns in **Q1 and Q4** can boost yearly revenue.

---

## **How the Model Works**

1. **Data Preprocessing**:  
   - We **removed duplicates** and filled **missing values**.  
   - Numerical values like **Total Spend** and **Transaction Frequency** were **standardized**.

2. **Modeling Process**:  
   - **Random Forest** was chosen due to its ability to capture **complex patterns**.  
   - We used an **80/20 split** between training and testing data to ensure robust evaluation.

3. **Evaluation Metrics**:  
   - **MAE (Mean Absolute Error)**: Measures the average prediction error.  
   - **RMSE (Root Mean Squared Error)**: Penalizes large errors, ensuring accuracy.

---

## **Model Results & Performance**

### **Actual vs Predicted CLV**

![image](https://github.com/user-attachments/assets/8a9b5670-a8c9-4920-8d84-e3195c70783b)

- **Perfect Prediction Line**: The closer the points are to the line, the better the predictions.  
- **Small Prediction Errors**: Most points align with the line, indicating **high model accuracy**.

---

### **Correlation Heatmap with CLV**

![image](https://github.com/user-attachments/assets/5d5e7c69-d8e0-420e-947d-ae9a93fd7878)

- **Positive Correlation**: Average order value (0.38) strongly impacts predicted CLV.  
  **Insight**: Encouraging larger purchases will **boost lifetime value**.

---

### **CLV by Purchase Channel**

![image](https://github.com/user-attachments/assets/1833b767-2362-4ac7-b125-852dce89f074)

- **Dealerships**: Median CLV ~3 million units
-  **Direct sales**: Median CLV ~3 million units  
- **Online Sales**: Median CLV ~2.5 million units  
  **Insight**: Focus on **dealerships** and  **Direct sales** to maximize revenue per customer.

---

### **Sample Customer Predictions**

![image](https://github.com/user-attachments/assets/5b0cb56a-f0e7-4b97-a1a2-fe9478d16a1d)

- **Example Predictions**:  
  - **Customer 1501**:  
    - **Predicted CLV**: 4,321,418 units  
    - **Actual CLV**: 4,305,863 units  
    - **Error**: 15,555 units  
  - **Customer 705**:  
    - **Predicted CLV**: 690,662 units  
    - **Actual CLV**: 724,346 units  
    - **Error**: -33,683 units  

  **Interpretation**: Small prediction errors demonstrate that the model can **reliably forecast future revenue**.

---

## **Business Insights & Recommendations**

1. **Focus on High-Value Customers**  
   - Prioritize retaining the **4,000 high-value customers** identified by the model.

2. **Enhance Dealership and direct sales Services**  
   - Offer **personalized experiences** to drive higher CLV through dealerships.

3. **Increase Average Order Values**  
   - Introduce **bundled packages and premium services** to encourage larger transactions.

4. **Leverage Seasonal Trends**  
   - Launch **promotions during Q1 and Q4** to capitalize on high spending.

5. **Optimize Online Platforms**  
   - Offer **subscription services** to increase repeat purchases.

---

## **Conclusion**

The **CLV Prediction Model for the Motor Industry** provides reliable insights into customer behavior, enabling businesses to:

- **Retain high-value customers** and improve customer satisfaction.  
- **Optimize sales channels** for better profitability.  
- **Forecast future revenue** to plan resources effectively.

By implementing these recommendations, the business can **boost revenue** and achieve sustainable growth.

---

## **Next Steps**

1. **Deploy the Random Forest Model** for real-time CLV predictions.  
2. **Monitor Model Performance** and update it regularly with new data.  
3. **Implement Seasonal Promotions** to maximize revenue potential.

---

