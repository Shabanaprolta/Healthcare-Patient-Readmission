# Healthcare-Patient-Readmission-Prediction
## Project Overview
This project predicts patient readmission in a hospital setting using machine learning and provides actionable insights via a dashboard. The model helps identify patients at higher risk of readmission and supports hospital decision-making for improved patient care and resource management.
## Project Structure
healthcare-readmission/
│
├── patients.csv # Patient dataset (synthetic/realistic healthcare data)
│
├── readmission_model.ipynb # Data cleaning, EDA, ML model
│--requirements.txt # Python dependencies
├── dashboard/
│ ├── Healthcare_Readmission.xlsx # Excel dashboard
│ └── Healthcare_Readmission.pdf # Dashboard export
└── README.md # Documentation


## Dataset Description
The dataset contains the following columns:

| Column               | Description |
|---------------------|-------------|
| PatientID           | Unique patient identifier |
| Age                 | Patient age (numeric or categorical: 0-9, 20-29, …, 80+) |
| Gender              | Male/Female |
| AdmissionType       | Emergency, Elective, Urgent |
| PrimaryDiagnosis    | Heart Failure, Diabetes, Pneumonia, Hypertension, Renal Failure, COPD, Other |
| LengthOfStay        | Number of days hospitalized |
| NumLabProcedures    | Number of lab tests performed |
| NumMedications      | Number of medications prescribed |
| PreviousAdmissions  | Number of prior hospitalizations |
| DischargeDisposition| Home, Nursing Facility, Transfer |
| Readmitted          | Target variable (Yes/No) |

## Workflow

### 1. Data Cleaning & EDA
- Handle missing values
- Encode categorical variables
- Explore readmission trends by:
  - Age group
  - Gender
  - Primary diagnosis
  - Length of stay

### 2. Model Building
- Train/Test split
- Algorithms used:
  - Logistic Regression
  - Random Forest
  - XGBoost
- Model Evaluation Metrics:
  - Accuracy, Precision, Recall, F1-score
  - ROC-AUC
- Feature importance analysis to identify key readmission drivers

### 3. Dashboard (Excel )
- **KPIs**:
  - Total Patients: 5000
  - Percent Readmitted Patients: 17%
  - Average Length of Stay: 4.62 days
- **Charts**:
  - Readmission by Age Group
  - Readmission Rate by Gender
  - Readmission by Top Diagnosis
  - Length of Stay Comparison (Readmitted vs Not)
- Filters for interactive analysis:
  - Gender, Age, Primary Diagnosis, Discharge Disposition

## Key Insights
- Readmission is higher in older patients (70-79, 80+ age groups)
- Male patients have slightly higher readmission rates than female
- Heart Failure shows the highest readmission rate (33%)
- Average length of stay is higher for readmitted patients (≈5.68 days)
