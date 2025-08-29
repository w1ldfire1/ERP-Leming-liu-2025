# ERP-Leming-liu-2025
Structural Complexity and Regional Heterogeneity in the UK Housing Market: Evidence from Persistent Homology

This repository contains the supporting materials for my MSc Data Science Extended Research Project (ERP) at the University of Manchester.  
The project accompanies the submitted dissertation titled:  
**Structural Complexity and Regional Heterogeneity in the UK Housing Market: Evidence from Persistent Homology**

---

## Project Overview
- **Author**: Leming Liu
- **Student-ID**:11517005
- **Pathway**: SAN
- **Year**: 2024-2025
- **Supervisor**: Simon Rudkin

### Abstract 
 
In recent years, the UK housing market has demonstrated notable nonlinear dynamics and structural changes, driven by a series of shocks including Brexit, the public health crisis, and a cycle of high inflation and interest rate hikes. Traditional econometric models, constrained by assumptions of linearity and stability, struggle to identify discontinuous changes in market conditions. The paper introduces a topological data analysis (TDA) framework, which is employed to construct a temporal trajectory of housing market structural complexity through multivariate and univariate embedding and sliding window persistent homology calculations. This study utilizes monthly data from London and Northwest England from 2009 to 2024 to investigate the disparities in uncertainty levels and shock response patterns between the two markets. London exhibits a phased-variable-dominated pattern, while the Northwest exhibits an overall synchronized response to national shocks. The findings indicate that the TDA persistent L₁ norm can function as an effective forward-looking indicator for identifying structural changes in the housing market and provide a quantitative basis for designing differentiated regional policies.

---

## Repository Structure
README.md
requirements.txt
London_Housing_Policy_Dataset.csv
London_Housing_Policy_Dataset_sd.csv
North_West_Housing_Policy_Dataset.csv
North_West_Housing_Policy_Dataset_sd.csv
preprocessing.ipynb
EDA.ipynb
Univariate and bivariate embedding-LD.ipynb
Univariate and bivariate embedding-NW.ipynb
Full multivariate embedding PH-LD.ipynb
Full multivariate embedding PH-NW.ipynb
norm-LD.csv
norm-NW.csv
Sensitivity.ipynb

## Datasets
* `London_Housing_Policy_Dataset.csv`: [Original dataset of London]
* `North_West_Housing_Policy_Dataset.csv`: [Original dataset of Northwest]
* `London_Housing_Policy_Dataset_sd.csv`: [Standardized dataset of London]
* `North_West_Housing_Policy_Dataset_sd.csv`: [Standardized dataset of Northwest]
* `norm-LD.csv/norm-NW.csv`: [Persistent Norm of joint embedding point cloud of all policy variables and lagged housing prices]

## Code Description
All code is provided in Jupyter Notebooks (`.ipynb`). It is recommended to run the notebooks in the following order to replicate the research workflow:
1.  **`preprocessing.ipynb`**:
    * **Purpose**: Data Preprocessing.
    * **Input**: `London_Housing_Policy_Dataset.csv`, `North_West_Housing_Policy_Dataset.csv`
    * **Output**: 'London_Housing_Policy_Dataset_sd.csv','London_Housing_Policy_Dataset_sd.csv'
      
2.  **`EDA.ipynb`**:
    * **Purpose**: Exploratory data analysis.


3.  **`Univariate and bivariate embedding-London.ipynb` / `Univariate and bivariate embedding-NW.ipynb`**:
    * **Purpose**: Univariate and bivariate embedding  point clouds Persistent Homology Analysis, Calculating Rolling Correlation
    * **Description**: 4.1 Housing price univariate lagged persistent homology; 4.3 Correlation Changes in Different Norm Periods(Calculating Rolling Correlation); 4.4 Regional Heterogeneity Analysis(joint embedding of single policy variables and housing prices)

4.  **`Full multivariate embedding PH-LD.ipynb` / `JFull multivariate embedding PH-NW.ipynb`**:
    * **Purpose**: Full multivariate embedding point clouds Persistent Homology Analysis.
    * **Description**: 4.2 Identification of market structure status combined with policy variables
    (joint embedding point cloud of all policy variables and lagged housing prices)
    * **Input**: 'London_Housing_Policy_Dataset_sd.csv','London_Housing_Policy_Dataset_sd.csv'
    * **Output**: 'norm-LD.csv','norm-NW.csv'
    
5.  **`Sensitivity.ipynb`**:
    * **Purpose**: Sensitivity Analysis.
    * **Description**: sensitivity analyses on two key parameters of the model: the size of the sliding window and the threshold used to define high and low norm periods.

## How to Run
To run the code, you will need Python and the following main libraries. It is recommended to use a virtual environment manager like `conda` or `venv`.

* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn
* gudhi
* tqdm

### Steps

1.  Clone this repository to your local machine:
    ```bash
    git clone https://github.com/w1ldfire1/ERP-Leming-liu-2025.git
    ```
2.  Navigate into the project directory:
    ```bash
    cd ERP-Leming-liu-2025
    ```
3.  Create and activate a virtual environment, then install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open Jupyter Notebook or Jupyter Lab and run the `.ipynb` files in the order suggested in the **Code Description** section.

## Reproducibility Statement

This repository is structured to ensure full reproducibility of the research, as per the guidelines of the MSc Data Science programme. The provided notebooks, when run in the suggested order, will regenerate all key figures, tables, and analytical results presented in the dissertation.

## Contact

For any questions regarding the code or the research project, please feel free to contact Leming Liu at [leming.liu@postgrad.manchester.ac.uk].
