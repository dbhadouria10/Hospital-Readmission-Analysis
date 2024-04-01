# Exploring Predictive Patterns: Patient Readmissions
Explored machine learning's role in predicting hospital readmissions among diabetic patients using a Kaggle dataset of 25,000 patient records spanning a decade. Analyzed variables like diagnosis duration, hospital stay length, age, and in-patient visits to uncover predictive patterns.

# Dataset
This dataset contains information on patients who have been hospitalized for diabetes-related conditions. It includes variables such as the age bracket of the patient, the length of hospital stay, the number of procedures and medications administered, and the number of visits to outpatient and emergency rooms in the year prior to the hospitalization. The dataset also includes the medical specialty of the admitting physician, primary and secondary diagnoses, and whether the patient received glucose and A1C tests. Additionally, it indicates whether there was a change in diabetes medication and whether a diabetes medication was prescribed, as well as whether the patient was readmitted to the hospital.

## Motivation
- Our project aims to improve patient outcomes by identifying individuals at a higher risk of readmission, allowing healthcare providers to intervene and provide targeted care to prevent readmissions. 
- This project can help hospitals optimize resource allocation and reduce healthcare costs by identifying factors contributing to readmissions and implementing strategies for their mitigation. 
-  By predicting readmissions, it contributes to the overall goal of enhancing the efficiency and quality of healthcare delivery, leading to improved patient satisfaction and better allocation of healthcare resources.


## Code and Resources Used
- Python Version: 3.7
- Packages: pandas, numpy, statsmodel, scipy, matplotlib, seaborn, sklearn, imblearn Tableau Public

# Data Features – Names, Datatypes & Descriptions
### Numeric Attributes
- "n_procedures" – integer - number of procedures performed during the hospital stay
- "n_lab_procedures" - integer - number of laboratory procedures performed during the hospital stay
- "n_medications" - integer - number of medications administered during the hospital stay
- "n_outpatient" - integer - number of outpatient visits in the year before a hospital stay
- "n_inpatient" - integer - number of inpatient visits in the year before the hospital stay
- "n_emergency" - integer - number of visits to the emergency room in the year before the hospital stay
- "glucose_test" - object - whether the glucose serum came out as high (> 200), normal, or not performed
- "A1Ctest" - object - whether the A1C level of the patient came out as high (> 7%), normal, or not performed

### Categorical Attributes
- "age" - object - age group of the patient
- "time_in_hospital" – integer - days (from 1 to 14)
- "medical_specialty" – object - the specialty of the admitting physician
- "diag_1" - object - primary diagnosis (Circulatory, Respiratory, Digestive, etc.)
- "diag_2" - object - secondary diagnosis
- "diag_3" - object - additional secondary diagnosis
- "change" - object - whether there was a change in the diabetes medication ('yes' or 'no')
- "diabetes_med" – object - whether a diabetes medication was prescribed ('yes' or 'no')
- "readmitted" - object - if the patient was readmitted at the hospital ('yes' or 'no')

### Some key points
- We have balanced target variable
- We have some outliers as well, but we'll keep them for phase 1
- Most of the patients are older as we can see, we got low count in the age group (90-100), as they are very few in general population
- Most of the data doesn't have A1C and glucose test

### Data Cleaning Steps
- Columns werent removed as the all the attributes were relevant to the project
- Data type Casting
- Data Encoding


## EDA
- We used descriptive statistics for both numercial and categorical variables.
- Distrubution and relation between the numerical attributes through correlation.
- Ploting Countplots, barplots other visualization tools to infer the importance of the features.



- Summary of Numerical features
![](images/WhatsApp%20Image%202023-06-09%20at%2018.27.30.jpeg)

- Pie Chart for the variation in Target Variable
![](images/WhatsApp%20Image%202023-06-09%20at%2018.27.45.jpeg)



## Machine Learning
- The Model might overfiting we tried hyperparameter tuning and feature selection, hyperparameter tuning improve the models performance but feature selection method gave us reasonable outputs.


## Results
[](images/Screenshot%202023-06-11%20at%2023.17.41.jpg)


## Limitations
- Non-descriptive categories in some attributes
- Feature selection was challenging as the correlation of the features was difficult to establish


## Conclusion
- the ideal solution when we have infinite or enough resources is to provide post discharge care for all the patients to reduce readmission. But in a real world, it is not possible to provide care for all the patients. Hence, the hospital should filter out patients who are potential to get readmitted and can be potentially prevented. Then, they can focus their resources and help them recover without readmission in 30 days


## Contact Information
- Deepak - db3533@drexel.edu
- Jibin - jj3225@drexel.edu
- Jeromey - jja99@drexel.edu

## References
- Scikit-Learn Documentation
- (https://www.cms.gov/Medicare/Quality-Initiatives-Patient-Assessment-Instruments/Value-BasedPrograms/HRRP/Hospital-Readmission-Reduction-Program##​

- https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6614936/​

- https://scikit-learn.org/stable/supervised_learning.html#supervised-learning​)
