 Anomaly Detection using Attention-Fusion & Transformer-VAE

A hybrid approach that leverages the power of deep learning and unsupervised learning for precise anomaly detection with low false positive rates for identity compromise attacks.

📌 Overview

The proposed solution offers an advanced multi-stage anomaly detection system that incorporates the following:

🧠 Deep learning-based feature extraction using a Transformer-based Variational Autoencoder (VAE)

🔍 Multiple unsupervised anomaly detection models

🎯 An Attention-based fusion mechanism for the final prediction

The proposed solution is well-suited for modern enterprise security scenarios where attackers use mimicry attacks.

🚀 Methodology & Architecture
The pipeline follows a hybrid architecture designed to maximize detection precision while minimizing false positives:

1. Latent Feature Extraction
Raw data is processed through a Patch-Transformer Variational Autoencoder (VAE). This stage projects high-dimensional tabular data into a 32-dimensional latent space, capturing complex non-linear dependencies and structural "normalcy".

2. Unsupervised Ensemble
Three industry-standard outlier detection models are trained on the extracted latent features to generate independent anomaly scores:

Isolation Forest: Detects isolation-based outliers.

One-Class SVM: Identifies boundary-based deviations.

Local Outlier Factor (LOF): Evaluates local density deviations.

3. Attention-Based Fusion
The final decision layer is a PyTorch-based Attention-Only Fusion model. It utilizes a Multi-head Attention mechanism to dynamically weight and aggregate scores from the ensemble into a final supervised prediction.

📊 Performance Benchmark
The Decoders team achieved high-fidelity results on the test set, demonstrating the effectiveness of the attention-fusion approach:

Metric	Score
Accuracy	99.07%
Precision	91.13%
F1-Score	0.8248
ROC-AUC	0.9961

🛠️ Implementation Highlights
Mixed-Type Preprocessing: Seamlessly handles numeric features via RobustScaler and categorical features via OneHotEncoder.

Optimal Thresholding: Decision boundaries are automatically tuned on validation data to maximize the F1-score.

Overfitting Protection: Both the VAE and Fusion training loops implement Early Stopping based on validation loss.

📁 Repository Structure
Anomaly detection final.ipynb: The primary end-to-end research and training pipeline.

trained_model.pkl: Serialized production-ready fusion model.

/outputs/: Granular metrics, confusion matrices, and classification reports for individual models.

/outputs_attention_only/: Final performance summaries for the fused ensemble.

⚙️ Tech Stack
Deep Learning: PyTorch

Machine Learning: Scikit-Learn

Analysis: Pandas, NumPy

Deployment: Joblib

Project Team: Decoders

Developers:SUNKARA MANOJ KUMAR, JASWANTH YADURLA
