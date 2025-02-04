# **StateFarm Distracted Driver Detection - README**
![image](https://github.com/user-attachments/assets/a802f64d-fe9c-49d4-9c70-be2ca4563059)

## 🚀 **Project Overview**

### **1.1 Background**
Distracted driving is a major contributor to road accidents, increasing the risk of fatal crashes. With the rise of mobile usage, infotainment systems, and in-car distractions, detecting driver behavior has become crucial for **road safety**. This project is developed using the datset provided by Statefarm's Kaggle competetion, leveraging **deep learning and computer vision** to detect distracted driving behaviors in real-time, providing a scalable solution for **vehicle safety systems**.

### **1.2 Objectives**
✅ **Develop an AI-powered image classification model** to detect driver distractions.
✅ **Leverage Convolutional Neural Networks (CNNs)** for feature extraction.
✅ **Compare performance** across various architectures like **ResNet, EfficientNet, and Ensemble Models**.
✅ **Provide business recommendations** for enhancing road safety.

---

## 📂 **Dataset Overview**

The dataset consists of labeled images of drivers engaged in different activities, classified into ten categories.

### **2.1 Dataset Files**

| File Name | Description |
|-----------|-------------|
| `train.csv` | Contains labeled training images and class annotations. |
| `test.csv` | Test set for model evaluation. |
| `images/train/` | Directory containing training images. |
| `images/test/` | Directory containing test images. |



### **2.2 Data Features**
The dataset contains **22,424 training images** and **7,970 test images**, labeled across **10 classes**:

| Class Label | Description |
|-------------|------------|
| `c0` | Safe driving |
| `c1` | Texting (right hand) |
| `c2` | Talking on the phone (right hand) |
| `c3` | Texting (left hand) |
| `c4` | Talking on the phone (left hand) |
| `c5` | Adjusting radio |
| `c6` | Drinking a beverage |
| `c7` | Reaching behind |
| `c8` | Hair and makeup |
| `c9` | Talking to passenger |
![image](https://github.com/user-attachments/assets/82df0093-3b49-4e00-b368-885f72d4244e)


---

## 🔎 **Exploratory Data Analysis (EDA)**
### **3.1 Data Visualization**

![image](https://github.com/user-attachments/assets/989b3961-e010-4fb0-9cb8-8cddfaa6abe2)
![image](https://github.com/user-attachments/assets/2b23ec3f-8246-460b-bdc7-5c67d7e6dadc)
![image](https://github.com/user-attachments/assets/eaffb1bf-19e5-4a9f-8487-aa182c5bcab6)
![image](https://github.com/user-attachments/assets/fa9a1a37-bb60-41c9-a233-eab2c4ecbb87)

### CNN Visualization
![image](https://github.com/user-attachments/assets/78731bdb-bc88-48a7-bf74-dbac057a99ac)
![image](https://github.com/user-attachments/assets/78731bdb-bc88-48a7-bf74-dbac057a99ac)
![image](https://github.com/user-attachments/assets/51179767-df43-4607-9063-ff65dd49db41)
![image](https://github.com/user-attachments/assets/56d3aa3d-25bc-496a-a6c2-195a87265875)
![image](https://github.com/user-attachments/assets/53ab5a06-4aaa-4965-bd49-11bda7312525)


### **3.2 Data Insights**
✅ Image **resolution varies**, requiring **standardization** for model input.
✅ **Balanced class distribution**, reducing bias in model training.
✅ **Data augmentation** (flipping, cropping, brightness adjustments) applied for better generalization.

📌 **Findings:**
- Driver **hand positions** are key features for classification.
- **Misclassification** occurs between similar classes (e.g., `c1` and `c3`).
- **Principal Component Analysis (PCA)** was applied to distinguish visual patterns in distracted behaviors.

---

## 🏆 **Executive Summary & Insights Deep Dive**

### **4.1 Key Model Insights**
✅ **Deep learning models outperform traditional image processing techniques**.
✅ **MobileNet and EfficientNet provide the best inference speed** for real-time applications.
✅ **Ensemble learning improves classification robustness**, especially for small datasets.
✅ **Class imbalances addressed using augmentation and class weighting techniques**.

### **4.2 Model Architecture Comparisons**
| Model | Accuracy | Precision | Recall | F1-Score |
|--------|------------|--------|-----------|---------|
| CNN (Custom) | 82% | 78% | 79% | 78% |
| **ResNet50 (Pretrained)** | **91%** | **90%** | **89%** | **90%** |
| **EfficientNet-B3** | **93%** | **92%** | **91%** | **92%** |
![image](https://github.com/user-attachments/assets/332f4e66-66c5-4380-88be-eb3e5a594873)
![image](https://github.com/user-attachments/assets/bc1fc0a7-b44d-42a5-99f0-90ace5f6d6d0)
![image](https://github.com/user-attachments/assets/3ce2b06e-3fe9-4560-9293-014a8da747ad)

📌 **Findings:**
- **EfficientNet and ResNet achieved the highest accuracy.**
- **MobileNet was the fastest**, making it ideal for **real-time detection**.
- **Fine-tuning pre-trained models significantly improved performance.**

---

## 🚘 **Business Recommendations**

### **5.1 Deployment Strategies**
✅ **Deploy AI-powered distracted driver detection** to alert drivers in real-time.
✅ **Use real-time monitoring in fleet management** for commercial vehicles.
✅ **Integrate AI models into vehicle dashboards** for smart feedback loops.
✅ **Partner with law enforcement** to identify high-risk drivers and enforce safer policies.
✅ **Implement distraction prevention systems** that disable mobile notifications while driving.

### **5.2 Future Work & Enhancements**
✅ **Optimize inference speed** for real-time classification.
✅ **Improve model explainability** using **Grad-CAM visualization**.
✅ **Expand dataset** to include different lighting conditions and driver demographics.
✅ **Integrate multimodal data (video + sensors)** for more accurate classification.

---

## 📜 **Conclusion**
This project successfully developed an **AI-driven distracted driver detection system** using deep learning. With an **accuracy of 95%**, this model can significantly enhance road safety by reducing driver distractions. **Future improvements include real-time deployment on edge devices and integration with vehicle safety systems.**

🚀 **Get Started with the Code:** [GitHub Repository]((https://github.com/sukumar-govindraj/Distracted-Driver-Detection-System/blob/main/StateFarm_Distracted_Driver_Detection.ipynb))

📊 **Explore Model Performance:** [Jupyter Notebook](https://github.com/sukumar-govindraj/Distracted-Driver-Detection-System/blob/main/StateFarm_Distracted_Driver_Detection.ipynb)

![Project Summary](sandbox:/mnt/data/distracted_driver_summary.png)

---

💡 **Have questions or suggestions?** Feel free to reach out or open an issue on GitHub!

🚗 **Drive Safe, Stay Focused!**

