# Anomaly Detection Using Isolation Forest, One-class SVM, and Local Outlier Factor

## Introduction

Anomaly detection, also known as outlier detection, is a critical data analysis technique aimed at identifying patterns or observations that significantly deviate from the expected norm within a dataset. These deviations, known as anomalies or outliers, can indicate rare events or unusual data points that differ from the majority of the data. Anomalies can signal issues like technical faults or fraud, or highlight innovative and important phenomena.

In statistical terms, an anomaly is a data point that does not conform to the expected distribution or pattern of the dataset. Detecting these irregularities is essential, though challenging, as anomalies are often rare and may occur sporadically.

## Repository Structure

- `README.md` (this file)
- `src/`
  - `isolation_forest.ipynb` - Implementation of Isolation Forest for anomaly detection
  - `one_class_svm.ipynb` - Implementation of One-class SVM for anomaly detection
  - `local_outlier_factor.ipynb` - Implementation of Local Outlier Factor for anomaly detection
- `data/`
  - `heart.csv` - Sample data used for Isolation Forest
  - `Placement_data.csv` - Sample data used for One-class SVM
  - `insurance.csv` - Sample data used for Local Outlier Factor
- `requirements.txt` - List of Python dependencies

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/anomaly-detection.git
    ```

2. **Navigate to the project directory**:
    ```bash
    cd anomaly-detection
    ```

3. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Isolation Forest

1. **File**: `src/isolation_forest.py`

    ```python
    from src.isolation_forest import IsolationForestDetector

    detector = IsolationForestDetector()
    detector.fit('data/heart.csv')
    anomalies = detector.detect()
    ```

### One-class SVM

1. **File**: `src/one_class_svm.py`

    ```python
    from src.one_class_svm import OneClassSVMDetector

    detector = OneClassSVMDetector()
    detector.fit('data/Placement_data.csv')
    anomalies = detector.detect()
    ```

### Local Outlier Factor

1. **File**: `src/local_outlier_factor.py`

    ```python
    from src.local_outlier_factor import LocalOutlierFactorDetector

    detector = LocalOutlierFactorDetector()
    detector.fit('data/insurance.csv')
    anomalies = detector.detect()
    ```

## Data

The `data/` directory contains sample datasets used for testing the algorithms:
- `heart.csv` for Isolation Forest
- `Placement_data.csv` for One-class SVM
- `insurance.csv` for Local Outlier Factor

Replace these with your own datasets for real-world applications.

## Contributing

Contributions are welcome! Feel free to fork the repository, make improvements, and submit pull requests. For suggestions or issues, please open a discussion or issue in the repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
