# LiverCirrhosisPrediction_DataScience
LiverCirrhosis Disease Prediction using several ML algorithms and finalizing insights from it. 

HEALTHCARE ANALYTICS FOR DISEASE PREDICTION PROJECT DOCUMENTATION


Project Scope:

•	Analyze healthcare data to predict the likelihood of a disease.
•	Utilize machine learning algorithms for classification.
•	Provide insights for early intervention and prevention.
Objective
In liver cirrhosis, there are mainly 4 stages which are as follows:
a.	Stage 1 : Normal
b.	Stage 2 : Fatty Liver
c.	Stage 3 : Liver Fibrosis
d.	Stage 4 : Liver Cirrhosis
The primary target is to predict the stage of the liver cirrhosis disease. The dataset consists of both numerical as well as categorical features.

Data Sources:
   - Collect relevant healthcare data from sources such as electronic health records (EHRs), medical databases, or public health datasets.


Dataset: cirrhosis.csv

Context:

Cirrhosis is a late stage of scarring (fibrosis) of the liver caused by many forms of liver diseases and conditions, such as hepatitis and chronic alcoholism. The following data contains the information collected from the Mayo Clinic trial in primary biliary cirrhosis (PBC) of the liver conducted between 1974 and 1984. A description of the clinical background for the trial and the covariates recorded here is in Chapter 0, especially Section 0.2 of Fleming and Harrington, CountingProcesses and Survival Analysis, Wiley, 1991. A more extended discussion can be found in Dickson, et al., Hepatology 10:1-7 (1989) and in Markus, et al., N Eng J of Med 320:1709-13 (1989).

A total of 424 PBC patients, referred to Mayo Clinic during that ten-year interval, met eligibility criteria for the randomized placebo-controlled trial of the drug D-penicillamine. The first 312 cases in the dataset participated in the randomized trial and contain largely complete data. The additional 112 cases did not participate in the clinical trial but consented to have basic measurements recorded and to be followed for survival. Six of those cases were lost to follow-up shortly after diagnosis, so the data here are on an additional 106 cases as well as the 312 randomized participants.

Attribute Information

1) ID: unique identifier
2) N_Days: number of days between registration and the earlier of death, transplantation, or study analysis time in July 1986
3) Status: status of the patient C (censored), CL (censored due to liver tx), or D (death)
4) Drug: type of drug D-penicillamine or placebo
5) Age: age in [days]
6) Sex: M (male) or F (female)
7) Ascites: presence of ascites N (No) or Y (Yes)
8) Hepatomegaly: presence of hepatomegaly N (No) or Y (Yes)
9) Spiders: presence of spiders N (No) or Y (Yes)
10) Edema: presence of edema N (no edema and no diuretic therapy for edema), S (edema present without diuretics, or edema resolved by diuretics), or Y (edema despite diuretic therapy)
11) Bilirubin: serum bilirubin in [mg/dl]
12) Cholesterol: serum cholesterol in [mg/dl]
13) Albumin: albumin in [gm/dl]
14) Copper: urine copper in [ug/day]
15) Alk_Phos: alkaline phosphatase in [U/liter]
16) SGOT: SGOT in [U/ml]
17) Triglycerides: triglicerides in [mg/dl]
18) Platelets: platelets per cubic [ml/1000]
19) Prothrombin: prothrombin time in seconds [s]
20) Stage: histologic stage of disease (1, 2, 3, or 4)




Data Cleaning:

Handle missing values:

Missing values are common in healthcare data due to various reasons such as data entry errors, equipment malfunction, or patients skipping certain tests. It's crucial to handle missing values appropriately as they can significantly impact the analysis. Techniques for handling missing values include:
   - Imputation: Replace missing values with a calculated estimate such as mean, median, or mode of the corresponding feature.
   - Deletion: Remove records or features with a high percentage of missing values if they don't hold significant importance.
   - Predictive modeling: Use machine learning algorithms to predict missing values based on other features.

Handle outliers:

Outliers are data points that significantly deviate from the rest of the data. In healthcare data, outliers can occur due to measurement errors, extreme cases, or anomalies. It's essential to identify and address outliers appropriately:
   - Visual inspection: Plotting histograms, box plots, or scatter plots can help identify outliers visually.
   - Statistical methods: Techniques such as z-score, interquartile range (IQR), or Tukey's method can be used to detect outliers statistically.
   - Transformation: Transforming skewed data using techniques like logarithmic transformation can mitigate the impact of outliers.
   - Trimming or winsorization: Assigning extreme values to the nearest non-outlier values or removing extreme values beyond a certain threshold.

Inconsistencies:

In healthcare data, inconsistencies can arise due to variations in data entry methods, coding errors, or inconsistencies in recording formats. To address inconsistencies:
   - Standardize data formats: Ensure consistency in date formats, coding systems (e.g., ICD-10 for diagnoses), and units of measurement.
   - Data validation: Implement validation checks to identify and correct inconsistencies in the data.
   - Data profiling: Analyze the data to identify patterns and inconsistencies, then correct them manually or programmatically.







Feature Engineering:

Patient demographics:
Demographic features such as age, gender, ethnicity, socioeconomic status, and geographic location can provide valuable insights into disease prediction. These features can be directly extracted from patient records or derived from additional sources.

Medical history:
Past medical history including pre-existing conditions, previous treatments, surgeries, medications, and lifestyle factors play a crucial role in disease prediction. Creating features that capture the presence, severity, and duration of medical conditions can enhance predictive models.

Diagnostic test results:
Results from diagnostic tests such as blood tests, imaging studies (e.g., X-rays, MRI), and genetic tests contain valuable information for disease prediction. Feature engineering involves transforming raw test results into meaningful features such as abnormality scores, biomarker levels, or disease risk scores.

Temporal features:
Time-related features such as frequency of hospital visits, time since diagnosis, or temporal patterns in symptoms can provide valuable insights into disease progression and prognosis.

Composite features:
Combining multiple related features or creating interaction terms can capture complex relationships and improve predictive performance. For example, creating a feature that combines age and comorbidity status to assess overall disease risk.

Dimensionality reduction:
Techniques such as principal component analysis (PCA) or feature selection methods can be used to reduce the dimensionality of the feature space while retaining relevant information and improving model efficiency.

By performing effective data cleaning and feature engineering, healthcare data can be transformed into a high-quality dataset suitable for building accurate and reliable predictive models for disease diagnosis, prognosis, and treatment planning.


