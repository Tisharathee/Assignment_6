### Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model
# Overview

This project models a probability density function (PDF) using a roll-number-parameterized non-linear transformation applied to real-world air quality data.

The dataset used is the India Air Quality Dataset from Kaggle.
We use the NO₂ (Nitrogen Dioxide) feature as the variable 
𝑥
x.

The objective is to:

Apply a roll-number-based non-linear transformation.

Learn parameters of a Gaussian-shaped probability density function.

Estimate parameters using Maximum Likelihood Estimation (MLE).

## Dataset

Source:
India Air Quality Data
https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

Feature Used:
no2 (Nitrogen Dioxide concentration)

## Mathematical Model
Step 1: Non-Linear Transformation

Each value of 
𝑥
x is transformed into 
𝑧
z using:

𝑧 =𝑥+𝑎𝑟sin(𝑏𝑟𝑥)z=x+ar.sin(br.x)


r = University Roll Number

mod = remainder operator

This transformation introduces a personalized non-linear modification based on the roll number.


### Learn Probability Density Function

We model the transformed variable 
𝑧
z using:𝑝^(𝑧)=𝑐𝑒−𝜆(𝑧−𝜇)2p^(z)=ce−λ(z−μ)2

Where:

μ = mean

λ = shape parameter

c = normalization constant

	​

This ensures the learned function is a valid probability density function.


### Implementation Steps

Load dataset using Pandas.

Extract no2 feature.

Compute 
𝑎
𝑟
a
r
	​

 and 
𝑏
𝑟
b
r
	​

 from roll number.

Apply transformation.

Estimate 
𝜇
μ, 
𝜆
λ, and 
𝑐
c.

Visualize empirical histogram and learned PDF.

### Visualization

The histogram of transformed data is compared with the learned PDF curve.

This verifies how well the estimated Gaussian-shaped model fits the transformed data.
<img width="1390" height="868" alt="image" src="https://github.com/user-attachments/assets/d90e867b-2a67-4ead-af82-3856e3d3e7e1" />
## Technologies Used

Python

NumPy

Pandas

Matplotlib

Google Colab

## Final Output

The following parameters are submitted:

μ (mean)

λ (lambda)

c (normalization constant)
