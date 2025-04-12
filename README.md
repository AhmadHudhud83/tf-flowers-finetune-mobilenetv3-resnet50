# 🌸 Flower Classification with Transfer Learning  
*Fine-Tuning ResNet50 and MobileNetV3 on TF Flowers Dataset*

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


## 📚 References  
- He et al. (2015) - *Deep Residual Learning for Image Recognition*  
- Howard et al. (2019) - *Searching for MobileNetV3*
