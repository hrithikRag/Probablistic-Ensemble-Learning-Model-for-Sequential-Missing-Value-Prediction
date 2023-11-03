# Predicting Missing IoT Sensor Data with Probabilistic Ensemble Learning

This repository contains the implementation of a cutting-edge machine learning solution that secured the 2nd place in the IISc Kaggle competition. The competition was centered around the challenging problem of predicting missing data in time series sequences from Internet of Things (IoT) sensors, which is a critical task for maintaining the integrity and usefulness of IoT applications in various domains such as environmental sensing, smart homes, and industrial automation.

## Project Overview

The crux of the project was to develop a predictive model capable of accurately inferring missing data points within a sequence of IoT sensor readings. To address this issue, we designed a sophisticated probabilistic ensemble learning framework that integrates several predictive models, each chosen for their unique strengths in modeling different aspects of the time series data.

## Methodology

The ensemble model is composed of three core components:

1. **Ridge Regression**: This linear modeling approach is particularly adept at understanding the associations between different features in the dataset, which in this case correspond to readings from various sensors. Ridge Regression was selected for its ability to handle multicollinearity and for its regularization capabilities, which help in preventing overfitting.

2. **Gaussian Process Regression (GPR)**: GPR was employed to capture the underlying kernel matrix of the time series. This non-parametric method is known for its ability to provide a measure of the uncertainty associated with the predictions, which is paramount in probabilistic modeling.

3. **Bi-directional Long Short-Term Memory (Bi-LSTM)**: To capture the temporal dependencies and trends in the sensor data, a Bi-LSTM neural network was utilized. The bi-directional nature of this LSTM variant allows it to process data points from both past and future states, offering a comprehensive understanding of time-based patterns.

### Ensemble Strategy

The ensemble model combines the predictions of these three models, each contributing a weighted vote to the final prediction. The weights of these votes were not arbitrarily assigned; instead, they were meticulously optimized through a series of Monte-Carlo simulations. This probabilistic approach to ensemble learning not only provided a mechanism to blend the strengths of individual models but also allowed for the quantification of uncertainty in the predictions.

## Results

The Monte-Carlo simulations were pivotal in determining the optimal weight distribution for the ensemble model. By simulating various window sizes and analyzing the performance across a multitude of scenarios, we were able to identify the most effective combination of models for predicting the missing data points.

## Conclusion

The proposed probabilistic ensemble learning model demonstrates a robust and reliable method for addressing the challenge of missing data prediction in IoT sensor time series. The project highlights the synergy that can be achieved by combining different machine learning paradigms and the effectiveness of probabilistic methods in dealing with uncertainties inherent in real-world data.

---
