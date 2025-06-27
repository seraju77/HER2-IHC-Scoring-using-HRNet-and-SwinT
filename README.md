🧠 #BCI Image Classification with Swin Transformer and HRNet
This repository presents two powerful deep learning models—Swin Transformer and HRNet—fine-tuned for multi-class classification of brain-computer interface (BCI) signal images. The goal is to compare their performance and evaluate their suitability for visual decoding tasks from EEG-derived representations.

📁 Repository Structure

📦BCI-Image-Classification
 ┣ 📄 swint-bci-amend-90.ipynb         # Swin Transformer based model (90 epochs)
 ┣ 📄 bci-amend-hrnet-50epo-92.ipynb   # HRNet based model (50 epochs)
 ┣ 📄 README.md                        # Project overview and usage


🔍 Dataset
Source: Custom dataset uploaded to Kaggle environment.
Classes: class_0, class_1+, class_2+, class_3+ (mapped to 0–3).
Format: .png images organized in folders per class.

🧠 Models
1. Swin Transformer (90 Epochs)
Backbone: swin_base_patch4_window7_224 via timm

Training Details:
Epochs: 90
Optimizer: Adam
Loss: CrossEntropy
Performance: Achieved high accuracy with strong generalization.

2. HRNet (50 Epochs)
Backbone: hrnet_w18
Training Details:
Epochs: 50
Augmentation: Resize, Normalize, Random Affine
Optimizer: Adam
Loss: CrossEntropy
Performance: Comparable performance with excellent class-wise precision.

🛠️ How to Run
⚠️ Both notebooks are designed for execution in Kaggle with GPU enabled.
pip install torch torchvision timm pandas scikit-learn matplotlib

Run in Kaggle
Upload your dataset and place it in /kaggle/input/train-bci-amend.
Launch either notebook:
swint-bci-amend-90.ipynb
bci-amend-hrnet-50epo-92.ipynb



📌 Conclusion
Swin Transformer shows superior feature extraction with window-based attention, ideal for spatially rich BCI images.

HRNet maintains resolution and balances speed-performance, making it a solid baseline model.










