# FTL_Ethiopia_ML1_Gr7
# Project Idea
## Objective
Develop a multi-class deep learning system to detect **4 critical eye diseases** (Cataracts, Glaucoma, Diabetic Retinopathy, Normal) from fundus/OCT images.

## Problem Statement
Over **1 billion people** globally suffer preventable vision loss due to delayed diagnosis (WHO 2023). Current manual screening faces:
- **72%** diagnostic delay in rural areas
- **40%** error rate in early-stage detection

---

# SDG Relevance
### **Primary: SDG 3 (Good Health)**
- **Target 3.8**: Achieve universal health coverage (early diagnosis)
- **Target 3.4**: Reduce non-communicable diseases (prevent blindness)

### **Secondary: SDG 10 (Reduced Inequalities)**
- Enable low-cost screening in resource-limited regions

---

# Literature Examples

### Example 1:
- **Authors**: Muhammad Waqas Nadeem, Hock Guan Goh, Muzammil Hussain, Soung-Yue Liew, Ivan Andonovic, and Muhammad Adnan Khan (2022)  
- **Source**: Google Scholar  

#### Summary:
This review paper explores the application of deep learning (DL) in the analysis of **diabetic retinopathy (DR)**.  
It provides a comprehensive overview of DL methodologies for:
- **Retinal blood vessel segmentation**
- **Lesion detection & classification**
- **Validation techniques**  

The review also highlights challenges and future directions for more effective DR diagnosis models.

### Example 2:
- **Title**: *“Automatic detection of glaucoma via fundus imaging and artificial intelligence: A review”*  
- **Authors**: L.J. Coan, B.M. Williams, V.K. Adithya, et al. (Liverpool John Moores University, Aravind Eye Hospital, etc.), and G. Czanner (2023)  
- **Source**: Elsevier  

#### Summary:
This review examines **AI-enabled glaucoma detection frameworks** using segmented fundus images.  
Findings:
- 36 relevant papers from **2011 to 2021** identified two main approaches:
  1. **Logical rule-based frameworks** (set of predefined rules)
  2. **Machine learning/statistical modeling frameworks**  
- **Two-step AI models** (segmentation + classification) show **better interpretability** and require smaller training datasets.

---

# Data Description
### **Dataset Source**: Eye Disease Image Dataset  
### **Data Type**: Fundus images  

#### **Details**:
- **Classes**: 4 main categories  
  - Cataracts  
  - Diabetic Retinopathy  
  - Glaucoma  
  - Normal  
- **Total Images**: 16,242 (augmented dataset)  
- **Image Format**: JPEG (RGB)  
- **Image Size**: Typically **512x512 pixels**  

#### **Preprocessing Steps**:
1. **Resizing**: Normalize all images to **256x256 pixels**  
2. **Augmentation**: Apply random **rotations, flips, brightness adjustments** to improve robustness  
3. **Normalization**: Scale pixel values to **[0, 1]**  

---

# Technical Approach
### **Chosen Method**: Deep Learning  
#### **Justification**:
- **Complexity of Task**: Hierarchical feature extraction required, best suited for deep learning models  
- **Data Volume**: 16,242 augmented images provide sufficient data for **CNN training**  
- **Transfer Learning**: Using pre-trained models like **EfficientNet** or **ResNet** improves performance  

### **Proposed Architecture**:
1. **Base Model**: Use **EfficientNetB0** for feature extraction  
2. **Fine-Tuning**: Unfreeze last few layers for transfer learning  
3. **Dense Layers**: Add **fully connected layers** for classification  
4. **Output Layer**: Use **Softmax activation** for multi-class classification  
