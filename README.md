# Health Cases Prediction
The goal of this project is to develop predictive models for health-related cases (mental health and respiratory) using deep learning models. The models are trained on relevant datasets (ambulance attendances) and evaluated based on established performance metrics. While model outputs are insightful, accuracy, translation potential and impact would be substantially improved through integrating patient level primary and secondary health service use data to increase data size.

## The Dataset
Mental health and respiratory data includes all records of ambulance attendance for the study area (insert here) based on the ‘primary impression’ of trained paramedic clinicians attending patients. Primary impressions include the professional judgement of a trained paramedic clinician as well as the health history reported by the patient or other individuals who are known to the patient and are present at the time of ambulance attendance, such as carers and family members. Thus, the preliminary impression of the paramedic clinician reflects the presenting symptoms of the patient at the time of the emergency as well as medical history. Therefore, ambulance records capture severe health symptoms as well as underlying conditions culminating in medical emergencies. 

Mental health primary impressions include: 
- `Acute Behavioural Disturbance (Mental Health)`
- `Anxiety (Mental Health)`
- `Intentional Drug Overdose (Mental Health)`
- `Dementia (Mental Health)`
- `Depression (Mental Health)`
- `Attempted Suicide (Mental Health)`
- `Suicidal Ideations / Thoughts (Mental Health)`
- `Intentional Substance Overdose (Mental Health)`
- `Under MHA Section 2 (Mental Health)`
- `Self Harm (Mental Health)`
- `S136 (Mental Health)`
- `Psychosis (Mental Health)`
- `S135 (Mental Health)`
- `Under MHA Section 3 (Mental Health)`
- `Substance Induced Presentation (Mental Health)`
- `Under MHA Section 4 (Mental Health)`
- `Unknown Mental Health Disorder (Mental Health)`

Respiratory health primary impressions include: 
- Chest Infection (Respiratory)
- Other Respiratory Problem (Respiratory)
- Suspected PE (Respiratory)
- COPD (Respiratory)
- Asthma (Respiratory)
- Infectious Disease (Respiratory)
- Covid-19 (Respiratory)
- PE (Respiratory)
- Exacerbation COPD (Respiratory)
- Other Acute Respiratory Problem (Respiratory)
- Pneumonia (Respiratory)
- Upper Respiratory Tract Infection (Respiratory)
- Other Chronic Respiratory Problem (Respiratory)
- Asthma - Mild / Moderate (Respiratory)
- Asthma - Severe (Respiratory)
- Lower Respiratory Tract Infection (Respiratory)
- Bronchiolitis (Respiratory)
- Infective Exacerbation COPD (Respiratory)
- Pleurisy (Respiratory)
- Aspiration (Respiratory)
- Croup (Respiratory)
- Pneumonia - Unspecified (Respiratory)
- Asthma - Life Threatening (Respiratory)
- Flu (Respiratory)
- Pneumothorax (Respiratory)
- Spontaneous Pneumothorax (Respiratory)
- Respiratory Disorder - Unspecified (Respiratory)
- Respiratory Distress - Acute (Respiratory)
- Acute Bronchitis - Unspecified (Respiratory)
- Influenza - Unspecified (Respiratory)
- Common Cold (Respiratory)
- Epistaxis (Respiratory)
- Choking (Respiratory)
- Respiratory Arrest (Respiratory)

This dataset was obtained from the East Midlands Ambulance Service NHS Trust (EMAS). The research was approved by the University of Lincoln ethics board (2024_16191). 

## Applications

- **Mental Health Prediction:** This system employs five deep learning models to forecast mental health-related case counts based on diverse air quality and climatic factors. At present, predictions are limited to overall case numbers rather than specific categories by primary impression codes. This is due to data gaps in both climate and health records, as well as the time series methodology used, which incorporates a five-day lag.
- **Respiratory Cases Prediction:** Again, this uses five deep learning models to predict the number of respiratory-related cases based on environmental and climatic features. Similar to the mental health model, it provides aggregated case counts rather than detailed classifications by primary impression codes, owing to missing data in the available datasets and the five-day lag inherent in the time series approach.

## Results

The project features visualisations of predictions over defined time periods, illustrating the models' effectiveness in forecasting health cases. Detailed results can be found in the respective ReadMe.md files within their corresponding folders in this repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

