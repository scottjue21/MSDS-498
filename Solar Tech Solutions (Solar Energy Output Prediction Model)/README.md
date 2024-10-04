# Solar Tech Solutions Project Overview

## Solar Energy Prediction Using Machine Learning

With the increasing demand for renewable energy, particularly solar energy, utility companies are seeking ways to optimize their energy grids. The Solar Tech Solutions project aims to develop predictive models to forecast solar power output using historical weather data to help electric utility companies forecast photovoltaic (PV) energy production with competitive accuracy. This project focuses on developing machine learning models to predict solar energy output, enabling utilities to make more informed decisions about grid utilization, reduce reliance on fossil fuels, and achieve cost savings. The dataset used for this project contains solar output and weather data from 12 Northern Hemisphere sites over a 14-month period.

## Objectives

The primary objective of this project was to improve the accuracy of solar energy output predictions using various machine learning techniques. The project aimed to deliver:

- **Improved Forecast Accuracy**: By leveraging machine learning algorithms, this project enhances the precision of solar energy output predictions.
- **Cost Savings**: Accurate predictions reduce the need for backup power sources, resulting in cost savings for utility companies.
- **Scalability**: The models can be trained on extensive historical and real-time data, allowing scalability across different solar systems and locations.
- **Competitive Advantage**: Adopting machine learning gives utility companies an edge in the energy market and supports innovation.
- **Environmental Benefits**: By optimizing solar energy use, utility companies can reduce their carbon footprint and contribute to a more sustainable future.

## Audience and Market

The predictive models developed by Solar Tech Solutions are relevant to:

- **Electric utility companies** in the Northern Hemisphere utilizing solar power as part of their energy mix.
- **Government agencies** and **municipalities** looking to integrate solar power into existing power grids.
- **Solar panel companies** interested in expanding operations through feasibility studies.
- **Utility customers** exploring the benefits of solar panel installation based on long-term cost savings.

## Methodology

### Process Management

We followed the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework, which includes the following phases:

1. **Business Understanding**: Defined business objectives, determined goals, and developed a project plan.
2. **Data Understanding**: Acquired and explored solar and weather data, ensuring data quality.
3. **Data Preparation**: Cleaned, formatted, and merged datasets to prepare for modeling.
4. **Modeling**: Applied various machine learning algorithms to build predictive models.
5. **Evaluation**: Assessed model performance using metrics like RMSE and R².
6. **Future Deployment Consideration**: Although not part of the project, deployment options were explored for future scalability.

### Dataset

This project utilized publicly available solar power output data from [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/northern-hemisphere-horizontal-photovoltaic), which contains weather and solar panel output data from 12 Northern Hemisphere sites over a 14-month period. Additional weather features were incorporated from [Solcast](https://toolkit.solcast.com.au/legacy-live-forecast) , a solar assessment and forecasting resource. Key independent variables include: 

- **Numerical features**: altitude, humidity, temperature, wind speed, visibility, pressure, cloud ceiling, and others.
- **Categorical feature**: season.
- **Text features**: date, time sampled, location.

## Modeling Approaches

Several predictive modeling approaches were developed and compared for their accuracy in predicting solar energy output:

- **Polynomial Regression**
- **Random Forests**
- **LightGBM**
- **Extra Trees**
- **Convolutional Neural Networks (CNN)**
- **Multilayer Perceptron (MLP)**
- **Bagging**
- **AutoML Tool**

These models were trained using historical solar power output data along with weather data to forecast future solar energy production. Each model’s performance was evaluated based on RMSE and R² values to identify the most effective approach.

## Results

After evaluating the models based on RMSE and R² values, **LightGBM** emerged as the best-performing model with an R² score of 0.6893 on the test data and an RMSE of 3.9599. It outperformed other models, such as Random Forest, Extra Trees, and Polynomial Regression.

- The **LightGBM** model demonstrated the highest predictive capability, while models like CNN and MLP performed poorly.
- A **feature importance analysis** indicated that variables like AmbientTemp, Humidity, and WindDirection10m were crucial in predicting solar output.

Additionally, performance varied based on season and location. For instance:

- **Extra Trees** performed best in the Summer and Winter seasons, while **LightGBM** was optimal for Spring and Fall.
- **Location-based models** showed that Extra Trees performed best in most locations, but LightGBM also did well in select locations.

## Recommendations

Based on the evaluations, we recommend using the LightGBM model as the primary forecasting model due to its high R² and low RMSE. For further improvement:

- **Location-based models** should be implemented, as performance varies significantly by geographic location.
- **Season-specific models** should be considered, as different models perform better in different seasons (e.g., LightGBM in Spring/Fall and Extra Trees in Summer/Winter).

## Conclusion

**Solar Tech Solutions** successfully developed models to predict solar power output based on weather data, with **LightGBM** showing the best performance among the models evaluated. The results demonstrated that weather features such as ambient temperature and humidity are highly predictive of solar output, and further analysis identified seasonal and location-specific model improvements. These findings provide utility companies with the tools to make data-driven decisions for optimizing solar energy production.

### Contributors

This project was a collaborative effort by the following team members:

- Andrew Gray
- Shahar Journo
- Johanna Sheu
- Scott Jue
