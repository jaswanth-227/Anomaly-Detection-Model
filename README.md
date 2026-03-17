🚀 Anomaly Detection using Attention-Fusion & Transformer-VAE

A hybrid approach of deep learning and unsupervised learning for accurate detection of identity compromise attacks with minimum false positive rates.

📌 Overview

This repository includes an implementation of an advanced anomaly detection system developed as part of the ISR Labs Bootcamp.

The system focuses on detecting identity compromise attacks in modern enterprise environments, where attackers mimic legitimate user behavior and traditional rule-based systems fail to respond effectively.

The system integrates a hybrid approach using:

🔸 Transformer Variational Autoencoder (VAE)
🔸 Unsupervised anomaly detection models
🔸 Attention-based fusion mechanism

This fusion enables effective detection of anomalies in high-dimensional data.

⚠️ Problem Statement

Identity compromise is one of the leading causes of security breaches in modern systems.

Detecting such attacks is challenging due to:

✧ Sophisticated attacker behavior that mimics normal users
✧ High-dimensional and heterogeneous data
✧ Non-linear relationships between features
✧ Limitations of traditional rule-based and signature-based systems

To address these challenges, the project proposes a hybrid system combining deep representation learning, unsupervised anomaly detection, and attention-based decision fusion.

🚀 Proposed Methodology

The system follows a multi-stage hybrid methodology designed to maximize accuracy while minimizing false positives.

🔷 Latent Feature Extraction

✦ Patch-Transformer Variational Autoencoder (VAE) is utilized
✦ Data is mapped to a 32-dimensional latent space
✦ Captures complex non-linear patterns and behavioral normalcy

🔷 Unsupervised Ensemble Models

✦ Three anomaly detection models operate independently on latent features

✦ Isolation Forest → detects anomalies using isolation
✦ One-Class SVM → learns boundary of normal behavior
✦ Local Outlier Factor → detects density-based anomalies

✦ Each model generates independent anomaly scores

🔷 Attention-Based Fusion

✦ Implemented using PyTorch Multi-Head Attention
✦ Dynamically assigns weights to model outputs
✦ Aggregates scores to produce final prediction

🛠️ Implementation Highlights

🔵 Mixed-type preprocessing:

    ✦ RobustScaler for numerical features
    ✦ OneHotEncoder for categorical features

🔵 Automatic threshold tuning using F1-score optimization

🔵 Early stopping applied to:

    ✦ VAE training
    ✦ Attention fusion model

🔵 Modular and scalable architecture

🧠 Models Used

▸ Isolation Forest
▸ One-Class SVM
▸ Local Outlier Factor
▸ Transformer VAE
▸ Attention Fusion Model

💡 Applications

The system can be applied in:

▪ Identity compromise detection
▪ Fraud detection systems
▪ Network intrusion detection
▪ User behavior analytics

🔍 Key Contributions

▪ Transformer-based latent feature extraction for anomaly detection
▪ Ensemble of multiple unsupervised detection techniques
▪ Attention-based fusion for improved decision-making
▪ Significant improvement in detection accuracy and robustness

🛠️ Tech Stack

➤ Deep Learning: PyTorch
➤ Machine Learning: Scikit-learn
➤ Data Processing: Pandas, NumPy
➤ Preprocessing: RobustScaler, OneHotEncoder
➤ Model Serialization: Joblib

👨‍💻 Team

Decoders

SUNKARA MANOJ KUMAR

YADURLA JASWANTH

⭐ Acknowledgment

Developed as part of the ISR Labs Bootcamp, focusing on solving real-world cybersecurity challenges.
