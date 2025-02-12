# Mental Health Cases Prediction with Deep Learning

This repository contains code for predicting mental health cases using various deep learning models such as LSTM, Bi-LSTM, GRU, Bi-GRU, and an ensemble model. The project uses time-series data to forecast mental health trends and evaluate multiple models' performance.

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
The results are based on key regression metrics, as shown in the table below. Mental health cases typically range between 1 and 100 per spatial location.

<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>RMSE</th>
      <th>MAE</th>
      <th>MSLE</th>
      <th>R-squared</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>lstm</td>
      <td>3.16</td>
      <td>2.38</td>
      <td>0.16</td>
      <td>0.63</td>
    </tr>
    <tr>
      <td>gru</td>
      <td>3.12</td>
      <td>2.39</td>
      <td>0.16</td>
      <td>0.64</td>
    </tr>
    <tr>
      <td>bi_lstm</td>
      <td>3.17</td>
      <td>2.40</td>
      <td>0.17</td>
      <td>0.63</td>
    </tr>
    <tr>
      <td>bi_gru</td>
      <td>3.17</td>
      <td>2.41</td>
      <td>0.17</td>
      <td>0.62</td>
    </tr>
    <tr>
      <td>ensemble</td>
      <td>3.09</td>
      <td>2.37</td>
      <td>0.16</td>
      <td>0.64</td>
    </tr>
  </tbody>
</table>

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

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

