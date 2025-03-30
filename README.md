# **Semantic Segmentation Using AWS SageMaker**

## 📌 Project Overview
This project implements **semantic segmentation** using **AWS SageMaker**, leveraging a **Fully Convolutional Network (FCN)** to segment pet images from the **Oxford-IIIT Pet Dataset**. The model is trained on SageMaker and deployed as an endpoint for real-time inference.

## 📂 Dataset: Oxford-IIIT Pet Dataset
The dataset consists of:
- **37 pet breeds** with labeled segmentation masks.
- Images and corresponding annotations for pixel-wise segmentation.
- Preprocessed image-mask pairs used for training.

## 🏗️ Model Architecture: Fully Convolutional Network (FCN)
- FCNs are designed for **pixel-wise classification**.
- No fully connected layers – maintains **spatial information**.
- Used to classify each pixel as pet or background.
- Trained using SageMaker’s **built-in Semantic Segmentation Algorithm**.

## 🚀 Training Using AWS SageMaker
AWS **SageMaker Estimator** is used for scalable model training:
1. **Data Storage:** Dataset uploaded to **Amazon S3**.
2. **Training Execution:** Runs on AWS SageMaker with a defined training script.
3. **Hyperparameters:** Configured for optimal learning.
4. **Instance Used:** `ml.m4.xlarge`.
5. **Model Output:** Trained weights stored in **Amazon S3**.

### 🔧 Hyperparameters:
- **Learning Rate:** Tuned for convergence.
- **Batch Size:** Controls number of images per step.
- **Epochs:** Set to **10** for effective learning.

## 🖥️ Model Deployment & Inference
After training, the model is deployed as an **AWS SageMaker Endpoint** for real-time segmentation:
- **Input:** Image (`JPEG` format).
- **Output:** Segmented mask (`PNG` format) highlighting pets.
- **Cloud-based scalable inference** ensures efficiency.

## 📊 Model Evaluation Metrics
To measure segmentation accuracy, we use:
1. **Intersection over Union (IoU)** – Measures overlap between predicted & ground truth masks.
2. **Dice Coefficient** – Another segmentation accuracy metric.

## 🔹 Technologies & Tools Used
✔ **AWS SageMaker** – Model training & deployment  
✔ **boto3** – AWS SDK for Python  
✔ **numpy** – Numerical computations  
✔ **matplotlib** – Visualization  
✔ **PIL (Pillow)** – Image processing  
✔ **tqdm** – Loop progress visualization  
✔ **xml.etree.ElementTree** – Parsing dataset annotations  

## 📌 Summary
This project demonstrates **cloud-based deep learning** for **semantic segmentation**. Using **AWS SageMaker**, a **Fully Convolutional Network (FCN)** is trained and deployed to segment pet images efficiently. The model is scalable and performs real-time segmentation.





