## Solar Tech Solutions Project Overview

### Solar Energy Prediction Using Machine Learning

With the increasing demand for renewable energy, particularly solar energy, utility companies are seeking ways to optimize their energy grids. Solar Tech Solutions offers a predictive tool that uses weather data to help electric utility companies forecast photovoltaic (PV) energy production with competitive accuracy. This project focuses on developing machine learning models to predict solar energy output, enabling utilities to make more informed decisions about grid utilization, reduce reliance on fossil fuels, and achieve cost savings.

### Mission and Goals

The primary objective of this project was to improve the accuracy of solar energy output predictions using various machine learning techniques. The project aimed to deliver:

- **Improved Forecast Accuracy**: By leveraging machine learning algorithms, this project enhances the precision of solar energy output predictions.
- **Cost Savings**: Accurate predictions reduce the need for backup power sources, resulting in cost savings for utility companies.
- **Scalability**: The models can be trained on extensive historical and real-time data, allowing scalability across different solar systems and locations.
- **Competitive Advantage**: Adopting machine learning gives utility companies an edge in the energy market and supports innovation.
- **Environmental Benefits**: By optimizing solar energy use, utility companies can reduce their carbon footprint and contribute to a more sustainable future.

### Dataset

This project utilized publicly available solar power output data from [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/northern-hemisphere-horizontal-photovoltaic), which contains weather and solar panel output data from 12 Northern Hemisphere sites over a 14-month period. Additional weather features were incorporated from [Solcast](https://toolkit.solcast.com.au/legacy-live-forecast) , a solar assessment and forecasting resource. Key independent variables include altitude, humidity, temperature, wind speed, pressure, and cloud ceiling, among others.

### Modeling Techniques

Several predictive modeling approaches were developed and compared for their accuracy in predicting solar energy output:

- Polynomial Regression
- Random Forests
- LightGBM
- Extra Trees
- Convolutional Neural Networks (CNNs)
- Multilayer Perceptron (MLP)
- Bagging
- AutoML Tool

These models were trained using historical solar power output data along with weather data to forecast future solar energy production. Each model’s performance was evaluated based on RMSE and R² values to identify the most effective approach.

### Results

The models were evaluated using RMSE and R² metrics, and the LightGBM model emerged as the best-performing model. It achieved an R² score of **0.6893** on the test data, surpassing other models such as Random Forest, Extra Trees, and Bagging. While some models, like Random Forest, demonstrated high R² values on training data, they underperformed on the test data. LightGBM outperformed all models in terms of predictive accuracy on the test data with an RMSE of **3.9599**, making it the most reliable model for predicting solar output based on weather data.

A key insight from the analysis is the seasonal variability in model performance. LightGBM performed best in Spring and Fall, while Extra Trees excelled in Summer and Winter. Location-specific analysis revealed that different models perform better depending on the geographic area, with Extra Trees consistently showing superior performance across most locations. However, LightGBM performed well in specific areas like Camp Murray and March AFB.

Additionally, a classification model was implemented using AutoML, and the XGBoost Classifier demonstrated strong performance with a **Weighted AUC of 0.81**. The Pressure variable emerged as the most important feature in this classification task, highlighting the significance of weather data in predicting solar output.

### Recommendations

Based on the evaluations, we recommend using the LightGBM model as the primary forecasting model due to its high R² and low RMSE. For further improvement:

- **Location-based models** should be implemented, as performance varies significantly by geographic location.
- **Season-specific models** should be considered, as different models perform better in different seasons (e.g., LightGBM in Spring/Fall and Extra Trees in Summer/Winter).

### Implementation

For deployment, the LightGBM model was saved using Python’s Pickle package and deployed through a REST API hosted on AWS Lambda. The model container includes the code, source data, and configuration files, enabling real-time solar output predictions via API. A potential future enhancement would be the addition of a batch processing API for 10-day weather forecasts to enable longer-term planning by utility companies.

The REST API setup allows for real-time energy mix decisions, providing utility companies with actionable insights for grid optimization. A potential extension of this project could include developing a web application or dashboard that visualizes energy predictions across different locations, allowing utilities to optimize their grid management more effectively.

### Conclusion

The Solar Tech Solutions project successfully developed a machine learning-based solar output prediction model, outperforming previous research and delivering competitive accuracy. The LightGBM model emerged as the best performer, with location and season-specific modeling revealing important insights for optimizing solar energy predictions. The deployment of the model through a REST API enables utility companies to integrate real-time solar output forecasts into their energy management systems, paving the way for further innovation in renewable energy optimization.
