# Multi Modal Pipeline For Pneumonia Classification And Localization Using CNN

## 📄 Academic Status / Preprint Note
The research paper associated with this repository, **"Multi Modal Pipeline For Pneumonia Classification And Localization Using CNN,"** was peer-reviewed and accepted for the **10th International Conference on Information and Communication Technology for Competitive Strategies (ICTCS-2025)**. Due to academic timeline constraints, the final camera-ready manuscript was not submitted for formal publication. The full preprint is provided in this repository for review.

---

## 🔍 Technical Project Overview
This project implements a **two-stage multimodal deep learning pipeline** to automate the diagnosis and spatial localization of pneumonia from chest radiographs. By integrating patient metadata with image features, the system mirrors clinical decision-making to provide accurate and interpretable results.

### 🛠 Key Architectural Innovations
* **Multimodal Fusion Classifier:** Employs an **Inception-v3** backbone fused with a Metadata Encoder (MLP) to process X-ray imagery alongside patient age, sex, and modality. This stage achieved a classification **AUC of 0.9012** on the RSNA dataset.
* **Two-Stage Localization Strategy:** Standard regression-based heads were found to have limited spatial precision (mean $IoU \le 0.21$). This pipeline gates positive cases into a dedicated **YOLOv8n** detector specifically trained for bounding-box prediction.
* **Performance Optimization:** By separating classification from localization, the system improved bounding-box accuracy to a **mean IoU of 0.30** and a **median IoU of 0.29**.

---

## 💻 Tech Stack
* **Languages:** Python
* **Deep Learning:** PyTorch 2.0, TensorFlow/Keras, Ultralytics YOLOv8
* **Computer Vision:** OpenCV
* **Data Processing:** NumPy, Pandas, Scikit-learn
* **Hardware:** Trained on NVIDIA T4 GPU with mixed-precision (fp16) acceleration
