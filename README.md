# FTL_Ethiopia_ML1_Gr7
1. Project Idea
Objective: Develop a multi-class deep learning system to detect 4 critical eye diseases (cataracts, glaucoma, diabetic retinopathy, Normal) from fundus/OCT images.

Problem: Over 1 billion people globally suffer preventable vision loss due to delayed diagnosis (WHO 2023). Current manual screening faces:
72% diagnostic delay in rural areas
40% error rate in early-stage detection
2. SDG Relevance
Primary: SDG 3 (Good Health)
Target 3.8: Achieve universal health coverage (early diagnosis)
Target 3.4: Reduce non-communicable diseases (prevent blindness)
Secondary: SDG 10 (Reduced Inequalities)
Enable low-cost screening in resource-limited regions
3. Literature Examples
Example 1: 
Authors: Muhammad Waqas Nadeem, Hock Guan Goh, Muzammil Hussain, Soung-Yue Liew, Ivan Andonovic, and Muhammad Adnan Khan.(2022)
Source : Google scholar 


Summary:
This review paper explores the application of deep learning (DL) in the analysis of diabetic retinopathy (DR). 
The paper provides a comprehensive overview of DL methodologies and algorithms for various tasks, including retinal blood vessel segmentation, lesion detection, lesion classification, and validation. 
The review also highlights the challenges and future research directions in the development of more effective DL models for DR diagnosis and management. 

Example 2: “Automatic detection of glaucoma via fundus imaging and artificial intelligence: A review”
Author : L.J. Coan, B.M. Williams, V.K. Adithya, et al., (Liverpool John Moores University, Aravind Eye Hospital, etc.) and G. Czanner.(2023)
Source : Elsevier
Summary:
This is a review of artificial intelligence (AI) enabled glaucoma detection frameworks that produce and use segmented fundus images. 
The authors identified 36 relevant papers from 2011 to 2021 and found 2 main approaches: 1) logical rule-based frameworks, based on a set of rules, and 2) machine learning/statistical modeling-based frameworks. 
Two-step AI approaches may have advantages over the one-step approaches, including increased interpretability and the requirement of smaller datasets for training. 
The review highlights that the two-step AI frameworks have presented promising results in identifying the contours of the optic cup and disc.
4. Data Description
Dataset Source: Eye Disease Image Dataset
Data Type: Fundus images of various eye diseases
Details:
Classes: 4 main categories
Cataracts
Diabetic Retinopathy
Glaucoma
Normal
Total Images: 16242 augmented images (images per class vary)
Image Format: JPEG (RGB)
Image Size: Varies, but typically 512x512 pixels
Preprocessing Steps:
Resizing: Normalize all images to 256x256 pixels
Augmentation: Apply random rotations, flips, and brightness adjustments to enhance model robustness
Normalization: Scale pixel values to the range [0, 1]
5. Technical Approach
Chosen Method: Deep Learning
Justification:
Complexity of Task: Eye disease classification requires hierarchical feature extraction, which is best suited for deep learning models.
Data Volume: The dataset contains a sufficient number of images (5335 images/ 16242 augmented images) to train a convolutional neural network (CNN) effectively.
Transfer Learning: Leverage pre-trained models (e.g., EfficientNet, ResNet) to improve performance and reduce training time.
Proposed Architecture:
1.Base Model: Use EfficientNetB0 as the backbone for feature extraction.
2.Fine-tuning: Unfreeze the last few layers for transfer learning to adapt to the eye disease classification task.
3.Dense Layers: Add fully connected layers for classification.
4.Output Layer: Softmax activation for multi-class output.
