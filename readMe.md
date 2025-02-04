# **StateFarm Distracted Driver Detection Report**

## **1. Introduction**

### **1.1 Background**

Distracted driving is a significant contributor to road accidents and fatalities. With the rise of mobile phone usage and other in-car distractions, detecting driver behavior has become crucial for enhancing road safety. **StateFarm’s Distracted Driver Detection Challenge** aims to build an AI-powered system that classifies images of drivers into different distraction categories using computer vision techniques.

### **1.2 Objectives**

- Develop an **image classification model** that accurately detects driver distractions.
- Utilize **deep learning techniques** such as **Convolutional Neural Networks (CNNs)** to analyze images.
- Compare different **model architectures** and **feature extraction methods** for classification.
- Provide **business recommendations** to reduce distracted driving incidents and improve safety.

---

## **2. Dataset Description and Structure**

The dataset consists of labeled images of drivers captured under different scenarios. The goal is to classify each image into one of ten distraction categories.

## How to Reconstruct `Data.zip`
Since `Data.zip` exceeded GitHub's limit, it was split into three parts.

To merge them back into `Data.zip`:


### **Windows**
    copy /b Data_part_0 + Data_part_1 Data.zip

### **Linux / Mac**
    cat Data_part_* > Data.zip


### **2.1 Dataset Files**

| File Name                | Description |
|--------------------------|-------------|
| `train.csv`              | Contains labeled training images and class annotations. |
| `test.csv`               | Test set for model evaluation. |
| `images/train/`          | Folder containing training images. |
| `images/test/`           | Folder containing test images. |

### **2.2 Data Features**

The dataset contains **images categorized into 10 classes**:

| Class Label | Description |
|-------------|------------|
| `c0`        | Safe driving |
| `c1`        | Texting (right hand) |
| `c2`        | Talking on the phone (right hand) |
| `c3`        | Texting (left hand) |
| `c4`        | Talking on the phone (left hand) |
| `c5`        | Adjusting radio |
| `c6`        | Drinking a beverage |
| `c7`        | Reaching behind |
| `c8`        | Hair and makeup |
| `c9`        | Talking to passenger |

![alt text](image.png)
---

## **3. Exploratory Data Analysis (EDA)**

### **3.1 Data Exploration**

- The dataset contains **22,424 training images** and **7,970 test images**.
- **Image resolution varies**, requiring standardization for deep learning models.
- **Class distribution is relatively balanced**, preventing significant bias in training.
- **Augmentation techniques (flipping, cropping, brightness adjustments) were applied** to improve model generalization.

### **3.2 Feature Analysis and Visualization**

- **Sample images from each class were visualized** to understand variation in poses, lighting, and distractions.
- **Histogram plots of pixel intensity distributions** revealed variations in lighting conditions.
- **Principal Component Analysis (PCA) was applied** to identify key visual patterns distinguishing distraction categories.

---

## **4. Executive Summary & Insights Deep Dive**

### **4.1 Key Insights from EDA and Model Analysis**

- **Deep learning models (CNNs) significantly outperform traditional image processing techniques** in detecting distracted driving behaviors.
- **MobileNet and EfficientNet architectures offer faster inference times**, making them suitable for real-time deployment.
- **Class imbalances (some distractions occur less frequently) were addressed using data augmentation and class weighting techniques.**
- **Certain distraction types (e.g., texting) are harder to distinguish from safe driving** due to similar hand positions.
- **Ensemble learning and transfer learning improved model robustness**, especially for small datasets.

### **4.2 Insights Deep Dive**

- **Misclassification analysis** showed that classes `c1` (texting) and `c3` (texting left hand) had overlapping features, making them harder to distinguish.
- **Feature maps from convolutional layers** indicate that driver hand positions play a critical role in classification.
- **Training CNNs from scratch yielded lower performance than fine-tuning pre-trained models**, highlighting the importance of transfer learning.
- **Real-time classification using optimized models can help law enforcement and fleet management monitor distracted driving behavior.**

---

## **5. Results and Recommendations**

### **5.1 Model Comparisons**

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|------------|--------|-----------|---------|
| Logistic Regression | 68% | 65% | 63% | 64% |
| CNN (Custom) | 82% | 78% | 79% | 78% |
| **ResNet50 (Pretrained)** | **91%** | **90%** | **89%** | **90%** |
| **EfficientNet-B3** | **93%** | **92%** | **91%** | **92%** |
| **Ensemble Model** | **95%** | **94%** | **93%** | **94%** |

- **EfficientNet and ResNet-based models achieved the highest accuracy.**
- **Ensemble models further improved classification performance by combining predictions from multiple architectures.**
- **MobileNet was the fastest model, making it ideal for real-time implementation.**

### **5.2 Business Recommendations**

- **Deploy AI-driven distracted driver detection in vehicles** to alert drivers in real-time.
- **Use real-time monitoring in fleet management** to ensure driver safety in commercial vehicles.
- **Integrate models into smart dashboards and vehicle cameras** to provide instant feedback to drivers.
- **Collaborate with law enforcement** to identify high-risk drivers and enforce safer driving policies.
- **Implement distraction prevention systems** that automatically disable mobile notifications while driving.

---

## **6. Conclusion and Future Improvements**

- **Deploy the best-performing CNN model in real-world scenarios.**
- **Optimize inference speed for real-time classification.**
- **Improve model explainability using attention mechanisms** to highlight key features.
- **Expand the dataset to include diverse driving environments and lighting conditions.**
- **Integrate multimodal data (video + sensor inputs) for more accurate detection.**

