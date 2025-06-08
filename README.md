# 🌸 Flower Classification with Transfer Learning  
**Fine-Tuning ResNet50 and MobileNetV3 on TF Flowers Dataset**


**For more info, consider reading the [transfer_learning_tf_flowers_report.pdf](transfer_learning_tf_flowers_report.pdf) documentation.**


---

## 📍 Project Overview  
This project applies transfer learning techniques using pre-trained ResNet50 and MobileNetV3 models to classify flower images from the TF Flowers dataset. By fine-tuning selected layers or blocks, the goal is to achieve high classification accuracy while analyzing the trade-offs between model complexity and performance.

---

## 🧾 Dataset  
- **Name**: TF Flowers  
- **Classes**: Daisy, Dandelion, Roses, Sunflowers, Tulips  
- **Total Samples**: 3,670  
- **Split**:
  - Training: 2,753 (75%)  
  - Validation: 550 (15%)  
  - Testing: 367 (10%)

---

## 🧠 Models Used  

### 🔹 ResNet50  
A deep residual network known for its high accuracy on ImageNet but with high computational cost.  

### 🔹 MobileNetV3  
A lightweight model designed for mobile deployment with reduced size and faster inference.

---

## ⚙️ Methodology  
- TensorFlow GPU was used for implementation and training.  
- Images were preprocessed using model-specific normalization and resizing.  
- Efficient data pipelines were built using `tf.data`.  
- Two fine-tuning strategies were tested:  
  - **Layer-wise** unfreezing (last *n* layers)  
  - **Block-wise** unfreezing (entire ResNet/MobileNet blocks)  
- Training used a low learning rate and the Adam optimizer.

---

## 📊 Results Summary  
After conducting several experiments with both models, the following results were achieved:

### **ResNet50**  
- **Best Experiment**:  
  - **Unfreeze from Layer 56** (Layer-wise unfreezing)  
  - **Training Accuracy**: 94.50%  
  - **Validation Accuracy**: 88.93%  
  - **Test Accuracy**: 92.64%  
- **Summary**: ResNet50 performed well, achieving high accuracy on the test set after unfreezing specific layers. However, it was more computationally expensive compared to MobileNetV3.

### **MobileNetV3**  
- **Best Experiment**:  
  - **Unfreeze 3 Blocks** (Block-wise unfreezing)  
  - **Training Accuracy**: 99.48%  
  - **Validation Accuracy**: 92.74%  
  - **Test Accuracy**: 94.28%  
- **Summary**: MobileNetV3 demonstrated excellent performance, especially in terms of test accuracy, while being computationally more efficient, making it ideal for mobile deployment.

Both models showed improvements through transfer learning, with MobileNetV3 being more suitable for resource-constrained environments.



## 📚 References  
- He et al. (2015) - *Deep Residual Learning for Image Recognition*  
- Howard et al. (2019) - *Searching for MobileNetV3*
