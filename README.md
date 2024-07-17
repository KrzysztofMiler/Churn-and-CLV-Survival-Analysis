# Churn-Prediction-and-CLV-using-Survival-Analysis

![image](https://github.com/user-attachments/assets/a30055d3-7931-4829-8e5b-a97ff8548e21)

## Overview
Welcome to the Churn Prediction and Customer Lifetime Value (CLV) project! This project leverages survival analysis to predict customer churn and calculate the lifetime value of each client. Additionally, it includes a "what-if" analysis feature to explore various scenarios and their potential impact on customer retention and value.

## Purpose
The goal is to develop an advanced model that can predict customer churn, calculate the lifetime value of customers, and provide actionable insights through scenario analysis. This demonstrates the practical application of survival analysis in business analytics.

## What is survival analysis?
Survival analysis is a statistical method used to analyze and predict the time until an event occurs. It was originally developed in the field of medical research to study patient lifetimes, especially in oncology. However, it can also be applied in non-medical fields where the main interest is the probability of an event happening over time, such as in cases of equipment failure.

![image](https://github.com/user-attachments/assets/ce1363ab-325f-4cf8-a74b-10ce2aae9bba)
Pictured above is a Kaplan-Meier curve applied to this dataset, separated between individuals with and without an international plan. On the Y-axis, the survival probability at each time point is denoted. This visualization shows that for the first ~50 days, the survival probability is high (around 97%), meaning there's a 97% chance that a customer hasn't churned, regardless of their chosen plan. However, after that point, a clear divergence occurs. Clients with an international plan have lower odds of not churning with each time step.

By day 200, a customer without an international plan has around a 55% chance of still staying with us, while this chance drops to below 10% for customers with an international plan.

**Here's an interesting question, however:** From a company's perspective, could it be more productive to push certain customers into such a plan, even if it leads to earlier cancellations, to receive more immediate funds than they would otherwise earn by keeping these customers longer?

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

**Why its used**: Traditional churn prediction methods often overlook the temporal aspect. Survival analysis captures this, providing more accurate and actionable insights, which can translate into more precise CLV modeling. It should be noted, however, that more advanced methods than Kaplan-Meier are necessary when making predictions for a particular individual, as done in this case.

### Customer Lifetime Value (CLV)
**Purpose**: CLV is calculated using the survival model's output, estimating the total revenue a business can expect from a customer over their entire relationship.

**Why its used**: Understanding CLV helps businesses allocate resources effectively, tailor marketing efforts, and improve customer retention strategies.

![image](https://github.com/user-attachments/assets/78387d90-a662-4914-ba3a-4bb98cc37b18)
The image above shows an example of a customer's lifetime value, with a red dashed line denoting the time point at which their survival probability (chance that they will churn) crosses 50%. This is the base case for such a customer, assuming they do not change their plan. The chart also displays the total value we can expect from a customer before they reach the 50% mark and the additional value when they go beyond that point.

### What-If Analysis
**Purpose**: This feature allows businesses to simulate different scenarios, such as changes in marketing strategies or customer service improvements, and see their potential impact on churn and CLV.

**Why its used**: What-if analysis provides a powerful tool for strategic planning, enabling businesses to make data-driven decisions. However, it is important to note that in many cases, such simulations might produce results that are incongruent with reality since they do not consider the underlying mechanisms that drive customers to choose certain options.

![image](https://github.com/user-attachments/assets/323eebae-9b46-4f0c-87df-cd42984d4e99)
Here are the results for the customer discussed previously. Currently, their chosen package includes only international calls (chart on the bottom left), which would earn the company just $101 before reaching the critical 50% mark. However, if the client were to decline their international calls package (bottom right chart), the company's earnings would rise to $119 (approximately a 17% increase). Additionally, if the client decided to add a voicemail plan, the value would increase to $191 (approximately an 89% increase).

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
