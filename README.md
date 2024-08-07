# IOT-Network-Intrusion-detection-system-using-Quantum-and-classical-Machine-Learning

## About the project
This project proposes the integration of quantum technology into an intrusion detection system, focusing on algorithms like Quantum Support Vector Classifier (QSVC) and Quantum Random Forest (QRF) machine learning models in comparison with Classical Support Vector Classifier (CSVC) and Classical Random Forest (CRF). The dataset used in all the models is UNSW-NB15. By harnessing the vast amount of UNSW-NB15 data, the models are processed in parallel using quantum technology, thereby improving computational power and speed. The results, observed by simulating QSVC and QRF in IBM Quantum Labs, show improved accuracy of 95.3% and 98%, respectively, compared to 96% accuracy for the classical CSVC and CRF methods. Further optimization of QSVC and QRF results in improved accuracy of 99.2% for QSVC and 99% for QRF. The proposed framework aims to enhance the resistance and efficiency of IDS in defending against evolutionary cyber threats in a highly interconnected digital ecosystem.

## Prerequisites

- Sklearn
- Pandas
- Numpy
- Matplotlib
- Pickle

## Running the Notebook
The notebook can be run on

Jupyter Notebook
Visual Studio Code

Clone the Repository
[git clone https://github.com/Deepakdee8/IOT-Network-Intrusion-detection-system-using-Quantum-and-classical-Machine-Learning.git
cd iot-network-ids-quantum-ml]

- install the Prerequisites to run IDS_Classical_ML

## Instructions
- you need to change the environments to run the IDS Quantum notebooks 
> **Caution - The code should be executed in the given order for best results without encountering any errors.**

### Required packages for Quantum random forest
Python=3.8.10 was used with the following libraries:

    - cirq==0.11.0
    - cirq-core==0.11.0
    - matplotlib==3.4.2
    - more-itertools==8.8.0
    - numpy==1.19.5
    - pandas==1.3.0
    - qiskit==0.27.0
    - scikit-learn==0.24.2
    - scipy==1.7.0
    - tqdm==4.61.1
    - tensorflow==2.4.1

-----

### Required packages for Quantum SVC
Python=3.8.10 was used with the following libraries:

    - matplotlib==3.4.2
    - more-itertools==8.8.0
    - numpy==1.19.5
    - pandas==1.3.0
    - qiskit==0.27.0
    - qiskit-algorithms==0.3.0                 
    - qiskit-machine-learning==0.7.2                 
    - qiskit-terra==0.25.0
    - scikit-learn==0.24.2
    - scipy==1.7.0
    - tqdm==4.61.1


-----
- <b> NOTE:</b> To run the IDS_QuantumSVC, you need to paste the "IBM API Token ID" in the notebook
- You can get the API Token by signing up here : https://quantum.ibm.com/

## Datasets
- UNSW_NB15.csv - Original Dataset
- UNSW_NB15_features.csv - 49 features with the class label, These features are described here.
- final_dataset_IDS.csv - Final CSV Dataset file for all models after data pre-processing.

## Data Preprocessing
- Dataset had **45 attributes** and **175341 rows**.
- After dropping null values Dataset had **45 attributes** and **81173 rows**.
- Data type of attributes is converted using provided datatype information from features dataset.
- ### One-hot-encoding
	- Categorical Columns  **'proto'**,  **'service'**,  **'state'**  are one-hot-encoded using  **pd.get_dummies()** and these 3 attributes are removed afterwards.
	-  **data_cat**  Dataframe had **19 attributes** after one-hot-encoding.
    - **data_cat** is concatenated with the main **data** dataframe.
	- Total attributes of **data** dataframe - **61**
- ### Data Normalization
	- **58 Numeric Columns** of DataFrame is scaled using  **MinMax Scaler**.
- ### Binary Classification
	- A copy of DataFrame is created for Binary Classification.
    - **'label'**  attribute is classified into two categories  **'normal'**  and  **'abnormal'**.
    - **'label'**  is encoded using  **LabelEncoder()**, encoded labels are saved in  **'label'**.
	- Binary dataset - **81173 rows**, **61 columns**

- ### Feature Extraction
	- No. of attributes of  **'bin_data'**  - **61**
	- The attributes with **more than 0.5** correlation coefficient with the target attribute  **label**  were selected.
	- No. of attributes of  **'bin_data'**  after feature selection - **4**
	-  **'sttl'**,  **'ct_state_ttl'**,  **'state_CON'**, **'state_INT'**, **'label'**

## Splitting Dataset
- Randomly Splitting the **bin_data** in **80% for training** and **20% for testing**

## IDS Classical ML Result
- ### Support Vector Classifier
	- Accuracy - **0.965**
	- Precision - **0.97** 
	- Recall - **0.96** 
	- F1-score - **0.965** 
- ### Random Forest 
	- Accuracy - **0.965**
	- Mean Absolute Error - **0.97** 
	- Mean Squared Error - **0.96** 
	- Root Mean Squared Error - **0.965** 

## IDS Quantum ML Result
- ### Support Vector Classifier
	- Accuracy - **0.992**
	- Precision - **0.9933** 
	- Recall - **0.9933** 
	- F1-score - **0.9933** 
- ### Random Forest 
	- Accuracy - **0.98**
	- Mean Absolute Error - **0.98** 
	- Mean Squared Error - **0.98** 
	- Root Mean Squared Error - **0.98** 

## License
This project is licensed under the MIT License. See the LICENSE file for details.


## Contact

For any questions or suggestions, please contact deepakdeepu101011@gmail.com.











