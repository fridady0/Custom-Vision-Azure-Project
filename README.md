# 🐟 Fish Classification Azure Custom Vision Project Documentation

# 1. Introduction
This project demonstrates how to build a custom image classification model using Microsoft Azure's Custom Vision service. The project uses a fish dataset with multiple categories (Catfish, Goldfish, Mullet, Green Puffer, Bangus) to train, evaluate, and deploy a computer vision model.

## 🎥 Project Demo 

Check out the full video tutorial here:  
👉 [Watch on YouTube](https://www.youtube.com/watch?v=PSHZJC1VvvI)  
[![Watch the video](https://img.youtube.com/vi/PSHZJC1VvvI/0.jpg)](https://www.youtube.com/watch?v=PSHZJC1VvvI)


# 2. Features
  - Upload and label custom image datasets
  - Train classification models (multiclass / multilabel)
  - Evaluate model performance using precision, recall, and average precision (AP)
  - Test models with new images (URL or local)
  - Publish and export models for integration into applications

# 3. Setup & Installation

  To set up the project, follow these steps:
  1. Sign in to the Azure Portal (https://portal.azure.com).
  2. Create a new Custom Vision resource:
     - Resource Group: create a new one (e.g., customvision-project01)
     - Training Resource: Standard (or Free if available)
     - Prediction Resource: Standard
  3. Deploy the resources.
  4. Navigate to https://customvision.ai and sign in with your Azure credentials.
  5. Create a new project (e.g., 'Fish Classification Project').
     - Project Type: Classification
     - Classification Type: Multiclass
     - Domain: General A2 (optimized for accuracy and speed)
  4. Dataset - The dataset consists of fish images across multiple categories:
      - Catfish
      - Goldfish
      - Mullet
      - Green Puffer
      - Bangus
  
  Each category contains around 45–50 labeled images. Duplicate images were automatically filtered by Custom Vision during upload.

# 5. Training Process

1. Upload training images and assign them to appropriate tags.
2. Use the 'Quick Training' option to start training (or 'Advanced Training' for higher accuracy at the cost of longer training time).
3. After training completes, model performance metrics are displayed:
   - Precision: Likelihood of correct predictions when a tag is assigned.
   - Recall: Percentage of actual tags correctly identified by the model.
   - Average Precision (AP): Summarized precision/recall across thresholds.
4. Example performance achieved in this project showed near 100% precision and recall for several fish categories.
6. Testing & Evaluation
The trained model can be tested using either:
    - Image URL (directly from the web)
    - Local image upload

During testing, the model assigns probabilities to each tag. For example:
    - A goldfish image was predicted with 99.9% probability.
    - A green puffer image was predicted with 76.2% probability (slightly lower due to dataset variation).

Users can adjust the probability threshold to balance precision and recall depending on use case requirements.

# 7. Deployment & Export

Once satisfied with the training results, the model can be published. Published models provide prediction endpoints and can be integrated into applications. Developers can export trained models for use in mobile or edge devices.

# 8. Project Structure


```
[Azure Portal]
     │
     ▼
Create Custom Vision Resource
     │
     ▼
[CustomVision.ai Website]
     │
     ▼
Create Project → (Classification / Multiclass / Domain: General A2)
     │
     ▼
Upload Dataset → Tag Images (Catfish, Goldfish, etc.)
     │
     ▼
Train Model → (Quick Training or Advanced Training)
     │
     ▼
Evaluate Model → Precision / Recall / AP
     │
     ▼
Test Model → (Local Upload / Image URL)
     │
     ▼
Publish Model → Get Endpoint & Keys
     │
     ▼
(Optional) Export Model → TensorFlow / ONNX / Docker / Mobile
```

# 9. Code of Conduct
This project follows the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code and foster a welcoming and respectful environment.

# 11. License
This project is licensed under the MIT License. You are free to use, modify, and distribute it with proper attribution.

# 🙏 Acknowledgments

Special thanks to **Mark Daniel Lampa** for providing the Fish Dataset, which was used to train and evaluate the classification model in this project.

**Dataset Source: Fish Species Image Dataset by Mark Daniel Lampa.**

The dataset contains multiple categories of fish (e.g., Catfish, Goldfish, Mullet, Green Puffer, Bangus and many more), which enabled the creation of this custom vision classification model.

⚠️ Note: This dataset is used strictly for educational and demonstration purposes in showcasing Azure Custom Vision service.
