# 21PD28-Sigma-Hackathon

This project involves the analysis of US stock data for the year 2023 using QuantRocket. The main focus is on calculating daily returns, classifying days into bull, flat, and bear markets based on returns, and maximizing the portfolio value and make decisions on certain days using the  pre-specified logic.

## Table of Contents

- [Introduction](#introduction)
- [Data Preparation](#data-preparation)
- [Analysis](#analysis)
  - [Returns Calculation](#returns-calculation)
  - [State Classification](#state-classification)
  - [Portfolio Value Calculation](#portfolio-value-calculation)
-[Plots](#plots)

## Introduction

This project leverages QuantRocket to obtain and analyze daily close prices of US stocks throughout the year 2023.

## Data Preparation

To access the data you will have to generate a license key.
https://www.quantrocket.com/account/

## Analysis

### Returns Calculation

Let r(d) be the % returns and p(d) be the close price on day d. Then, 
r(d) = ((p(d) - p(d-1)))/p(d-1). 

### State Classification

if r(d) >= 0.1, s(d) = +1
else if r(d) > -0.1, s(d) = 0
else, s(d) = -1

### Portfolio Value Calculation

Assuming we decide to place a buy order trade for the day d+1,
if s(d+1) = 1 & s(d) = 0, then V(d+1) = V(d) + 1
else if s(d+1) = -1 & s(d) = 0, then V(d+1) = V(d) -1
and V(d+1) = V(d) in all other cases 

## Plots

![image](https://github.com/rk032/21PD28-Sigma-Hackathon/assets/105430589/16a9f134-9200-4681-aaa8-b86258170188)

We can interpret that if the line is generally ascending, it suggests an uptrend, while a descending line indicates a downtrend. A flat line may indicate a sideways or consolidating market.

![image](https://github.com/rk032/21PD28-Sigma-Hackathon/assets/105430589/0ebb03aa-1862-47dc-8c6d-f8bb32c60444)

Sudden spikes or dips suggest rapid changes in the stock's value. We can check for any recurring patterns

![image](https://github.com/rk032/21PD28-Sigma-Hackathon/assets/105430589/dce77bea-dd53-45b5-926a-9afcd358de92)

![image](https://github.com/rk032/21PD28-Sigma-Hackathon/assets/105430589/1480b244-76ee-457b-b254-29c810da1784)







