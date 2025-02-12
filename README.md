# Health Cases Prediction

This repository focuses on predicting health cases, including mental health and respiratory conditions, using deep learning models. 

<table>
  <tr>
    <th style="text-align: center; font-weight: bold;">Health Condition</th>
    <th style="text-align: center; font-weight: bold;">Actual Cases (2024-01-09)</th>
    <th style="text-align: center; font-weight: bold;">Predicted Cases (2024-01-09)</th>
  </tr>
  <tr>
    <td style="text-align: center; font-weight: bold;">Respiratory Cases</td>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/d33eb868-6a8f-4c9b-bfee-a0c9f23fa2c0" alt="Actual Cases on 2024-01-09" style="width: 100%;" />
    </td>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/2b2a475c-efc6-483f-9c95-c95b20f6b819" alt="Predicted Cases on 2024-01-09" style="width: 100%;" />
    </td>
  </tr>
  <tr>
    <td style="text-align: center; font-weight: bold;">Mental Health Cases</td>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/018ddcaf-d4d8-4d52-b2b9-065f3e53ea80" alt="Actual Cases on 2024-01-09" style="width: 100%;" />
    </td>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/44bd4263-fe39-49c5-ac38-55d7ac28ecd1" alt="Predicted Cases on 2024-01-09" style="width: 100%;" />
    </td>
  </tr>
</table>


## Overview

The goal of this project is to develop predictive models for health-related cases, helping healthcare professionals and policymakers make data-driven decisions. The models are trained on relevant datasets (ambulance attendances) and evaluated based on established performance metrics. While model outputs are insightful, accuracy, translation potential and impact would be substantially improved through integrating patient level primary and secondary health service use data to increase data size.

## Applications

- **Mental Health Prediction:** This system employs five deep learning models to forecast mental health-related case counts based on diverse air quality and climatic factors. At present, predictions are limited to overall case numbers rather than specific categories by primary impression codes. This is due to data gaps in both climate and health records, as well as the time series methodology used, which incorporates a five-day lag.
- **Respiratory Cases Prediction:** Again, this uses five deep learning models to predict the number of respiratory-related cases based on environmental and climatic features. Similar to the mental health model, it provides aggregated case counts rather than detailed classifications by primary impression codes, owing to missing data in the available datasets and the five-day lag inherent in the time series approach.

## Results

The project features visualisations of predictions over defined time periods, illustrating the models' effectiveness in forecasting health cases. Detailed results can be found in the respective ReadMe.md files within their corresponding folders in this repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

