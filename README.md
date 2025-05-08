# 🧬  Advanced-Skin-Disease-Diagnosis-Using-Deep-Learning

This project presents a multimodal, multiclass skin disease classification system developed using state-of-the-art deep learning techniques. The goal is to provide a reliable AI-based diagnostic aid for a variety of skin conditions using advanced modeling strategies.

The system leverages:

✅ Focal Loss & Categorical Cross-Entropy Loss

✅ Data augmentation for better generalization

✅ Transfer learning with Xception architecture

✅ Fine-tuning for improved accuracy on specific categories

# 📁 Datasets
Datasets used in this project are available here : https://www.kaggle.com/meriemaadou/datasets

# 🤖 Pretrained Models
Pretrained .h5 model files (including model weights and architectures of model trained using cce"categorical cross entropy loss ") are available for download:
https://www.kaggle.com/meriemaadou/models

# 🧠 Project Structure
```bash
main/
├── xception-focal-loss.ipynb               # Training using Focal Loss with adjusted alpha
├── xception-cce-class_weights.ipynb       # Training using CCE Loss with class weights
├── acne-rosacea.ipynb                     # Transfer learning for acne & rosacea classification
├── bullous.ipynb                          # Transfer learning for bullous skin conditions
├── eczema.ipynb                           # Transfer learning for eczema-related conditions
├── skin-cancer.ipynb                      # Transfer learning for skin cancer classification
└── README.md                              # Project documentation
```

#🧪 Comparative Model Training
Two versions of the main classification model were trained using different loss functions to evaluate their performance:

CCE Model: Trained with Categorical Cross-Entropy (CCE) and class weights.
✅ Achieved slightly better overall accuracy.

Focal Loss Model: Trained with Focal Loss, which emphasizes hard-to-classify examples.
✅ Performed better on minority classes (bullous).

Although both models performed well, the CCE model was selected as the base for transfer learning, due to its consistent performance across all classes.

# 🔁 Transfer Learning & Fine-Tuning
Each category-specific model (acne-rosacea, bullous, eczema, skin cancer) was developed by:

Using the CCE-trained Xception model as the base.

Training on a targeted dataset for that skin condition.

Freezing all layers, training for 5 epochs.

Gradually unfreezing layers (5 at a time) every 5 epochs to fine-tune.


# 📊 Evaluation Metrics
Models were evaluated(on both validation and test sets) using:

✅ Accuracy

✅ F1-Score

✅ Precision & Recall

✅ Confusion Matrices 
