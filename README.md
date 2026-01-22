# EVCS DDoS Detection

A machine learning project for detecting DDoS (Distributed Denial of Service) attacks in Electric Vehicle Charging Station (EVCS) systems using performance statistics.

## Overview

This project analyzes performance monitoring data from CICEV2023 dataset to detect anomalous behavior indicative of DDoS attacks on electric vehicle charging infrastructure. The analysis includes multiple attack scenarios and utilizes various machine learning models for classification.

## Dataset

The project uses the **CICEV2023** dataset which contains:
- Multiple attack types:
  - `Correct_ID` - Normal operations with correct identifiers
  - `Wrong_CS_TS` - Attacks with wrong Charging Station timestamps
  - `Wrong_EV_TS` - Attacks with wrong Electric Vehicle timestamps
  - `Wrong_ID` - Attacks with wrong identifiers

- Scenario configurations:
  - CS (Charging Station) modes: Random_CS_On, Random_CS_Off
  - Gaussian distribution modes
  - Attack vs Normal traffic patterns

## Features

The system analyzes performance statistics including:
- CPU metrics (cycles, instructions, cache references)
- Memory operations
- Branch predictions
- Page faults
- Context switches
- Network-related performance counters

## Requirements

Install the required Python packages:

```bash
pip install xgboost imbalanced-learn scikit-learn pandas numpy matplotlib seaborn plotly
```

### Dependencies
- Python 3.7+
- pandas
- numpy
- scikit-learn
- xgboost
- imbalanced-learn
- matplotlib
- seaborn
- plotly

## Usage

1. **Setup Dataset**: Place the CICEV2023.zip file in the project directory or extract the CICEV2023 folder directly.

2. **Run the Notebook**: Open `evcs_ddos_detection_by_miqbalj_final.ipynb` in Jupyter Notebook or Google Colab and run the cells sequentially.

3. **Main Steps**:
   - Load and extract dataset
   - Import required libraries
   - Parse performance statistics files
   - Preprocess and balance data
   - Train machine learning models
   - Evaluate model performance
   - Visualize results

## Methodology

1. **Data Loading**: Parses `perf_stat` files from various attack scenarios
2. **Feature Engineering**: Extracts performance metrics and creates feature vectors
3. **Data Preprocessing**: Handles missing values, scales features, and balances classes
4. **Model Training**: Trains multiple ML models for binary classification (Attack vs Normal)
5. **Evaluation**: Assesses model performance using accuracy, precision, recall, F1-score
6. **Visualization**: Generates plots for performance analysis and feature importance

## Models

The project likely implements various machine learning algorithms including:
- XGBoost
- Random Forest
- Decision Trees
- Support Vector Machines (SVM)
- Logistic Regression
- Neural Networks

## Project Structure

```
*/
├── evcs_ddos_detection_by_miqbalj_final.ipynb  # Main notebook
├── final_model.pkl                              # Trained model file
├── CICEV2023/                                   # Dataset directory (not included)
│   ├── Correct_ID/
│   ├── Wrong_CS_TS/
│   ├── Wrong_EV_TS/
│   └── Wrong_ID/
└── README.md                                    
```

## Output

You can see the final model (output) on the `final_model.pkl`.

## Google Colab Support

The notebook includes automatic detection for Google Colab environment and provides:
- File upload functionality
- Automatic ZIP extraction
- Environment-specific path handling

## Author

[Katyusha47](https://github.com/Katyusha47)

## License

Please refer to the dataset license and terms of use for [CICEV2023](https://www.unb.ca/cic/datasets/cicev2023.html).

## Acknowledgments

This project uses the CICEV2023 dataset for analyzing cybersecurity threats in electric vehicle charging infrastructure.
