# Membership-Inference-Attack-on-Text-Based-Linkage-Models

This prototype presents a **Membership Inference Attack (MIA)** to evaluate vulnerabilities of privacy-preserving text data linkage models. It simulates a real-world attacker attempting to infer whether specific sensitive records (e.g., patient details) were included in the training data of a machine learning-based record linkage system.

The project was developed as part of a final-year university PACE unit focused on **offensive security**, **privacy testing**, and **machine learning-based** techniques.

---

## 🔍 Project Objective

Modern data linkage systems - used in sectors like healthcare — often rely on neural network models to match unstructured text records. While powerful, these models are vulnerable to inference attacks that can compromise data privacy even when datasets are hidden.

This repository demonstrates:
- How an attacker can train a **shadow model** to mimic the target linkage system
- How to craft an **attack model** that exploits confidence scores and distances to infer record membership
- The **privacy risks** involved when publishing or deploying machine learning models trained on sensitive text-based data

---

## 🧪 Tools & Techniques

The project involves two core components:

### 1. Training Shadow Model
- Trained on synthetic text-based record pairs
- Outputs embedding distances to simulate the decision boundary of the target model
- Uses loss and a contrastive learning approach for pair similarity

### 2. Attack Model
- Uses confidence thresholds and output embeddings from the shadow model
- Trained to classify whether a record was *in* or *out* of the training dataset
- Evaluated using precision, recall, and membership inference success rate
