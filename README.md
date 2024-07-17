# Churn-Prediction-and-CLV-using-Survival-Analysis

![image](https://github.com/user-attachments/assets/a30055d3-7931-4829-8e5b-a97ff8548e21)

## Overview
Welcome to the Churn Prediction and Customer Lifetime Value (CLV) project! This project leverages survival analysis to predict customer churn and calculate the lifetime value of each client. Additionally, it includes a "what-if" analysis feature to explore various scenarios and their potential impact on customer retention and value.

## Purpose
The goal is to develop an advanced model that can predict customer churn, calculate the lifetime value of customers, and provide actionable insights through scenario analysis. This demonstrates the practical application of survival analysis in business analytics.

## Main Difference Between This Approach and Other Common Ones
The key difference in using survival analysis over plain regression or classification models lies in the type of answer we are seeking. A regression-based model can predict when a client will churn with a certain probability, and a classification model can accurately determine if a client will churn at a particular moment in time (e.g., 30 days). Survival analysis allows us to visualize the probability of a customer staying with us at each point in time. This leads to more precise evaluations of why churn may be happening (e.g., a customer canceling a subscription after the free period is over) and enables a more accurate calculation of customer lifetime value (CLV).

## Project Structure
### Data Used
The data used is the Orange Telecommunications dataset downloaded from Kaggle. The main variables of interest in CLV calculations are the voice plan and international plan. This dataset also contains usage data for each particular client and their basic demographic information.

## Project Execution Schema
After preprocessing the data, survival analysis is applied to model the time until a customer churns. The model is then used to calculate the Customer Lifetime Value (CLV) for each client. The project also incorporates a "what-if" analysis to simulate different business scenarios and their impact on churn and CLV.

## Methodologies
### Survival Analysis
**Purpose**: Survival analysis is used to predict the time until an event occurs, in this case, customer churn. It models the probability of a customer remaining active over time.

**Why its used**: Traditional churn prediction methods often overlook the temporal aspect. Survival analysis captures this, providing more accurate and actionable insights.

### Customer Lifetime Value (CLV)
**Purpose**: CLV is calculated using the survival model's output, estimating the total revenue a business can expect from a customer over their entire relationship.

**Why its used**: Understanding CLV helps businesses allocate resources effectively, tailor marketing efforts, and improve customer retention strategies.

### What-If Analysis
**Purpose**: This feature allows businesses to simulate different scenarios, such as changes in marketing strategies or customer service improvements, and see their potential impact on churn and CLV.

**Why its used**: What-if analysis provides a powerful tool for strategic planning, enabling businesses to make data-driven decisions.

![image](https://github.com/user-attachments/assets/323eebae-9b46-4f0c-87df-cd42984d4e99)

## Benefits of This Solution
-**Temporal Modeling**: Accurately captures the time-dependent nature of customer churn.
-**Strategic Insights**: Provides actionable insights into customer retention and value.
-**Scenario Simulation**: Enables businesses to explore the impact of various strategies before implementation.
-**Resource Optimization**: Helps in allocating marketing and retention resources more effectively.

## Performance Characteristics
-**Accuracy**: High accuracy in predicting churn and estimating CLV.
-**Business Impact**: Demonstrates significant potential for improving customer retention and revenue.
-**Scalability**: Can be adapted to different business contexts and data types.

## Key Features
**Survival Analysis for Churn Prediction**: Models the probability of customer churn over time.
**Customer Lifetime Value Calculation**: Estimates the total revenue from each customer.
**What-If Analysis**: Simulates the impact of different strategies on churn and CLV.


## Possible Future Directions
- **Integration with Real-Time Data**: Implementing real-time data feeds for dynamic churn prediction and CLV calculation.
- **Advanced Modeling Techniques**: Exploring more sophisticated survival models and machine learning algorithms.
- **Dashboard**: Developing a Power BI-based interactive dashboard enabling easier customer analysis.

## Contact
For inquiries, please contact krzy.miler@gmail.com.
