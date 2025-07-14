# Network Intrusion Detection System (NIDS) using NSL-KDD Dataset

## 📌 Project Overview

This project implements a Machine Learning-based Network Intrusion Detection System (NIDS) using the NSL-KDD dataset. It identifies abnormal network traffic patterns and classifies them into different types of network attacks or as normal behavior. The system uses preprocessing techniques, feature selection, model training, and performance evaluation.

---

## 📂 Dataset

**NSL-KDD Dataset**  
- Source: [NSL-KDD GitHub Repository](https://github.com/merteroglu/NSL-KDD-Network-Instrusion-Detection)
- Files Used:
  - `NSL_KDD_Train.csv`
  - `NSL_KDD_Test.csv`

**Features:**  
41 input features + 1 label  
**Classes:** Normal, DoS, Probe, R2L, U2R (Attack categories)

---

## ⚙️ Environment Setup

```python
import pandas as pd
import numpy as np
import sys
import sklearn
import io
import random
```

---

## 🧹 Data Preprocessing

- Loaded and cleaned raw CSV data
- Converted categorical values (e.g., `protocol_type`, `service`, `flag`) to numerical form using `LabelEncoder`
- Normalized feature values for consistent input to classifiers

---

## 📊 Feature Selection

- Removed redundant and non-informative features such as `num_outbound_cmds`
- Used correlation matrices and feature importance (e.g., from Random Forest) to refine input feature set

---

## 🤖 Machine Learning Models Used

1. **Random Forest Classifier**
2. **Decision Tree Classifier**
3. **Logistic Regression**
4. **K-Nearest Neighbors (KNN)**
5. **Support Vector Machine (SVM)**
6. **Gradient Boosting Classifier**

Each model was trained on the preprocessed training data and evaluated on the test set.

---

## 📈 Evaluation Metrics

- Accuracy
- Confusion Matrix
- Precision, Recall, F1-Score
- ROC Curve (for binary and multi-class)

---

## 🧪 Results

| Model                 | Accuracy |
|----------------------|----------|
| Random Forest        | ~99%     |
| Decision Tree        | ~95%     |
| KNN                  | ~91%     |
| SVM                  | ~96%     |
| Logistic Regression  | ~89%     |
| Gradient Boosting    | ~98%     |

Performance varies by attack type, but ensemble models like Random Forest and Gradient Boosting consistently outperform others.

---

## 📌 Conclusion

- Feature engineering and model selection are crucial for high-accuracy intrusion detection.
- Random Forest and Gradient Boosting are most effective for detecting complex attack types.
- The system demonstrates the feasibility of ML-driven intrusion detection with real-world datasets.

---

## 🛠️ Future Enhancements

- Integrate deep learning models (e.g., LSTM, CNN) for sequential pattern recognition.
- Deploy the trained model in real-time NIDS architecture.
- Expand dataset to include modern threats and protocols.

---

## 🧾 License

This project is for educational and research purposes.
