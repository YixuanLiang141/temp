# OPC Completion Prediction AI

This repository contains several Python scripts and dependencies that are instrumental to the operation of the OPC completion prediction model.

## Usage

1. Clone the entire directory to anywhere.

2. Create a file ".env" in the root directory which includes the SQL credentials:

    ```
    MYSQL_HOST=XXXXXX.com
    MYSQL_USER=XXXXXX
    MYSQL_PASSWORD=XXXXXX
    MYSQL_DB=XXXXXX
    ```

3. To make predictions everyday at 3 AM UTC, keep the following command running:

    ```bash
    python everyday.py
    ```

    To predict once at any time, run the following command:

    ```bash
    python auto.py
    ```

    In both cases, the prediction results will be saved to "predictions" directory.

    To verify past predictions with existing results, change the date in verify.py and run the following command:

    ```bash
    python verify.py
    ```

## Requirements

* pandas
* numpy
* joblib
* xgboost
* scikit-learn
* SQLAlchemy
* python-dotenv
* python-dateutil
* PyMySQL
