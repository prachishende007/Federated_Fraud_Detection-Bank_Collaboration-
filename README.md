# Federated Fraud Detection: Bank Collaboration

![Federated Learning](https://img.shields.io/badge/Focus-Federated%20Learning-orange)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Domain-Fraud%20Detection-red)

## 📌 Project Overview
This repository contains a decentralized framework for detecting fraudulent financial transactions through **Federated Learning (FL)**. In a traditional setup, banks must share sensitive customer data with a central server to train a robust model. This project implements a collaborative approach where multiple "Bank Clients" train a shared global model without ever exchanging raw transaction data.

## 🚀 Key Features
* **Privacy-Preserving Collaboration:** Enables banks to improve fraud detection accuracy by learning from global patterns while keeping local data on-premises.
* **Non-IID Data Handling:** Designed to manage the "Non-Independent and Identically Distributed" nature of financial data across different banking institutions.
* **Secure Aggregation:** Implements a central server to aggregate model weights (e.g., using FedAvg) rather than data points.
* **Performance Monitoring:** Includes metrics for Precision-Recall and F1-Score, which are critical for imbalanced fraud datasets.

## 🛠️ Technical Stack
* **Languages:** Python
* **ML Libraries:** TensorFlow / PyTorch, Scikit-Learn
* **FL Frameworks:** (e.g., Flower, OpenMined, or Custom Simulation)
* **Data Processing:** Pandas, NumPy

## 🏗️ System Architecture

1. **Local Training:** Each bank client trains a local model on its own transaction history.
2. **Weight Export:** Clients send only the model gradients/weights to the central server.
3. **Global Aggregation:** The server averages these weights to update the Global Fraud Model.
4. **Synchronization:** The updated global model is sent back to all participating banks.

## 📊 Results & Evaluation
The model is evaluated against standard fraud detection benchmarks, focusing on:
* **Detection Rate:** Identifying fraudulent transactions with high sensitivity.
* **False Positive Rate:** Minimizing "false alarms" for legitimate customers.
* **Convergence Rate:** How quickly the global model reaches optimal performance compared to localized models.

## 📂 Project Structure
```text
├── data/               # Simulation scripts for generating bank-specific datasets
├── models/             # Local and Global model architectures
├── notebooks/          # Exploratory Data Analysis and FL simulations
├── src/                # Core logic for Federated Aggregation (FedAvg)
└── requirements.txt    # Project dependencies

```
## 🤝 Contributing
This is an ongoing research project exploring the bounds of Differential Privacy and Secure Multi-Party Computation in Fintech. Contributions and feedback are welcome!

Developed by Prachi Shende
