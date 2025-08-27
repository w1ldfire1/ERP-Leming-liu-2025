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
 
The repository provides all code, instructions, and additional materials required to reproduce the analyses presented in the dissertation.

---

## Repository Structure
├── Joint embedding PH-LD.ipynb
├── Joint embedding PH-NW.ipynb
├── London_Housing_Policy_Dataset.csv
├── London_Housing_Policy_Dataset_sd.csv
├── North_West_Housing_Policy_Dataset.csv
├── North_West_Housing_Policy_Dataset_sd.csv
├── README.md
├── Section 3 Method Visualiaztion.ipynb
├── Sensitivity.ipynb
├── norm-LD.csv
├── norm-NW.csv
├── preprocessing.ipynb
├── univariate lagged_London.ipynb
└── univariate lagged_NW.ipynb

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
      
2.  **`Section 3 Method Visualiaztion.ipynb`**:
    * **Purpose**: Method Visualization.
    * **Description**: 

3.  **`univariate lagged_London.ipynb` / `univariate lagged_NW.ipynb`**:
    * **Purpose**: Core Model Implementation.
    * **Description**: 4.1 Housing price univariate lagged persistent homology; 4.3 Correlation Changes in Different Norm Periods(Calculating Rolling Correlation); 4.4 Regional Heterogeneity Analysis(joint embedding of single policy variables and housing prices)

4.  **`Joint embedding PH-LD.ipynb` / `Joint embedding PH-NW.ipynb`**:
    * **Purpose**: Core Model Implementation.
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

To ensure reproducibility, you can generate a `requirements.txt` file by running the following command in your terminal and uploading it to this repository:
```bash
pip freeze > requirements.txt
```

### Steps

1.  Clone this repository to your local machine:
    ```bash
    git clone [https://docs.github.com/en/get-started/using-github/connecting-to-github](https://docs.github.com/en/get-started/using-github/connecting-to-github)
    ```
2.  Navigate into the project directory:
    ```bash
    cd [name-of-your-project-directory]
    ```
3.  (Optional but recommended) Create and activate a virtual environment, then install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open Jupyter Notebook or Jupyter Lab and run the `.ipynb` files in the order suggested in the **Code Description** section.
