# DataMining - Predicting Acute Inflammations
This repository aims to **predict acute inflammations** using clinical features through a full data-science pipeline in Python.

It demonstrates strong competency in **data visualization**, exploratory data analysis (EDA), model training and evaluation on real-world biomedical data.


## Dataset
#### `acute_inflammations.csv`
* The number of row: 120
* 6 Features
* 2 Target(Binary classification): bladder-inflammation / nephritis
|Variable Name    | 	Role|	Type        |
|`temperature`	    |Feature|	Continuous  |		
|`nausea`	          |Feature|	Categorical	|	
|`lumbar-pain`      |	Feature|	Categorical|			
|`urine-pushing`    |	Feature|	Categorical|		
|`micturition-pains`|	Feature|	Categorical|		
|`burning-urethra`  |	Feature|	Categorical|			
|**bladder-inflammation**|	**Target**|	Categorical|		
|**nephritis**        |	**Target**	|Categorical	|
#### Preprocessing
* temperature: normalization from 0 to 1


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

## EDA
* Correlation Heatmap
<img width="901" height="749" alt="image" src="https://github.com/user-attachments/assets/d808d38c-0c56-4731-a7ed-6e86bc71863c" />
* Relative Frequency Histogram
<img width="1209" height="1222" alt="image" src="https://github.com/user-attachments/assets/85d3c189-1a8a-405e-aa8c-f858772835e3" />


* Target Variable Analysis
  * Heatmap: Acute Inflammations for variables
    <img width="1098" height="386" alt="image" src="https://github.com/user-attachments/assets/3acfd894-8f56-476a-ba47-2c82a95cb4f0" />

  * Frequency Histogram: Acute Inflammations for `temperature`
  <img width="668" height="653" alt="image" src="https://github.com/user-attachments/assets/d5d22ddd-a82e-48ab-8872-cd5d261641b3" />

  * Scatter Plot: Acute Inflammations for variables
    <img width="1622" height="767" alt="image" src="https://github.com/user-attachments/assets/cba5a3f8-7300-4b10-b7b4-98c0eb537adc" />


## Evaluation & Results
* Cross-validation: `StratifiedKFold`, `n_split = 5`, `shuffling`
| | | | 



## Conclusion









