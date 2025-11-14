# DataMining - Predicting Acute Inflammations
This repository aims to **predict acute inflammations** using clinical features through a full data-science pipeline in Python.

It demonstrates strong competency in **data visualization**, exploratory data analysis (EDA), model training and evaluation on real-world biomedical data.


## Dependencies
The following libraries are required to run this project:
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
You can install the project dependencies via pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```


## Usage
1. Clone the repository:

2. Move to the project directory:

3. Open and run `Predicting_AcuteInflammations.ipynb` in Jupyter:
```bash
jupyter notebook Predicting_AcuteInflammations.ipynb
```


## Dataset
[acute_inflammations.csv](https://github.com/YewonMin/DataMining_Predicting-Acute-Inflammations/blob/main/acute_inflammations.csv)
* The number of row: 120
* 6 Features
* 2 Target(Binary classification): bladder-inflammation / nephritis

| **Variable Name** | 	**Role** |	 **Type**  |
|-------------------|-----------|------------|
|`temperature`	     |Feature |	Continuous  |		
|`nausea`	          |Feature |	Categorical	|	
|`lumbar-pain`      |	Feature|	Categorical |			
|`urine-pushing`    |	Feature|	Categorical |		
|`micturition-pains`|	Feature|	Categorical |		
|`burning-urethra`  |	Feature|	Categorical |			
|`bladder-inflammation`|	**Target**|	Categorical|		
|`nephritis`        |	**Target**	|Categorical	|

#### Preprocessing
* temperature: normalization from 0 to 1


## EDA
* Correlation Heatmap
<img width="901" height="749" alt="image" src="https://github.com/user-attachments/assets/d808d38c-0c56-4731-a7ed-6e86bc71863c" />

* Relative Frequency Histogram
<img width="1209" height="1222" alt="image" src="https://github.com/user-attachments/assets/4db054f9-b929-4213-a75c-321874733bac" />



* Target Variable Analysis
  * Heatmap: Acute Inflammations for variables
  <img width="1098" height="386" alt="image" src="https://github.com/user-attachments/assets/3acfd894-8f56-476a-ba47-2c82a95cb4f0" />

  * Frequency Histogram: Acute Inflammations for `temperature`
  <img width="668" height="653" alt="image" src="https://github.com/user-attachments/assets/d5d22ddd-a82e-48ab-8872-cd5d261641b3" />

  * Scatter Plot: Acute Inflammations for variables
  <img width="1622" height="767" alt="image" src="https://github.com/user-attachments/assets/cba5a3f8-7300-4b10-b7b4-98c0eb537adc" />


## Evaluation
* Training:Test = 80:20
* Cross-validation: `StratifiedKFold`, `n_split = 5`, `shuffling`
* Overall Results

| Model | Best Params | Accuracy | F1_Score |
| ------ | ---------- | -------- | -------- |
| Decision Tree | max_depth=3, min_samples_split=2 | 0.98 | 0.98 |
| Logistic Regression | C=0.01 | 1.00 | 1.00 |
| Random Forest | max_features=auto, n_estimators=10 | 0.98 | 0.98 |
| Gradient Boosting | learning_rate=0.01, max_depth=3, n_estimators=50 | 0.98 | 0.98 |
| Naive Bayes | - | 0.98 | 0.94 |
| K-Nearest Neighbors | n_neighbors=3, weights=uniform | 1.00 | 1.00 |

#### Visualization
* F1 Score Comparison
<img width="850" height="648" alt="image" src="https://github.com/user-attachments/assets/e88cb632-ca3f-4612-9f30-8baafbe77861" />

* Color DT
<img width="1446" height="1367" alt="image" src="https://github.com/user-attachments/assets/cd4cc92f-922e-4c7d-81a5-963e07fe45a4" />

* Feature importance in Random Forest
  * `urine-pushing`
  <img width="916" height="552" alt="image" src="https://github.com/user-attachments/assets/09cc1516-0c62-4f0b-95c8-980ed4c55320" />


## Conclusion
* This project conducted Python-based EDA, visualization, and multi-model evaluation to predict acute inflammations.
* Across analyses, the `Urine` feature emerged as the most influential factor in identifying acute cystitis.
* Most models, including `Logistic Regression` and `KNN`, achieved perfect accuracy (1.00), indicating that the dataset is highly separable.
* Overall, the project provides analytical support for designing an expert-system algorithm capable of performing preliminary diagnostic estimation for urological conditions.
