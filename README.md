# **SVM Classification Models for Salary Data and Forest Fire Size**  

This project demonstrates the application of Support Vector Machines (SVM) for two distinct classification problems:  

1. Predicting salary categories (`<=50K` or `>50K`) based on demographic and work-related features.  
2. Classifying forest fire size (`Small` or `Large`) based on meteorological and environmental factors.  

## **Table of Contents**  
1. [Overview](#overview)  
2. [Datasets](#datasets)  
3. [Modeling Approach](#modeling-approach)  
4. [Results](#results)  
5. [Prerequisites](#prerequisites)  
6. [Installation](#installation)  
7. [Usage](#usage)  
8. [Project Structure](#project-structure)  
9. [License](#license)  

## **Overview**  
This project focuses on using SVM, a powerful supervised learning algorithm, to solve two classification problems. GridSearchCV and RandomizedSearchCV are utilized to optimize hyperparameters for improved model performance.  

- **Salary Prediction Model**: Uses demographic and work-related features to classify individuals into salary categories.  
- **Forest Fire Size Classification Model**: Predicts the size of burned forest areas based on meteorological conditions.  

## **Datasets**  
### Salary Dataset  
- Features:  
  - **age**: Age of the individual.  
  - **workclass**: Type of work classification.  
  - **education**: Educational level of the individual.  
  - **maritalstatus**: Marital status of the individual.  
  - Other features: `occupation`, `relationship`, `race`, `sex`, `capitalgain`, `capitalloss`, `hoursperweek`, `native`.  
- Target: **Salary** (`<=50K` or `>50K`).  

### Forest Fire Dataset  
- Features:  
  - **FFMC**, **DMC**, **DC**, **ISI**: Fire weather indices.  
  - **temp**: Temperature in Celsius.  
  - **RH**: Relative humidity (%).  
  - Other features: `wind`, `rain`, `month`, `day`.  
- Target: **Size_Categorie** (`Small` or `Large`).  

## **Modeling Approach**  
1. **Data Preprocessing**:  
   - Standardization using `StandardScaler`.  
   - Train-test split using `train_test_split`.  

2. **SVM Classifier**:  
   - Kernel Options: Linear, Polynomial, Radial Basis Function (RBF).  
   - Hyperparameter Optimization:  
     - **GridSearchCV** for exhaustive search.  
     - **RandomizedSearchCV** for faster exploration.  

3. **Evaluation Metrics**:  
   - **Accuracy Score**.  
   - **Confusion Matrix**.  
   - **Classification Report**.  

## **Results**  
- **Salary Prediction Model**:  
  - Accuracy: **82.7%**.  
  - Confusion Matrix:  
    ```
    [[9726,   78],
     [2155,  947]]
    ```  

- **Forest Fire Size Classification Model**:  
  - Accuracy: **91.67%**.  
  - Confusion Matrix:  
    ```
    [[ 25,  11],
     [  2, 118]]
    ```  

## **Prerequisites**  
- Python 3.7 or above.  
- Libraries:  
  - `numpy`  
  - `pandas`  
  - `scikit-learn`  

## **Installation**  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/R-Mahesh45/svm-classification.git  
   cd svm-classification  
   ```  
2. Install the required libraries:  
   ```bash  
   pip install -r requirements.txt  
   ```  

## **Usage**  
1. Load the dataset.  
2. Run the Jupyter notebooks or Python scripts for Salary Prediction or Forest Fire Size Classification.  
3. Evaluate model performance using accuracy and confusion matrices.  

## **Project Structure**  
```plaintext  
├── data/  
│   ├── salary_data.csv  
│   ├── forest_fire_data.csv  
├── notebooks/  
│   ├── salary_classification.ipynb  
│   ├── forest_fire_classification.ipynb  
├── scripts/  
│   ├── salary_svm.py  
│   ├── forest_fire_svm.py  
├── requirements.txt  
└── README.md  
```  
 
