# 📌 Image Classification Using Deep Learning Architectures

This repository contains three image classification experiments using different deep learning approaches. The goal is to compare traditional CNN architectures, transfer learning models, and modern transformer-based models for supervised image classification.

---

## 📁 Repository Structure

├── ConvNeXt_+Swin_Transformer.ipynb
├── VGG19.ipynb
├── Custom_CNN_Image_Classification.ipynb
└── dataset/
├── class_1/
├── class_2/
└── class_3/


---

## 🧠 Models Implemented

### **1️⃣ Custom CNN Architecture**
A convolutional neural network built from scratch to serve as the baseline model.

**Features**
- Multiple Conv → ReLU → MaxPooling layers  
- Batch Normalization  
- Fully connected dense layers  
- Softmax output layer  
- Data augmentation  
- Early Stopping & ReduceLROnPlateau callbacks  

---

### **2️⃣ VGG19 (Transfer Learning)**
A classical ImageNet-pretrained network with excellent feature extraction capability.

**Features**
- `include_top=False` for custom head  
- Additional dense classifier layers  
- Fine-tuning of selective layers  
- High performance on small and medium datasets  

---

### **3️⃣ ConvNeXt + Swin Transformer**
Modern deep learning architectures combining convolutional updates (ConvNeXt) and hierarchical transformers (Swin).

**Features**
- Pretrained on ImageNet  
- Patch merging + shifted window attention (Swin)  
- Highly efficient and accurate  
- Fine-tuned classifier head added  

---

## 📊 Dataset

- Images are organized in **class-wise folders**  
- Automatically split into **train / validation / test**  
- Data augmentation applied to training images  
- Works seamlessly with `ImageDataGenerator` or `tf.data`

---

## 🧪 Training Pipeline

Each model uses the same general workflow:

1. Load dataset  
2. Normalize images  
3. Split into train/val/test  
4. Build model  
5. Compile with Adam or SGD  
6. Apply callbacks  
   - EarlyStopping  
   - ReduceLROnPlateau  
7. Train the model  
8. Evaluate accuracy and loss  
9. Visualize training curves  

---

## 📈 Results Comparison

| Model | Training Time | Accuracy | Notes |
|-------|----------------|----------|-------|
| Custom CNN | Fast | Moderate | Good baseline |
| VGG19 | Medium | High | Beneficial transfer learning |
| ConvNeXt + Swin | Slow | Highest | Best overall performance |

(*Update with your actual accuracy values later if you want.*)

---

## ▶️ How to Run

### **1. Clone the repository**
```bash
git clone https://github.com/idkzeynav/Image-Classification-Using-Deep-Learning.git
cd Image-Classification-Using-Deep-Learning
