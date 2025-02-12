# Health Cases Prediction

This repository focuses on predicting health cases, including mental health and respiratory conditions, using deep learning models. 

## Overview

The goal of this project is to develop predictive models for health-related cases, helping healthcare professionals and policymakers make data-driven decisions. The models are trained on relevant datasets (ambulance attendances) and evaluated based on established performance metrics. While model outputs are insightful, accuracy, translation potential and impact would be substantially improved through integrating patient level primary and secondary health service use data to increase data size.

## Applications

- **Mental Health Prediction:** This system employs five deep learning models to forecast mental health-related case counts based on diverse air quality and climatic factors. At present, predictions are limited to overall case numbers rather than specific categories by primary impression codes. This is due to data gaps in both climate and health records, as well as the time series methodology used, which incorporates a five-day lag.
- **Respiratory Cases Prediction:** Again, this uses five deep learning models to predict the number of respiratory-related cases based on environmental and climatic features. Similar to the mental health model, it provides aggregated case counts rather than detailed classifications by primary impression codes, owing to missing data in the available datasets and the five-day lag inherent in the time series approach.

## Results

The project features visualisations of predictions over defined time periods, illustrating the models' effectiveness in forecasting health cases. Detailed results can be found in the respective ReadMe.md files within their corresponding folders in this repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

