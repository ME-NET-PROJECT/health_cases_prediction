# Mental Health Cases Prediction with Deep Learning

This repository contains code for predicting mental health cases using various deep learning models such as LSTM, Bi-LSTM, GRU, Bi-GRU, and an ensemble model. The project leverages time-series data to forecast mental health trends and evaluate multiple models' performance.

<table>
  <tr>
    <td style="text-align: center; font-weight: bold;">
      <img src="(https://github.com/user-attachments/assets/825f22e8-f876-4331-b550-b5cba08e072a" alt="Actual Cases on 2024-01-09" style="width: 100%;" />
      Actual Cases (2024-01-09)
    </td>
    <td style="text-align: center; font-weight: bold;">
      <img src="https://github.com/user-attachments/assets/44bd4263-fe39-49c5-ac38-55d7ac28ecd1" alt="Predicted Cases on 2024-01-09" style="width: 100%;" />
      Predicted Cases (2024-01-09)
    </td>
  </tr>
</table>

## Overview

The models in this repository are designed to predict mental health cases using data collected from healthcare and environmental monitoring sources. The primary models implemented are:

- **LSTM (Long Short-Term Memory)**
- **Bi-LSTM (Bidirectional Long Short-Term Memory)**
- **GRU (Gated Recurrent Unit)**
- **Bi-GRU (Bidirectional Gated Recurrent Unit)**
- **Ensemble Model** (combination of the above models)

The evaluation includes multiple performance metrics, including RMSE, MAE, MSLE, and R-squared. The results are saved as CSV files for further analysis.

## Requirements

To run the code, you need to install the following dependencies:

- `TensorFlow`
- `NumPy`
- `Pandas`
- `Matplotlib`
- `Scikit-learn`

You can install them by running:

```bash
pip install -r requirements.txt
```

## Functionality

### 1. Model Evaluation: `evaluate_all_models()`
This function evaluates several pre-trained models (LSTM, Bi-LSTM, GRU, Bi-GRU) on test data (`X_test`, `y_test`) and stores performance metrics and predictions. The metrics include:

- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**
- **MSLE (Mean Squared Logarithmic Error)**
- **R-squared (Coefficient of Determination)**

It also saves the prediction results in CSV files and generates plots comparing predicted vs true values.

### 2. Training the Ensemble Model: `train_ensemble_model()`
This function trains an ensemble model by combining the predictions of the individual models (LSTM, Bi-LSTM, GRU, Bi-GRU). It utilizes a custom training loop with callbacks for early stopping and learning rate adjustments.

### 3. Ensemble Model Evaluation: `evaluate_ensemble()`
After training the ensemble model, this function evaluates its performance using the same metrics as the individual models. It saves the predictions and evaluation metrics to CSV files.

## Usage

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-repo/mental-health-prediction.git
cd mental-health-prediction
```

### Step 2: Install Dependencies

Make sure to install the required Python libraries:

```bash
pip install -r requirements.txt
```

### Step 3: Training and Evaluation

Run the model training and evaluation script. For example:

```python
output_dir = Path(dataset_folder) / Path(model_dataset) / Path('results')
evaluate_all_models(models_folder, X_test, y_test, X_test_meta, output_dir)
```

### Step 4: Ensemble Model Training and Evaluation

To train and evaluate the ensemble model, use:

```python
model_fns = [lstm_model, bi_lstm_model, gru_model, bi_gru_model]
history = train_ensemble_model(X_train, y_train, X_test, y_test, sequence_length, models_folder, model_fns, epochs=500)
evaluate_ensemble(models_folder, X_test, y_test, X_test_meta, output_dir, model_name="ensemble")
```

## Results

The results are based on regression metrics. Below is a visualization of a 7-day prediction from 05/01/2024 to 11/01/2024.

![7 days_Prediction](https://github.com/user-attachments/assets/7be44e03-8fee-401c-a301-c54cd78dbbe4)

The results of the evaluations are saved in the following structure:

```
results/
    ├── lstm/
    │   ├── lstm_metrics.csv
    │   ├── lstm_predictions.csv
    │   ├── visualise/
    ├── bi_lstm/
    │   ├── bi_lstm_metrics.csv
    │   ├── bi_lstm_predictions.csv
    │   ├── visualise/
    ├── ensemble/
    │   ├── ensemble_metrics.csv
    │   ├── ensemble_predictions.csv
    │   ├── visualise/
    └── ...
```

### Metrics File: `model_name_metrics.csv`
Contains the evaluation metrics for each model (RMSE, MAE, MSLE, R-squared).

### Predictions File: `model_name_predictions.csv`
Contains the predicted mental health case values alongside true values for comparison.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

