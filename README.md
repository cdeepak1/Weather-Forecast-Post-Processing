# Weather Forecast Post-Processing

This repository contains the implementation of linear and non-linear post-processing techniques for improving weather forecast accuracy using the EUPPBench dataset. The project focuses on correcting errors in deterministic weather forecasts, particularly for 2-meter air temperature, using Principal Component Regression (PCR) and Boosted Trees.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methods](#methods)
   - [Principal Component Regression (PCR)](#principal-component-regression-pcr)
   - [Boosted Trees](#boosted-trees)
4. [Results](#results)


## Introduction
The goal of this project is to enhance the accuracy of weather predictions by applying statistical post-processing methods to the output of numerical weather prediction (NWP) models. The project applies linear and non-linear techniques to adjust raw model outputs, aiming to improve temperature forecast accuracy.

## Dataset
The dataset used is the EUPPBench dataset, which includes forecast data from the Integrated Forecasting System (IFS) of ECMWF and observational data from the German Weather Service (DWD). The data comprises both modeled forecasts and real-world observations, providing a robust foundation for post-processing analysis.

## Methods

### Principal Component Regression (PCR)
- **Description:** PCR is a linear method that transforms predictor variables into uncorrelated principal components, then performs regression on these components. It helps reduce dimensionality and manage multicollinearity in the predictors.
- **Use Cases:** Effective when predictors are highly correlated or numerous.
- **Limitations:** May fail if the principal components do not capture significant variance or if the underlying relationship is non-linear.

### Boosted Trees
- **Description:** Boosted Trees is a non-linear ensemble method using Classification and Regression Trees (CART). It iteratively corrects errors from previous models to improve overall performance.
- **Use Cases:** Suitable for complex datasets with non-linear relationships and mixed data types.
- **Limitations:** Computationally intensive and prone to overfitting without careful tuning.

## Results
- **PCR MSE:** 4.80
- **Boosted Trees MSE:** 5.20
- Despite expectations, the linear PCR method outperformed the non-linear Boosted Trees method in this specific context, highlighting the importance of method selection and dataset characteristics.

