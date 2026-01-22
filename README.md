README – ML for Quantum Experiment Simulation

1. Project overview
        This project applies machine learning to a simulated single-qubit quantum experiment to predict properties derived from expectation values and pulse data. It covers data loading, exploratory data analysis, feature engineering, model training (Logistic Regression, Random Forest, MLP), and comparison of model performance.

2. Folder structure
        Please keep the folder organized as follows:

        - code/
            -ml-for-quantum-experiment-simulation-pratik-flossy
        - data/
            - expectations.csv
            - pulses.csv
        - readme.txt
        - requirements.txt

        The notebooks expect the CSV files to be in the data/ folder, with the paths:
            - Data/expectations.csv
            - Data/pulses.csv

3. Environment setup
        Python version:
            - Python 3.9 or later is recommended.

        Required packages:
            - numpy
            - pandas
            - matplotlib
            - seaborn
            - scikit-learn

        You can install all dependencies with:
            pip install -r requirements.txt

        Supported environments:
            - Jupyter Notebook / JupyterLab
            - VS Code with the Python extension
            - Google Colab

4. How to run the project

        Step 1 – Download and open the project
        1. Download the project folder from OneDrive.

        Step 2 – Check data files
        1. Make sure the following files exist:
            - Data/expectations.csv
            - Data/pulses.csv

        Step 3 – Run the notebook
        1. In Jupyter, choose “Run All” (or run each cell sequentially from top to bottom).
        2. The notebook will:
            - Import all required libraries.
            - Load and inspect expectations.csv and pulses.csv.
            - Perform exploratory data analysis (summary statistics, distributions, and example plots).
            - Engineer features from the preparation coordinates (e.g., magnitudes, means, variances).
            - Construct a 3-class target variable from the continuous Z_prep1 value.
            - Split the dataset into train and test sets and apply feature scaling.
            - Train three models: Logistic Regression, Random Forest, and MLPClassifier.
            - Evaluate each model using accuracy and classification reports.
            - Display a bar chart comparing the accuracy of all models.

        If the environment is correctly set up and the data files are present, the notebook should execute from start to finish without errors.

5. Notes and limitations
        - The current work is focused on a single-qubit simulation; extending to multi-qubit systems would require additional modelling.
        - The three-class target labels are based on binning a continuous measurement, which is a design choice and may affect class balance and interpretability.

Data source

        The data used in this project is derived from the QDataSet, a collection of simulated
        single- and two-qubit experiments designed for machine learning tasks. It provides
        expectation values (Bloch sphere coordinates) and control pulse information for
        10,000 single-qubit examples.

QDataSet:
        - E. Perrier et al., "QDataSet, quantum datasets for machine learning"
        - GitHub repository: https://github.com/eperrier/QDataSet
        - Article: https://www.nature.com/articles/s41597-022-01639-1

In this project I work with a preprocessed subset of the single-qubit data
(expectations and pulse features) saved as `expectations.csv` and `pulses.csv`.
The original simulation setup and generation details are described in the paper.

