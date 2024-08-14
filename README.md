# **Intrusion Detection Using Machine Learning Techniques On CIC-IDS2017 Dataset**

Created By [Mohammad Amirifard](https://www.linkedin.com/in/mohammad-amirifard/)


<img src="https://www.teligentsolutions.com/wp-content/uploads/2015/04/Teligent_Solutions_Intrusion_Detection.jpg" alt="Image" />

# **Problem Statement:**
The objective of this project is to **detect** and classify various types of **anomalies** within the `CIC-IDS2017 dataset`, which is a widely recognized benchmark dataset used for cybersecurity research, particularly in the domain of intrusion detection systems (IDS). Anomalies in this context refer to unusual or suspicious patterns in the network traffic data that may indicate potential security threats such as attacks or intrusions.

To achieve this, we will apply a range of **machine learning techniques** that are commonly used for anomaly detection and classification tasks. These techniques include, but are not limited to, supervised learning methods, such as decision trees, support vector machines, and neural networks, as well as unsupervised learning approaches like clustering algorithms and autoencoders. By leveraging these methods, we aim to accurately classify network traffic data into normal and anomalous categories.

The problem we are addressing is inherently a classification problem, where the primary goal is to categorize the data into predefined classes based on the learned patterns. This involves training machine learning models on labeled data to distinguish between normal and anomalous network traffic, enabling the detection of potential security threats with high precision and recall.

# **Goal:**

Our ultimate aim is to develop a robust system that can effectively identify various types of anomalies, contributing to the enhancement of network security measures.

# **Dataset:**
you can see detail of available dataset on this [link](https://www.unb.ca/cic/datasets/ids-2017.html)

# Rpository Structure:
```
- 📦 ....
  |- 📄 README.md        #Guide file
  |- 📄 License.md      #License file
  |- 📂 Data             #Here you can see dataset link.
  |- 📂 Notebooks        #Here you can see jupyter files which should be run on Google Colab or Kaggle.
  |- 📂 Src              #Here you can see python files to run
  |- 📂 Report           #Here you can see a complete report of what we have done.
```

# **Structure of notebooks**
`This program includes several notebooks regarding different parts.

1.   Notebook number 1, [Part1_EDA](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part1_EDA.ipynb)
2.   Notebook number 2, [Part2_KNN_Models](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part2_KNN_Models.ipynb)
3.   Notebook number 3, [Part3_SVM_Models](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part3_SVM_Models.ipynb)
4.   Notebook number 4, [Part4_Gboost_Model](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part4_GBoost_Model.ipynb)
5.   Notebook number 5, [Part5_MLP_Model](https://github.com/Mohammad-Amirifard/Intrusion_Detection/blob/main/Notebooks/Part5_MLP_Model.ipynb)



# **Guide to run:**
# Option 1: Run it locally.For this, copy and paste the following commands in terminal of your IDE.
Step 1: 
```
git clone https://github.com/Mohammad-Amirifard/Intrusion_Detection.git
```
Step 2:
```
cd .\Intrusion_Detection\
```
 
Step 3:
```
pip install -r .\requirement.txt
```
Step 4: 
```
jupyter notebook
```
Step 5: Run each file you need. There is no necessity to run them in order.

# Option 2: Run files on Colab or Kaggle. There is no necessity to run them in order.


# Result



